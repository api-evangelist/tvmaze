# TVmaze (tvmaze)

TVmaze is a community-driven TV show database that publishes a free RESTful API for TV show, episode, season, cast, crew, and broadcast/streaming schedule data. The public API is anonymous, CORS-enabled, and licensed under CC BY-SA 4.0. A paid Premium subscription unlocks a separate user-scoped API for managing follows, votes, marks, tags, and scrobbling.

- **Website:** https://www.tvmaze.com
- **API homepage:** https://www.tvmaze.com/api
- **Premium signup:** https://www.tvmaze.com/premium
- **APIs.yml:** [apis.yml](apis.yml)

## Type

- **x-type:** company
- **x-tier:** 2 (profiled public and premium APIs)
- **source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Video

## APIs

### TVmaze Public API

Anonymous, free REST API for shows, episodes, seasons, cast, crew, schedules, and incremental updates. Rate limit is at least 20 calls every 10 seconds per IP. Most endpoints are edge-cached for 60 minutes.

- **Base URL:** `https://api.tvmaze.com`
- **Documentation:** https://www.tvmaze.com/api
- **OpenAPI:** [openapi/tvmaze-public-openapi.yml](openapi/tvmaze-public-openapi.yml)
- **JSON Schemas:** `json-schema/tvmaze-public-*.json` (16 schemas)
- **Naftiko Capabilities:**
  - [capabilities/public-search.yaml](capabilities/public-search.yaml) — Search Shows / People / Single / Lookup (4 ops)
  - [capabilities/public-schedule.yaml](capabilities/public-schedule.yaml) — TV, Web, Full schedules (3 ops)
  - [capabilities/public-shows.yaml](capabilities/public-shows.yaml) — Show details, episodes, seasons, cast, crew, akas, images (11 ops)
  - [capabilities/public-seasons.yaml](capabilities/public-seasons.yaml) — Season retrieval and episode listing (2 ops)
  - [capabilities/public-episodes.yaml](capabilities/public-episodes.yaml) — Episode, guest cast, guest crew (3 ops)
  - [capabilities/public-people.yaml](capabilities/public-people.yaml) — People index, profile, credits (5 ops)
  - [capabilities/public-updates.yaml](capabilities/public-updates.yaml) — Incremental sync for shows and people (2 ops)
- **Operation Examples:** `examples/public-*.json` (10 real-data response samples)

### TVmaze Premium User API

User-scoped REST API available only to Premium subscribers. Authenticated via HTTP Basic using the TVmaze username and API key, with a device-pairing flow at `/v1/auth/start` + `/v1/auth/poll`. The `/v1/scrobble/*` endpoints are available to free users as well.

- **Base URL:** `https://api.tvmaze.com/v1`
- **Documentation:** https://static.tvmaze.com/apidoc/
- **OpenAPI:** [openapi/tvmaze-premium-openapi.yml](openapi/tvmaze-premium-openapi.yml)
- **JSON Schemas:** `json-schema/tvmaze-premium-*.json` (16 schemas)
- **Naftiko Capabilities:**
  - [capabilities/premium-auth.yaml](capabilities/premium-auth.yaml) — Device-pairing + credential validation (3 ops)
  - [capabilities/premium-scrobbling.yaml](capabilities/premium-scrobbling.yaml) — Bulk and single episode scrobbling (4 ops)
  - [capabilities/premium-marked-episodes.yaml](capabilities/premium-marked-episodes.yaml) — Watched / acquired episode tracking (4 ops)
  - [capabilities/premium-followed-networks.yaml](capabilities/premium-followed-networks.yaml) — Follow / unfollow networks (4 ops)
  - [capabilities/premium-followed-people.yaml](capabilities/premium-followed-people.yaml) — Follow / unfollow people (4 ops)
  - [capabilities/premium-followed-shows.yaml](capabilities/premium-followed-shows.yaml) — Follow / unfollow shows (4 ops)
  - [capabilities/premium-followed-webchannels.yaml](capabilities/premium-followed-webchannels.yaml) — Follow / unfollow web channels (4 ops)
  - [capabilities/premium-tagged-shows.yaml](capabilities/premium-tagged-shows.yaml) — User-defined show tags (7 ops)
  - [capabilities/premium-voted-episodes.yaml](capabilities/premium-voted-episodes.yaml) — 1-10 episode votes (4 ops)
  - [capabilities/premium-voted-shows.yaml](capabilities/premium-voted-shows.yaml) — 1-10 show votes (4 ops)

## Common Artifacts

- **JSON-LD context:** [json-ld/tvmaze-context.jsonld](json-ld/tvmaze-context.jsonld) — schema.org alignment for shows, episodes, people, cast/crew credits.
- **Spectral rules:** [rules/tvmaze-rules.yml](rules/tvmaze-rules.yml) — enforces TVmaze API conventions (Title Case summaries, operationId casing, no path extensions, integer IDs, /v1 namespace, 429 documented, etc.).
- **Vocabulary:** [vocabulary/tvmaze-vocabulary.yml](vocabulary/tvmaze-vocabulary.yml) — domain terms across television, people, and schedule surfaces.
- **JSON Structures:** `json-structure/tvmaze-*.json` — flattened structural docs derived from OpenAPI components.
- **Plans:** [plans/tvmaze-plans-pricing.yml](plans/tvmaze-plans-pricing.yml) — Public (free), Premium Bronze/Silver/Gold, Enterprise.
- **Rate Limits:** [rate-limits/tvmaze-rate-limits.yml](rate-limits/tvmaze-rate-limits.yml) — 20 req / 10 sec / IP + edge-cache policies.
- **FinOps:** [finops/tvmaze-finops.yml](finops/tvmaze-finops.yml) — FinOps Framework / FOCUS mapping for the subscription surface.

## Pricing & Plans (summary)

| Plan | Cycle | Notes |
|---|---|---|
| Public API | Free | Anonymous, personal use, CC BY-SA attribution |
| Premium Bronze | $25/yr | Unlocks the user-scoped API, weekly calendars, bulk marking |
| Premium Silver | $50/yr | Adds custom iCal + RSS feeds |
| Premium Gold | $100/yr | Adds influence over pending features |
| Enterprise | Contact sales | Commercial / high-volume licensing |

Rate limit: at least **20 calls every 10 seconds per IP** for both public and premium calls.

## Tooling

- **Python SDK (community, hosted under the TVmaze GitHub org):** https://github.com/tvmaze/tvmaze
- **Community MCP servers:**
  - https://github.com/pipeworx-io/mcp-tvmaze
  - https://github.com/vivekjne/tvmaze-mcp-server
  - https://github.com/DudaAraujo14/tvmaze-mcp-server
  - https://github.com/Formacio-3Cat/3cat-tvmaze-mcp

## Tags

Video, Television, Streaming, Schedule, Metadata, Entertainment, Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## Maintainers

- **Kin Lane** — kin@apievangelist.com
