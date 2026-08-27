# Client product configurator — application specification

**Version:** 0.1  
**Date:** 2026-08-25  
**Status:** Workbook MVP implemented; software application deferred pending workflow evidence

## Product intent

Turn a client request such as “3 ChatGPT Business seats, 4 Midjourney Pro seats, and a monthly OpenRouter budget” into a controlled product mix, deployable scope, and auditable estimate.

The product is a **portfolio composer and operating quote**, not a checkout cart. It must surface prerequisites, commercial pathway, customer ownership, risk, deployment work, recurring management, usage uncertainty, and unresolved approval items before order.

## Users and jobs

| User | Job |
|---|---|
| Prospect / client sponsor | Compare approved choices, quantities, commitments, and full operating cost |
| Dirtyworks.ai seller | Create a clear estimate without implying unverified resale rights |
| Solutions / delivery lead | Identify prerequisites, data/integration risk, work, runbook, and support tier |
| Finance / operations | Separate vendor pass-through or customer-direct estimates from Dirtyworks.ai revenue and margin |
| MSP partner | Compose a portfolio while preserving seller-of-record, support, ownership, and white-label responsibilities |

## MVP now: spreadsheet

The workbook at `documents/business-plan/dirtyworks-ai-client-product-configurator.xlsx` is the working prototype. It contains:

- `Start Here` — purpose, workflow, ownership rules, and warnings;
- `Client Quote` — editable client details and client-facing totals;
- `Configuration` — selectable product IDs, quantities or usage budgets, price overrides, management tiers, and formula outputs;
- `Catalog` — candidate products, commercial posture, public price assumptions, sources, prerequisites, and approval notes;
- `Fee Schedule` — editable Register/Manage/Operate hypotheses;
- `Sources` — source register and quote-time verification rules; and
- `Checks` — formula and readiness checks.

Yellow/blue input cells are editable. Calculated cells are protected by convention rather than workbook password. The workbook is an estimating tool, not an order form or vendor price book.

## Core domain model

```text
Client
  └── Portfolio Version
        ├── Product Selection
        │     ├── Product / SKU
        │     ├── quantity or usage estimate
        │     ├── price snapshot and currency
        │     ├── commercial pathway
        │     ├── management tier
        │     └── prerequisite / approval state
        ├── One-time Service Line
        ├── Responsibility Schedule
        ├── Approval
        └── Quote / Order Export

Product
  ├── Vendor and product family
  ├── plan / SKU / billing basis / commitment
  ├── public-price snapshot and effective date
  ├── allowed commercial pathways
  ├── admin and identity capabilities
  ├── data / integration risk fields
  ├── deployment and offboarding runbook
  └── support / approval state
```

Price must be versioned. A quote must retain the exact price snapshot, FX assumption, fee schedule, terms, and catalogue version used even after the live catalogue changes.

## Required application workflow

1. Create client and choose direct, MSP co-managed, or white-label sales context.
2. Capture workforce size, existing Microsoft/Google/cloud estate, data classes, identity provider, regions, use cases, and support expectation.
3. Browse the client-friendly `WORK / FIND / MAKE / BUILD / MOVE / HOLD / WATCH` menu.
4. Add product/plan and quantity or monthly usage estimate.
5. Show prerequisites, product overlap, minimum seats, commitment, customer-direct versus authorized resale status, and required management tier.
6. Calculate vendor estimate, Dirtyworks.ai one-time work, monthly management, first-month total, and annualized run rate.
7. Route conditional or custom products for commercial and technical approval.
8. Generate three views from the same versioned record:
   - client proposal with assumptions and exclusions;
   - deployment bill of materials and responsibility schedule; and
   - internal revenue, cost, margin, cash-exposure, and renewal view.
9. Convert an accepted quote into implementation tasks and an account/product register.
10. Reconcile licences, usage, access, value, and renewal dates during operation.

## Business rules

- The client owns its tenant, data, billing account, and administrative recovery path by default.
- `CUST-DIRECT` items appear as estimated third-party charges, not Dirtyworks.ai invoice revenue.
- `AUTH-RESELL` cannot be selected unless the vendor, SKU, geography, term, seller-of-record, price book, support duty, and authorization evidence are current.
- Annual contracts must show monthly equivalent and actual vendor payment timing.
- Usage products require a budget, warning threshold, approver, and hard-limit policy where supported.
- Minimum quantity and product prerequisites generate blocking warnings.
- A user can override price or management tier only with a reason and approver.
- Every product must have an owner, renewal/cancellation date, admin method, support route, and offboarding procedure before deployment is complete.
- Products that can access sensitive, regulated, employment, financial, or safety-related data require the corresponding review; catalogue inclusion is not approval for a use case.
- Shared user accounts are prohibited.

## Pricing engine

The software should preserve multiple pricing policies rather than encode one permanent answer:

```text
vendor_estimate = quantity_or_budget × unit_price × fx × commercial_adjustment
one_time_service = tier_setup + per_unit_onboarding + scoped_services
monthly_management = tier_platform_fee + per_unit_admin + managed_usage_or_change_fee
client_monthly_estimate = vendor_estimate + monthly_management
first_month_estimate = client_monthly_estimate + one_time_service
```

Policy alternatives to support:

- transparent per-platform plus per-user management;
- predefined portfolio bundles with tool/user/change limits;
- authorized resale with contract-specific discount/margin and pass-through cost;
- MSP wholesale or white-label fee schedule; and
- negotiated enterprise/custom platform pricing.

The internal view must distinguish booked revenue, vendor cost, gross margin, taxes, working-capital exposure, customer-direct estimated spend, and consumption contingency.

## Catalogue governance

Each product should pass these gates before it is marked standard:

| Gate | Required evidence |
|---|---|
| Commercial | price source/effective date; seller and billing path; resale/partner evidence; tax and cancellation treatment |
| Administration | organization controls; roles; identity/SSO; joiner/mover/leaver; audit availability; recovery method |
| Data and security | service terms; training use; retention; region/residency; subprocessors; encryption; export/deletion |
| Delivery | prerequisites; deployment checklist; configuration baseline; test and acceptance criteria; training |
| Operations | support route; health/cost signals; incident process; change cadence; service limits |
| Exit | licence removal; data/artifact export; credential/access revocation; account transfer or deletion |
| Economics | measured deployment time; steady-state support; minimum fee; target margin |

Catalogue states: `Candidate`, `Conditional`, `Standard`, `Suspended`, and `Retired`. Product facts should include source, capture date, reviewer, next review, and confidence.

## Integrations worth considering later

- Vendor/distributor catalogues for authorized SKUs and renewal data.
- CRM for client, opportunity, proposal, and approval state.
- Accounting/PSA for approved service lines, invoice ownership, and margin.
- Identity providers for user reconciliation.
- Cloud billing APIs for consumption and budgets.
- Service desk for product-specific triage and SLA routing.
- E-signature/order forms and a client portal.

No integration should be built until its system of record, permissions, error handling, and reconciliation owner are established.

## Build options

| Option | Strength | Constraint | Appropriate trigger |
|---|---|---|---|
| Keep the spreadsheet | Fast, inspectable, cheap, easy to change | Weak concurrency, approval, versioning, and catalogue maintenance | Discovery and first 3–5 real quotes |
| Low-code internal app | Better forms, workflow, and permissions | Platform dependency and eventual complexity ceiling | Repeated quoting by 2+ internal users or MSP partners |
| Custom web application | Exact workflow, portal potential, multi-tenant integration | Highest build/security/maintenance cost | 10+ quotes, 3+ deployed portfolios, and stable repeated requirements |
| Configure an existing PSA/CPQ | Mature quoting, contracts, renewals, and finance integration | AI catalogue logic and client experience may require adaptation | When a PSA/CRM is already the operating system |

The choice is deliberately unmade. The spreadsheet is sufficient to learn which fields, rules, and exceptions are real.

## Application acceptance criteria

- A seller can create and version a mixed portfolio without manual arithmetic.
- Client-facing output separates vendor estimates from Dirtyworks.ai fees.
- Minimum seats, prerequisites, volatile prices, and unauthorized resale states cannot disappear from the approval view.
- Direct, resale, cloud-marketplace, and managed-deployment items are represented without accounting ambiguity.
- A delivery lead receives the selected products, owners, quantities, prerequisites, tier, and acceptance work.
- A renewal review can reconcile contracted, assigned, active, and valuable products.
- Every material override is attributable and preserved in the quote version.
- The system can export the customer’s catalogue and access inventory at offboarding.

## Activation gate for software development

Do not replace the workbook because a web interface would look better. Start application implementation when at least three of these are true:

- five real quotes expose a stable shared schema;
- three client portfolios require ongoing reconciliation;
- two people or one MSP partner need concurrent access;
- manual price/term review creates a measurable quoting error or delay;
- a signed opportunity requires a client-facing interactive composer; or
- a PSA/CRM integration will remove repeated double entry with a named owner.

Before that gate, improve the catalogue, runbooks, and commercial evidence rather than hardening speculative workflow.

