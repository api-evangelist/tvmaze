# TVmaze (tvmaze)

TVmaze is a community-driven TV show database that publishes a free RESTful API for TV show, episode, season, cast, crew, and broadcast/streaming schedule data. The public API is anonymous, CORS-enabled, and licensed under CC BY-SA 4.0. A paid Premium subscription unlocks a separate user-scoped API for managing follows, votes, marks, tags, and scrobbling.

**APIs.json:** [https://www.tvmaze.com/api](https://www.tvmaze.com/api)

## Tags

- Video
- Television
- Streaming
- Schedule
- Metadata
- Entertainment
- Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## APIs

### TVmaze Public API

Anonymous, free REST API for shows, episodes, seasons, cast, crew, schedules, and incremental updates. Rate limit is at least 20 calls every 10 seconds per IP. Most endpoints are edge-cached for 60 minutes. Licensed under CC BY-SA 4.0 with attribution to tvmaze.com required.

- **Human URL:** [https://www.tvmaze.com/api](https://www.tvmaze.com/api)
- **Base URL:** `https://api.tvmaze.com`

#### Tags

- Video
- Television
- Schedule

#### Properties

- [Documentation](https://www.tvmaze.com/api)
- [OpenAPI](openapi/tvmaze-public-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvmaze-public.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvmaze-public.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/tvmaze-public-show-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-episode-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-season-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-person-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-character-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-castcredit-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-crewcredit-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-network-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-webchannel-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-country-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-image-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-schedule-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-rating-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-externals-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-links-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-public-aka-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/public-get-show-example.json)
- [Example](examples/public-get-show-episodes-example.json)
- [Example](examples/public-get-show-seasons-example.json)
- [Example](examples/public-get-show-cast-example.json)
- [Example](examples/public-get-episode-example.json)
- [Example](examples/public-get-season-example.json)
- [Example](examples/public-get-person-example.json)
- [Example](examples/public-search-shows-example.json)
- [Example](examples/public-get-schedule-example.json)
- [Example](examples/public-get-show-updates-example.json)
- [Rate Limits](rate-limits/tvmaze-rate-limits.yml)

### TVmaze Premium User API

User-scoped REST API available only to Premium subscribers. Provides read-write access to a user's followed shows/people/networks/web-channels, marked episodes, voted shows and episodes, tagged shows, and scrobbling. Authenticated via HTTP Basic using the TVmaze username and API key, with a complementary device-pairing flow exposed at /v1/auth/start and /v1/auth/poll. Available even for free users on the scrobbling endpoints.

- **Human URL:** [https://static.tvmaze.com/apidoc/](https://static.tvmaze.com/apidoc/)
- **Base URL:** `https://api.tvmaze.com/v1`

#### Tags

- Video
- Television
- Premium
- User

#### Properties

- [Documentation](https://static.tvmaze.com/apidoc/)
- [OpenAPI](openapi/tvmaze-premium-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tvmaze-premium.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tvmaze-premium.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Authentication](https://static.tvmaze.com/apidoc/)
- [Pricing](https://www.tvmaze.com/premium)
- [JSON Schema](json-schema/tvmaze-premium-show-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-episode-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-person-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-network-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-webchannel-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-markedepisode-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-showfollow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-personfollow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-networkfollow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-webchannelfollow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-showvote-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-episodevote-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-tag-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-taginstance-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-marktype-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tvmaze-premium-bulkresponse-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Rate Limits](rate-limits/tvmaze-rate-limits.yml)

## Common Properties

- [Website](https://www.tvmaze.com)
- [Documentation](https://www.tvmaze.com/api)
- [API Reference](https://static.tvmaze.com/apidoc/)
- [Sign Up](https://www.tvmaze.com/account/register)
- [Login](https://www.tvmaze.com/account/login)
- [Console](https://www.tvmaze.com/dashboard)
- [Pricing](https://www.tvmaze.com/premium)
- [Plans](plans/tvmaze-plans-pricing.yml)
- [Rate Limits](rate-limits/tvmaze-rate-limits.yml)
- [Fin Ops](finops/tvmaze-finops.yml)
- [Support](https://www.tvmaze.com/request/create)
- [F A Q](https://www.tvmaze.com/faqs)
- [Changelog](https://www.tvmaze.com/threads/4/api-changelog)
- [Blog](https://www.tvmaze.com/blog)
- [Terms of Service](https://www.tvmaze.com/site/tos)
- [Privacy Policy](https://www.tvmaze.com/site/privacy)
- [Legal](https://www.tvmaze.com/site/copyright)
- [Data Privacy](https://www.tvmaze.com/faqs/9/data-policies)
- [GitHub Organization](https://github.com/tvmaze)
- [SDK](https://github.com/tvmaze/tvmaze)
- [Spectral Rules](rules/tvmaze-rules.yml)
- [Vocabulary](vocabulary/tvmaze-vocabulary.yml)
- [JSON-LD](json-ld/tvmaze-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)
- [Tools](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
