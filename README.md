# TVmaze (tvmaze)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
