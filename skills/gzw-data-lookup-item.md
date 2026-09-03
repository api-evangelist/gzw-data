---
name: gzw-data-lookup-item
description: Resolve a Gray Zone Warfare item, weapon, key or task by its display name and return the full record from the GZW Data API.
api: GZW Data API
base_url: https://gzw-data.dev/api/v1
authentication: none
operations:
- GET /api/v1/metadata
- GET /api/v1/{dataset}
- GET /api/v1/{dataset}/{id}
- GET /api/v1/search
generated: '2026-08-26'
method: generated
source: openapi/_original/gzw-data-openapi.json + https://gzw-data.dev/docs/ + conventions/gzw-data-conventions.yml
---

# Look up one GZW item by name

The GZW Data API keys every record on a **slugified id** (`AK-12` → `ak-12`) and matches it
**exactly** — there is no fuzzy lookup on `/{dataset}/{id}`. A user will almost always give you a
display name, so resolve the name to an id first.

The published OpenAPI declares **no operationIds**, so every step below is bound to its HTTP method
and path, which are the real, verified identifiers this contract exposes.

## Steps

1. **Pick the dataset.** If you do not already know which of the 85 datasets holds the thing,
   call `GET /api/v1/metadata`. It returns the dataset registry — `name`, `file`, `itemCount` and
   the observed `fields` for each. Datasets are auto-discovered from the wiki, so never hardcode
   the list; read it.

2. **Resolve the name to an id.** Call `GET /api/v1/{dataset}?search={name}`. The response envelope
   is `{data, count, page, perPage, total, totalPages, source, timestamp}`. Read `data[].id`.
   - If you do not know the dataset at all, use `GET /api/v1/search?q={name}` instead — it searches
     across datasets and returns results grouped by dataset name. **Caveat:** this route is live and
     documented but is *not* in the published OpenAPI, so treat it as best-effort.

3. **Fetch the record.** Call `GET /api/v1/{dataset}/{id}` with the exact id from step 2.
   A wrong id returns `404` with `{"error":{"code":"RECORD_NOT_FOUND","dataset":"…","id":"…"}}`.

4. **Report the record.** Fields are dataset-specific and are all **strings with units embedded**
   (`"weight":"3.553 kg"`, `"fire_rate":"700 RPM"`). Do not parse them into numbers without saying
   you did. `image` is an absolute URL on the Fandom CDN.

## Rules

- **Read-only.** Every operation in this contract is a `GET`. Never attempt a write; there is none.
- **Rate limit:** 100 requests/minute/IP, best-effort. Watch `X-RateLimit-Remaining`; on `429`
  honour `Retry-After`. Chain steps 1→3 rather than fanning out across datasets.
- **Cache.** Data routes send `Cache-Control: public, max-age=300`. Reuse a metadata response
  across a session instead of re-fetching it per lookup.
- **Freshness.** Data is scraped weekly from the community GZW Fandom Wiki and may be incomplete or
  out of date after a game patch. The provider's own Terms say so. Check `dataVersion` / the last
  scrape time from `GET /api/v1/health` before asserting a value is current.
- **Not authoritative.** This is a fan project, not affiliated with the game's publisher. Say so
  when a user might act on the numbers.
