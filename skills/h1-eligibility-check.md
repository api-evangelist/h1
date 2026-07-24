---
name: Check member insurance eligibility
description: Confirm a supported eligibility insurance partner, then verify a member's coverage, deductible, and cost-share.
api: openapi/ribbon-health-api-openapi.json
operations: [getEligibilityInsurancePartners, getEligibility]
---

# Check member insurance eligibility

## Steps
1. Call `getEligibilityInsurancePartners` to confirm the member's insurance is a supported eligibility partner (and get its identifier).
2. Call `getEligibility` (POST /eligibility) with the member and insurance details to verify current coverage and benefits - deductible and out-of-pocket progress, copay, and coinsurance.

## Rules
- Eligibility is a POST endpoint; supply member identifiers in the request body.
- Only insurances returned by `getEligibilityInsurancePartners` are supported for eligibility checks.
- Authenticate with `Authorization: Bearer {customer_token}`; handle non-2xx JSON errors per errors/h1-problem-types.yml.
- This handles PHI - do not log member identifiers or responses in shared/insecure locations.
