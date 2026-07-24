---
name: Price-transparency and procedure cost lookup
description: Search negotiated rates by procedure, provider, and insurance, and estimate procedure costs by location.
api: openapi/ribbon-health-api-openapi.json
operations: [getProcedures, getPricingProviders, getPricingProviderProcedure, getProcedureCostEstimate]
---

# Price-transparency and procedure cost lookup

## Steps
1. Call `getProcedures` to resolve the target `procedure_uuid` (or `procedure_code`).
2. Call `getPricingProviders` to search providers performing that procedure and find the lowest insurance-specific negotiated rate in an area (pass insurance, `location`, `distance`).
3. For a single provider, call `getPricingProviderProcedure` with `npi` + `procedure_uuid` to compare that provider's prices across locations.
4. For a consumer estimate, call `getProcedureCostEstimate` with the procedure and the user's location.

## Rules
- Pricing data is drawn from payer price-transparency disclosures; use `getPricingCarriers` / `getPricingCarrier` to check data recency per carrier.
- `getPricingCarrierNames` and `getPricingVersionCarrier` are **deprecated** - use `getPricingCarriers` / `getPricingCarrier` instead (see lifecycle/h1-lifecycle.yml).
- Handle `400` / `404` per errors/h1-problem-types.yml.
