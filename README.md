# H1

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

H1 (h1.co) is a New York City-based healthcare data and technology company, founded in 2017, that combines deep healthcare provider data with agentic AI to power drug development, medical and commercial engagement, care navigation, and provider and network intelligence for life sciences, pharma, health plans, and digital health organizations across the United States. Its developer-facing API is the Ribbon Health API (H1 acquired Ribbon Health), a proprietary REST API served over HTTPS at https://api.ribbonhealth.com that provides accurate, comprehensive data on healthcare providers, locations, insurances, procedures, price transparency, cost estimates, and insurance eligibility. Two OpenAPI 3.1 contracts are published - the 75-operation v1 API under /v1, and a newer 7-operation location-first Price Transparency v2 surface under /v2 that H1 tells new integrations to prefer over the legacy provider-first /v1/pricing endpoints. The API is not FHIR-based and does not expose a SMART-on-FHIR or Da Vinci PDEX Plan-Net surface; it authenticates with a bearer API key, has no OAuth scopes, and gates product families on per-account entitlement flags. It is segmented into provider, location, custom-filter, focus-area, price-transparency (v1 and v2), cost-estimate/eligibility, organization, reference-data, and network-analysis product families. Access is gated behind a request-demo / API-key sign-up rather than fully self-serve, and no pricing, plans, SDKs, sandbox, changelog or webhook surface is published.

**Areas:** Healthcare · United States · Life Sciences · Provider Data · Healthcare API · Price Transparency · Eligibility · Network Intelligence · Digital Health · Pharma

## H1 on APIs.io

Everything profiled for H1 is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/h1/](https://apis.io/providers/h1/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [H1 Cost Estimates API](https://apis.io/apis/h1/h1-insights-cost-estimates-api/) — The Cost Estimates API from H1 — 4 operation(s) for cost estimates.
- [H1 Filters API](https://apis.io/apis/h1/h1-insights-filters-api/) — The Filters API from H1 — 4 operation(s) for filters.
- [H1 Focus Area Endpoints API](https://apis.io/apis/h1/h1-insights-focus-area-endpoints-api/) — The Focus Area Endpoints API from H1 — 6 operation(s) for focus area endpoints.
- [H1 Locations API](https://apis.io/apis/h1/h1-insights-locations-api/) — The Locations API from H1 — 5 operation(s) for locations.
- [H1 Networks API](https://apis.io/apis/h1/h1-insights-networks-api/) — The Networks API from H1 — 1 operation(s) for networks.
- [H1 Organizations API](https://apis.io/apis/h1/h1-insights-organizations-api/) — The Organizations API from H1 — 2 operation(s) for organizations.
- [H1 Price Transparency API](https://apis.io/apis/h1/h1-insights-price-transparency-api/) — The Price Transparency API from H1 — 8 operation(s) for price transparency.
- [H1 Providers API](https://apis.io/apis/h1/h1-insights-providers-api/) — The Providers API from H1 — 10 operation(s) for providers.
- [H1 Reference Endpoints API](https://apis.io/apis/h1/h1-insights-reference-endpoints-api/) — The Reference Endpoints API from H1 — 13 operation(s) for reference endpoints.
- [H1 TI Ns API](https://apis.io/apis/h1/h1-insights-tins-api/) — The TINs API from H1 — 2 operation(s) for tins.
- [H1 Virtual Care Platforms API](https://apis.io/apis/h1/h1-insights-virtual-care-platforms-api/) — The Virtual Care Platforms API from H1 — 2 operation(s) for virtual care platforms.
- [H1 Price Transparency v2 API](https://apis.io/apis/h1/h1-price-transparency-v2-api/) — Location-first negotiated rates under `/v2/*`. Prefer these endpoints for new integrations. Carrier ids come from `GET /v2/carriers` and are not…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [h1-ribbon-health](https://apis.io/servers/h1/h1-ribbon-health/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [H1 Agentic Access](https://apis.io/agentic-access/h1/h1-agentic-access/)

#### Collections (12)

Postman and Open Collection request collections.

- [Ribbon Health Cost Estimates API](https://apis.io/collections/h1/open-h1-cost-estimates-api/)
- [Ribbon Health Filters API](https://apis.io/collections/h1/open-h1-filters-api/)
- [Ribbon Health Focus Area Endpoints API](https://apis.io/collections/h1/open-h1-focus-area-endpoints-api/)
- [Ribbon Health Locations API](https://apis.io/collections/h1/open-h1-locations-api/)
- [Ribbon Health Networks API](https://apis.io/collections/h1/open-h1-networks-api/)
- [Ribbon Health Organizations API](https://apis.io/collections/h1/open-h1-organizations-api/)
- [Ribbon Health Price Transparency API](https://apis.io/collections/h1/open-h1-price-transparency-api/)
- [Ribbon Health Providers API](https://apis.io/collections/h1/open-h1-providers-api/)
- [Ribbon Health Reference Endpoints API](https://apis.io/collections/h1/open-h1-reference-endpoints-api/)
- [Ribbon Health TI Ns API](https://apis.io/collections/h1/open-h1-tins-api/)
- [Ribbon Health Virtual Care Platforms API](https://apis.io/collections/h1/open-h1-virtual-care-platforms-api/)
- [Ribbon Health API](https://apis.io/collections/h1/open-ribbon-health-api/)

#### Overlays (3)

OpenAPI overlays, including conversational phrasing for each operation.

- [H1 Openapi Overlay](https://apis.io/overlays/h1/h1-openapi-overlay/)
- [H1 Price Transparency V2 Overlay](https://apis.io/overlays/h1/h1-price-transparency-v2-overlay/)
- [H1 Ribbon Health Api Overlay](https://apis.io/overlays/h1/h1-ribbon-health-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [H1 Authentication](https://apis.io/security/h1/h1-authentication/)
- [H1 Domain Security](https://apis.io/security/h1/h1-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [H1 Plans Pricing](https://apis.io/plans/h1/h1-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [H1 Rate Limits](https://apis.io/rate-limits/h1/h1-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://h1.co/)
- [Documentation](https://ribbon.readme.io/docs/welcome-to-the-ribbon-health-api)
- [Getting started](https://ribbon.readme.io/docs/getting-started)
- [API reference](https://ribbon.readme.io/reference)
- [Sign up](https://h1.co/request-demo/)
- [Support](https://h1.co/contact/)
- [Blog](https://h1.co/blog/)
- [Terms of service](https://h1.co/terms-of-use/)
- [Privacy policy](https://h1.co/privacy-policy/)
- [GitHub](https://github.com/RibbonHealth)
- [Status](https://status.ribbonhealth.com)

## API Evangelist rating

**Kin Score 48.3** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 54.2 |
| Contract governance | 4.5 |
| Operational transparency | 57.9 |
| Developer ergonomics | 49.4 |
| Access clarity | 34.2 |

**Agent readiness 31.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 30.5** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/h1/](https://apis.io/providers/h1/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for H1: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/h1/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
