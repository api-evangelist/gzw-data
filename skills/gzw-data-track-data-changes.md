---
name: gzw-data-track-data-changes
description: Detect whether the GZW dataset snapshot moved since you last cached it, and find out which datasets changed, before re-pulling anything.
api: GZW Data API
base_url: https://gzw-data.dev/api/v1
authentication: none
operations:
- GET /api/v1/version
- GET /api/v1/changes
- GET /api/v1/schema/{dataset}
- GET /api/v1/items/{id}/context
generated: '2026-09-03'
method: generated
source: openapi/_original/gzw-data-openapi.json (4.2.0) + https://gzw-data.dev/docs/ + live probes 2026-09-03
---

# Track GZW data changes instead of re-pulling everything

Implementation 4.2.0 added four routes that let a client answer "did anything change?" in **one
request** instead of re-downloading 85 datasets. Every route below is declared in the published
OpenAPI and was probed live on 2026-09-03.

## Steps

1. **Pin what you have.** `GET /api/v1/version` returns `implementationVersion` (the API build,
   `4.2.0` at time of writing), `apiVersion` (`v1`), `dataVersion` (an ISO timestamp), and a
   `snapshot` object with `snapshotId` and a per-dataset record count. Store `dataVersion` and
   `snapshotId` alongside anything you cache.

2. **Compare cheaply.** Every ordinary data response also carries `dataVersion`. If the
   `dataVersion` on a cheap call matches what you stored, the snapshot has not moved and your
   cache is current — no further requests needed.

3. **Find out what moved.** `GET /api/v1/changes` returns `current`, `latest` and `previous`
   snapshots plus a computed `changes` object with `added`, `removed` and per-dataset entries.
   Re-pull only the datasets it names.

4. **Re-read the field shape before parsing.** `GET /api/v1/schema/{dataset}` returns generated
   field metadata — types, `presentCount`, `optional`, `nullable` and a stable `example` — for one
   dataset. Fields are observed from the scraped data, so a wiki change can add or drop a field
   without any version moving.

5. **Resolve a vendor without a second search.** `GET /api/v1/items/{id}/context` returns the item
   plus its `sold_by` vendor resolved into real vendor objects, plus a `references` array.

## Rules

- **`/api/v1/changes` keeps a history depth of 2.** Only the latest and previous snapshots are
  retained (`historyCount: 2`). If you poll less often than the scraper runs, the diff will not
  cover what you missed — fall back to comparing `snapshot.datasets` counts from
  `/api/v1/version` against your own stored copy.
- **`/api/v1/items/{id}/context` is scoped to the `items` dataset only.** Passing an id from
  `weapons` or `loot_items` returns `404 RECORD_NOT_FOUND` with `"dataset": "items"` — verified by
  probe. For the other 84 datasets, resolve `sold_by` the old way: `GET /api/v1/vendors?search=<value>`.
- **The provider's own caveat on `context`:** references are "exact or textual matches found in the
  current datasets; they are not guaranteed gameplay relationships." Do not present them as
  authoritative game mechanics.
- **`/api/v1/changes` compares dataset SNAPSHOTS, not the API contract.** It will not tell you that
  an endpoint was added or a response shape changed. There is no prose changelog for that — see
  `changelog/gzw-data-changelog.yml`.
- **These routes are cheap; use them instead of polling data.** One `/version` call replaces
  85 collection calls against a 100 req/min/IP budget.
