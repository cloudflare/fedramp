# Cloudflare FedRAMP

This repository is the authoritative, machine-readable, version-controlled source of truth for the **Cloudflare for Government** FedRAMP Marketplace listing.

- **FedRAMP Package ID**: [`FR2000863987A`](https://www.fedramp.gov/marketplace/products/FR2000863987A/)
- **Certifications**: FedRAMP Class C and FedRAMP Class D (Rev5) *(previously FedRAMP Moderate and High authorizations)*
- **Provider**: Cloudflare, Inc. (UEI `JV9YXS9MLA48`)
- **Assessor**: Schellman Compliance, LLC
- **Service Model**: SaaS + PaaS
- **Deployment Model**: Public Cloud

## What's in this repository

| File | Purpose |
|---|---|
| [`cloudflare-for-government.json`](./cloudflare-for-government.json) | Certification Package Overview conforming to the FedRAMP 2026 [`certification-package-overview`](https://www.fedramp.gov/schemas/fedramp-certification-package-overview-schema-2026-06-24.json) schema. Enumerates the 56 in-scope services with per-Certification-class notation. |
| [`LICENSE`](./LICENSE) | License terms. |
| [`SECURITY.md`](./SECURITY.md) | How to report a security vulnerability. |
| [`CONTRIBUTING.md`](./CONTRIBUTING.md) | How Cloudflare maintains this file. |

## Per-service Certification-class notation

Following the [Google Services FedRAMP listing pattern](https://www.fedramp.gov/marketplace/products/FR1805751477/), per-service Certification class is denoted by symbol suffix on `serviceName`:

| Symbol | Meaning | Count |
|---|---|---|
| (none) | Certified at both Class C and Class D | 50 |
| `*` | Certified at Class C only | 4 |
| `†` | Certified at Class D only | 2 |

The full legend is included in the JSON's top-level `serviceDescription` field.

## Access environments

The two Certifications are delivered from separate environments with separate control planes:

| Certification | Dashboard | API |
|---|---|---|
| Class C | `dash.cloudflare.com` | `api.cloudflare.com` |
| Class D | `dash.fed.cloudflare.com` | `api.fed.cloudflare.com` |

Federal customers select the environment that matches the FedRAMP Certification required for their workload.

## How this repository is maintained

Content changes originate in Cloudflare's internal source-of-truth repository (Cloudflare-only) and are mirrored here on merge to `main`. This repository accepts issues for questions, but code changes should follow the process below.

1. A Cloudflare employee (typically GRC) files an internal Jira ticket describing the change.
2. Change is drafted in the internal source-of-truth repo via merge request.
3. The updated JSON is re-validated against the FedRAMP schema before merge.
4. Merge triggers a mirror job that updates this repository.
5. The updated JSON is re-submitted to the FedRAMP PMO via the [2026 intake form](https://help.fedramp.gov/hc/en-us/requests/new?ticket_form_id=50939227168027).

## Validation

The JSON validates against `fedramp-certification-package-overview-schema-2026-06-24.json` and its referenced common definitions. You can verify locally with any Draft 2020-12 JSON Schema validator, or paste into the [FedRAMP official validator](https://www.fedramp.gov/schemas/validator/?schema=fedramp-certification-package-overview-schema-2026-06-24.json).

## Questions

- **General questions about Cloudflare's FedRAMP posture**: [`fedramp-team@cloudflare.com`](mailto:fedramp-team@cloudflare.com)
- **Federal sales inquiries**: [`publicsector@cloudflare.com`](mailto:publicsector@cloudflare.com)
- **Vulnerability reporting**: see [`SECURITY.md`](./SECURITY.md)
- **Issue with the listing content**: [open an issue](../../issues) and tag `@cloudflare/fedramp`
