---
name: Search and retrieve healthcare providers
description: Find providers by specialty, procedure, insurance, and geography, then pull a full provider profile by NPI.
api: openapi/ribbon-health-api-openapi.json
operations: [getCustomProviders, getCustomProvider, getSpecialties, getInsurances]
---

# Search and retrieve healthcare providers

Use the H1 (Ribbon Health) API to find providers and read their full profiles. All requests use `Authorization: Bearer {customer_token}` against `https://api.ribbonhealth.com/v1`.

## Steps
1. (Optional) Resolve a specialty UUID with `getSpecialties` and/or an insurance with `getInsurances` if you want to constrain the search.
2. Call `getCustomProviders` to search. Pass search criteria (specialty, procedure, insurance, `location`, `distance`) plus `page` / `page_size` for pagination.
3. For a specific match, call `getCustomProvider` with the provider's `npi` to retrieve the full profile (locations, specialties, insurances, clinical areas).

## Rules
- Providers are keyed by **NPI** (National Provider Identifier), not an internal UUID.
- List endpoints paginate with `page` and `page_size`.
- Respect documented rate limits: `v1/custom/providers` = 1,000 calls/min, `v1/custom/providers/{npi}` = 5,000 calls/min; a `429 rate_limit_exceeded` signals throttling (see rate-limits/h1-rate-limits.yml).
- Errors are JSON bodies (not RFC 9457); handle `400` (bad params), `403` (entitlement), `404` (unknown NPI). See errors/h1-problem-types.yml.
