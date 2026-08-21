# Contributing

Thanks for looking at this repository. Contributions are limited by design.

## What kind of contributions are accepted

**Issues** — welcome. If you spot a mismatch between the content here and the [FedRAMP Marketplace listing](https://www.fedramp.gov/marketplace/products/FR2000863987A/), or the internal service scope has drifted, open an issue and we'll investigate. Tag `@cloudflare/fedramp` in your issue for routing.

**Pull requests** — this repository is a mirror of Cloudflare's internal source-of-truth for the FedRAMP listing. Content changes must originate in Cloudflare's internal Jira/GitLab workflow so that the FedRAMP-scoped change-management controls (CCF-CM-022 / 023 / 024 / 260) are honoured. External PRs cannot be merged directly; if you have a suggested edit, please file an issue with the proposed diff and we'll take it into the internal workflow.

## Editorial standards

If you're a Cloudflare employee proposing an edit through the internal source-of-truth workflow, please:

1. Update the JSON in the internal repository and re-validate against the [FedRAMP 2026 certification-package-overview schema](https://www.fedramp.gov/schemas/fedramp-certification-package-overview-schema-2026-06-24.json).
2. Confirm the change is consistent with the current authorized boundary (internal `Security-Privacy-AI-Certifications - Product Scope` page).
3. Link the FedRAMP intake ticket (or note that one will be filed after merge).
4. Get GRC review on the internal merge request.

## Contact

- **FedRAMP posture / controls questions**: `fedramp-team@cloudflare.com`
- **Federal sales**: `publicsector@cloudflare.com`
- **Security disclosures**: see [`SECURITY.md`](./SECURITY.md)
