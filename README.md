# H1 (h1)

H1 (h1.co) is a New York City-based healthcare data and technology company, founded in 2017, that combines deep healthcare provider data with agentic AI to power drug development, medical and commercial engagement, care navigation, and provider and network intelligence for life sciences, pharma, health plans, and digital health organizations across the United States. Its developer-facing API is the Ribbon Health API (H1 acquired Ribbon Health), a proprietary REST API served over HTTPS at `https://api.ribbonhealth.com/v1`, authenticated with a bearer API key. It is not FHIR-based.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/h1/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/h1/refs/heads/main/apis.yml)

## Tags

- Healthcare
- United States
- Life Sciences
- Provider Data
- Healthcare API
- Price Transparency
- Eligibility
- Network Intelligence
- Digital Health
- Pharma

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

The Ribbon Health API is a single REST API (OpenAPI 3.1.0, 57 paths, base URL `https://api.ribbonhealth.com/v1`) segmented into the following product families:

### H1 Ribbon Providers API

Provider data and network intelligence keyed by NPI - retrieve and curate healthcare providers along with their specialties, procedures, clinical areas, locations, and insurance affiliations.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Locations API

Healthcare location data - create, read, update, and delete provider locations and manage their associated clinical areas, insurances, and organizations.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Custom Filters API

Create, edit, and delete saved custom filters for providers and locations to scope and reuse queries.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Focus Areas API

Clinical focus-area reference data - browse clinical areas, conditions, and treatments used to describe and match provider expertise.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Price Transparency API

Machine-readable price-transparency data - negotiated rates by carrier, provider (NPI), procedure, and location.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Cost Estimates & Eligibility API

Procedure cost estimates and insurance eligibility - submit eligibility checks and retrieve supported eligibility insurance partners and estimated procedure costs.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Organizations API

Healthcare organization records - retrieve organizations and their details used to group and affiliate providers and locations.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Reference Data API

Shared reference data and custom taxonomies - insurances, specialties, procedures, provider types, location types, languages, TINs, and virtual care platforms.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

### H1 Ribbon Network Analysis API

Network analysis endpoint for assessing provider network composition and adequacy.

- **Human URL:** [https://ribbon.readme.io/reference](https://ribbon.readme.io/reference)
- **Base URL:** `https://api.ribbonhealth.com/v1`
- [OpenAPI](openapi/ribbon-health-api-openapi.json)

## Common Properties

- [Website](https://h1.co/)
- [Developer Portal](https://ribbon.readme.io/)
- [Documentation](https://ribbon.readme.io/docs/welcome-to-the-ribbon-health-api)
- [API Reference](https://ribbon.readme.io/reference)
- [Getting Started](https://ribbon.readme.io/docs/getting-started)
- [Sign Up / Request Demo](https://h1.co/request-demo/)
- [Blog](https://h1.co/blog/)
- [Support](https://h1.co/contact/)
- [Security](https://h1.co/security/)
- [Terms of Service](https://h1.co/terms-of-use/)
- [Privacy Policy](https://h1.co/privacy-policy/)

## Authentication

API key passed as an HTTP Bearer token (OpenAPI `BearerAuth`, applied globally). The API is not FHIR / SMART-on-FHIR. Production keys are gated behind a request-demo / partner sign-up; documentation is fully public.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
