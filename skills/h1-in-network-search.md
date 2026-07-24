---
name: Find in-network providers for an insurance
description: Resolve an insurance, then search for providers that accept it and inspect network composition by geography.
api: openapi/ribbon-health-api-openapi.json
operations: [getInsurances, getCustomProviders, getNetworkAnalysis]
---

# Find in-network providers for an insurance

## Steps
1. Call `getInsurances` to search insurances and obtain the target `insurance_uuid` / `insurance_id`.
2. Call `getCustomProviders` filtered by that insurance (plus `location` / `distance` / specialty) to list in-network providers, paginating with `page` / `page_size`.
3. (Optional) Call `getNetworkAnalysis` to assess network composition and adequacy across a geography (e.g. counties) for network-adequacy use cases.

## Rules
- Insurances are referenced by standard Ribbon insurance UUIDs.
- Rate limits: `v1/insurances` = 1,000 calls/min; back off on `429 rate_limit_exceeded`.
- Handle `400` / `403` / `404` per errors/h1-problem-types.yml.
