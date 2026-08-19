---
name: Shop procedure and bundle prices near a location (Price Transparency v2)
description: Use H1's location-first Price Transparency v2 endpoints to resolve a procedure or care cluster, pick a carrier, and return the cheapest nearby facility prices.
api: openapi/h1-price-transparency-v2-openapi.json
operations: [getV2Procedures, getV2CareClusters, getV2Carriers, getV2PricingLocationProcedures, getV2PricingLocationCareClusters, getV2LocationProcedurePricing, getV2LocationCareClusterPricing]
---

# Shop procedure and bundle prices near a location (Price Transparency v2)

Price Transparency v2 (`/v2/*`) is **location-first**: prices hang off facilities, not providers. It is a
separate surface from the legacy provider-first `/v1/pricing/*` endpoints, and H1's own contract says to
prefer v2 for new integrations. Provider-scoped v2 routes are not live yet.

## Before you start
- Auth is a bearer API key: `Authorization: Bearer {customer_token}`.
- Every `/v2/*` path is gated on the `doctors.can_price_transparency` account entitlement. A `403` means
  the key is not entitled — it does not mean the request was malformed.
- All `/v2/*` endpoints share one rate limit: 1,000 requests per minute. No `RateLimit-*` or
  `Retry-After` header is returned, so budget client-side; a `429` is the only signal you get.

## Steps
1. Resolve the procedure. Call `getV2Procedures` to look up a CPT (or other) code and confirm its
   description and which care cluster it belongs to. This endpoint returns **no dollar amounts**.
2. If the user is shopping an episode rather than a single code, call `getV2CareClusters` instead to find
   the cluster (for example `JOINT_REPLACEMENT`) and the procedure set it expects.
3. Resolve the carrier. Call `getV2Carriers` and take the `carrier_id` from there. **Do not reuse a v1
   carrier UUID** — v2 carrier ids are string business ids and the two are not interchangeable.
4. Shop by geography. Call `getV2PricingLocationProcedures` (single procedure) or
   `getV2PricingLocationCareClusters` (bundle) with the code plus **either** `address` **or** both `lat`
   and `lng`. Results come back cheapest-first — by `min` for procedures, by `bundle_price` for clusters.
5. Drill into one facility. Once the user picks a site, call `getV2LocationProcedurePricing` or
   `getV2LocationCareClusterPricing` with that `location_id` to list everything priced there for the
   carrier. `location_id` accepts either the integer location id or the location UUID.

## Rules
- **Location is required on the geo searches.** v1 silently defaulted a missing location to a New York
  City address; v2 returns `400`. Supplying only one of `lat`/`lng`, or an address that fails to
  geocode, is also `400`. Never let a caller fall through without a location.
- **Filter with `carrier_id`, not `plan_id`.** `plan_id` is in the contract but returns `501` until
  plan-to-carrier mapping ships. Sending both `carrier_id` and `plan_id` returns `400`.
- Every v2 response uses the same envelope — `parameters`, `total_count`, `page`, `page_size`, `data` —
  so paginate with `page`/`page_size` and read `parameters` to confirm which filters actually applied.
- On the cluster endpoints, check `completeness_pct` / `missing_procedures` before quoting a bundle: a
  low completeness means the site has pricing for only part of the expected procedure set.
- An unknown `location_id` returns `404`. Full status handling is in `errors/h1-problem-types.yml`.
- These are negotiated-rate disclosures, not a quote. For a member-specific out-of-pocket figure use the
  v1 eligibility and cost-estimate flow (`skills/h1-eligibility-check.md`).
