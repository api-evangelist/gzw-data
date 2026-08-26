---
name: gzw-data-check-freshness
description: Establish how current GZW Data is, and how healthy the API is, before quoting a game value to a user.
api: GZW Data API
base_url: https://gzw-data.dev/api/v1
authentication: none
operations:
- GET /api/v1/health
- GET /api/v1/ready
- GET /api/v1/stats
- GET /api/v1/spec
generated: '2026-08-26'
method: generated
source: openapi/gzw-data-openapi.json + https://gzw-data.dev/docs/ + lifecycle/gzw-data-lifecycle.yml
---

# Check GZW Data freshness before you quote a number

This API serves **community wiki data refreshed by a weekly scraper**, and the provider's own Terms
of Service say the data "may be incomplete, outdated, or incorrect" and that "game updates can change
values and mechanics without notice." A game patch can therefore make a weapon stat wrong days before
the scrape catches up. Check freshness whenever a user might act on the value.

## Steps

1. **Health and last scrape.** `GET /api/v1/health` returns `ok`, `status`, `ready`, `apiVersion`,
   `version`, `datasetCount` and the last-scrape information. Note the scrape timestamp.

2. **Readiness.** `GET /api/v1/ready` is documented to return `503` until the datasets have finished
   loading. A `503` here means cold start, not outage — retry after a short delay. There is **no
   status page** for this API; these two routes are the only operational signal published.

3. **Shape of the corpus.** `GET /api/v1/stats` returns per-dataset item counts plus the latest scrape
   timestamp. Use it to notice a dataset that has gone empty or shrunk sharply since your last run.
   (Live and documented, but not present in the published OpenAPI.)

4. **Contract drift.** `GET /api/v1/spec` returns the OpenAPI 3.0.3 document. Its `info.version` is
   the project version (4.0.0), which is independent of the `/api/v1` path prefix — do not read one
   as the other.

## Rules

- **State the age.** When you report a stat, say when it was scraped. Error responses also carry a
  `dataVersion` timestamp you can quote.
- **Never present this as official.** GZW Data is an unofficial fan project, not affiliated with or
  endorsed by the game's publisher. The provider says this on every page.
- **No SLA.** The Terms state the service is provided as-available with no uptime, response-time or
  data-retention guarantee, and that any endpoint may be changed or discontinued without notice.
  Degrade gracefully; do not build a hard dependency without a cache.
- **Rate limit:** 100 requests/minute/IP. These three checks cost three requests — run them once per
  session, not per lookup.
