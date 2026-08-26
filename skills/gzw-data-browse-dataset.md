---
name: gzw-data-browse-dataset
description: Filter, search, sort and page through any of the 85 auto-discovered Gray Zone Warfare datasets without exhausting the rate limit.
api: GZW Data API
base_url: https://gzw-data.dev/api/v1
authentication: none
operations:
- GET /api/v1/metadata
- GET /api/v1/metadata/{dataset}
- GET /api/v1/{dataset}
generated: '2026-08-26'
method: generated
source: openapi/gzw-data-openapi.json + https://gzw-data.dev/docs/#queries + conventions/gzw-data-conventions.yml
---

# Browse and filter a GZW dataset

Every collection route takes the same small, composable query vocabulary. **None of these
parameters are declared in the published OpenAPI** — they exist only in the provider's docs — so
they are listed here explicitly.

| Parameter | Meaning |
|---|---|
| `?{field}={value}` | Equality filter on any string field, e.g. `?type=Keycard` |
| `?search={q}` | Full-text search across the record's fields |
| `?sort={field}:asc\|desc` | Sort by a field |
| `?page={n}&per_page={n}` | Page-number pagination; `per_page` defaults to 50, caps at 500 |
| `?all=true` | Return every filtered record with no pagination |

## Steps

1. **Discover the field names before filtering.** Call `GET /api/v1/metadata/{dataset}` — it returns
   the observed fields, detected types, optional/nullable flags and a stable example value. Filtering
   on a field that does not exist on that dataset silently returns unfiltered results.

2. **Filter server-side, not client-side.** Combine filters with search and pagination in one
   request, e.g.
   `GET /api/v1/keys?type=Keycard&search=alpha&page=1&per_page=20`.

3. **Page deliberately.** Read `total` and `totalPages` from the envelope and stop at `totalPages`.
   Stop early on an empty page or a page shorter than `perPage`.

4. **Use `?all=true` only on a narrow filter.** It bypasses pagination entirely. On a large dataset
   that is one very big response; filter first.

## Rules

- **Validate your own inputs.** The API is lenient: `?per_page=99999` (above the documented cap of
  500) and `?page=abc` both return `200` rather than an error — verified by probe. You will not get a
  4xx telling you the query was wrong, so check `count`, `perPage` and `total` in the response
  against what you asked for.
- **Rate limit:** 100 requests/minute/IP. Prefer one larger page over many small ones; `per_page=500`
  costs the same one request as `per_page=10`.
- **Datasets change without a version bump.** New wiki categories become endpoints and removed ones
  become 404s, with no change to `/api/v1`. Re-read `GET /api/v1/metadata` rather than caching a
  dataset list across days.
- **Three routes are unions, not datasets:** `/api/v1/armor` (vests + helmets + glasses),
  `/api/v1/weapon_parts`, `/api/v1/helmet_mods` (night vision + mounts). They accept the same query
  parameters.
- **Read-only.** All 352 operations are `GET`.
