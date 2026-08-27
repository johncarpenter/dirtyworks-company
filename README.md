# Functional company repository template

**Repository role:** authoritative company knowledge and operating system  
**Status:** Empty candidate shell  
**Excludes:** application code, tool codebases, client-specific records, secrets and restricted source records

This repository is organized by stable company function. Document type, status, authority and sensitivity belong in document metadata rather than in the folder path.

## Structure

```text
company/
├── README.md
├── _system/
│   ├── documentation-policy.md
│   ├── document-template.md
│   ├── systems-and-repositories-register.md
│   └── registers/
├── 01-governance/
│   ├── company/
│   ├── planning/
│   ├── board-and-investors/
│   └── policies/
├── 02-strategy-and-research/
│   ├── company-strategy/
│   ├── business-model/
│   ├── market/
│   ├── segments/
│   ├── channels/
│   ├── competitive-intelligence/
│   ├── experiments/
│   └── roadmaps/
├── 03-offers-and-products/
│   ├── portfolio/
│   ├── service-packages/
│   ├── pricing/
│   ├── product-strategy/
│   └── product-catalog/
├── 04-marketing-and-brand/
│   ├── brand/
│   ├── design-system/
│   ├── messaging/
│   ├── website/
│   ├── campaigns/
│   ├── content/
│   └── events/
├── 05-sales-and-partnerships/
├── 06-client-delivery/
├── 07-company-operations/
├── 08-finance/
├── 09-legal-risk-and-compliance/
├── 10-people/
├── 11-technology-and-data/
├── 80-initiatives/
├── 90-templates/
├── 95-reference/
└── 99-archive/
```

## Boundary with other repositories

- This repository records why an application or tool exists, who owns it, its business constraints and its current status.
- Each application or material tool owns its implementation, tests, deployment, architecture and release history in a separate repository.
- This repository owns the brand strategy and reusable design system. Applications consume a released or explicitly vendored design-system version and own their application-specific implementation.
- Client-specific records belong in the client repository. This repository may contain aggregated, sanitized company measures but not client source data.
- Passwords, tokens and recovery material belong in a secrets manager. Restricted personnel, tax, banking and executed legal source records belong in approved record systems.

## Navigation

Each numbered area contains a local README defining its scope. `_system/` governs the repository itself. `80-initiatives/` contains temporary initiative coordination, while durable outputs move to the functional area that owns them.

