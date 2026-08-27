# Core managed AI SaaS operating model

**Version:** 0.1  
**Date:** 2026-08-26  
**Status:** Sponsor-directed launch model; commercial and vendor assumptions require validation  
**Related:** [Offer and pricing model](../../03-offers-and-products/pricing/offer-and-pricing-model.md), [managed AI product catalogue](../../03-offers-and-products/product-catalog/managed-ai-product-catalog.md), [Markdown client repository operating model](../client-operations-platform/markdown-client-repository-operating-model.md), [agent-operated service platform blueprint](../../11-technology-and-data/architecture/agent-operated-service-platform-blueprint.md)

## Decision

Dirtyworks.ai's repeatable core is **managed AI SaaS operations** for packaged products such as ChatGPT Enterprise and comparable workforce AI tools. Dirtyworks.ai helps the client select, acquire, configure, govern, adopt, support, measure and renew those products.

Custom data, hosted models, production APIs, retrieval systems, bespoke agents, integrations and application operations are valuable expansion services, but they are not required to make the core offer useful. They are separately discovered, designed, priced and contracted.

This boundary creates a simpler operating mechanism:

```text
Packaged AI SaaS selected
        ↓
Tenant, users, policy and support configured
        ↓
Users onboarded, trained and supported
        ↓
Seats, adoption, cost, incidents and renewals managed
        ↓
Monthly operating decision: keep, change, expand or remove
```

## Corrections to the proposed base stack

| Proposed component | Verdict | Precise role and constraint |
|---|---|---|
| Freshdesk | Correct | Client-facing support portal, email intake, tickets, knowledge articles, service communications and response reporting. Freshservice is a different ITSM product; consider it only when asset/change/catalogue depth or an MSP seam requires it. |
| Per-client Markdown repository | Selected in place of Hudu | Private client operating source: contacts, product/tenant records, onboarding, runbooks, responsibilities, renewals, evidence links and procedures. One private Git-backed repository per end customer, with human-reviewed publication and derived interface/graph. It is not authoritative for vendor users, usage, invoices or accounting. See the [Markdown client repository operating model](../client-operations-platform/markdown-client-repository-operating-model.md). |
| Hudu | Optional later platform | Useful if collaboration, granular permissions, read auditing, portal or maintenance needs exceed the Markdown model. It is not required for launch; see the [Hudu alternative](../client-operations-platform/hudu-client-documentation-structure.md). |
| 1Password | Correct | Internal human access and brokered connector credentials. Store references/scoped credentials, never raw secrets in tickets, Markdown prose or model context. Prefer customer-owned admin accounts, least privilege and short-lived tokens where supported. |
| Langfuse, Sentry or Datadog for base cost | Incorrect for ordinary packaged SaaS | Langfuse observes instrumented LLM applications; Sentry observes application failures and performance; Datadog observes broader applications/infrastructure. None is normally the authoritative source for ChatGPT Enterprise seats, native usage or issued invoices. Use them only for advanced workloads they can actually instrument. |

## Core service catalogue

The core is not merely licence access. It is an operating service around the client's product portfolio.

### Select and acquire

- needs and product-fit review;
- approved catalogue and security/commercial screen;
- quote and procurement coordination;
- customer-direct, authorized-resale or approved marketplace path;
- tenant ownership, billing owner, renewal and cancellation record.

### Configure and control

- workspace/tenant setup and administrative baseline;
- roles, groups, approved features and supported-use boundaries;
- joiner, mover and leaver administration;
- access review, offboarding and evidence;
- acceptable-use, privacy/security and escalation baseline, without representing legal advice or certification.

### Enable and support

- administrator and user onboarding;
- role-specific quick starts and practical training;
- Freshdesk portal, knowledge articles and business-hours support;
- office hours and common-use coaching;
- vendor escalation and known-issue communication.

### Measure and improve

- contracted, purchased, assigned and active-seat reconciliation where the vendor exposes those facts;
- native adoption/usage reporting with the vendor's definitions and freshness disclosed;
- support themes, training completion and adoption gaps;
- cost, budget, invoice and renewal review;
- product removal, plan change or expansion recommendations;
- monthly operating report and decision register.

## Base systems and authority

| Operational job | Base system | Authoritative source |
|---|---|---|
| Client requests, incidents and support communications | Freshdesk | Freshdesk ticket and communication record |
| Runbooks, responsibilities, tenant/product metadata and procedures | Private per-client Markdown repository | Published Markdown for Dirtyworks.ai operating procedure; customer/vendor source for underlying facts |
| Privileged credentials and access delegation | 1Password | Customer identity/vendor tenant for entitlement; 1Password for stored credential/reference |
| Users, roles, product configuration and native activity | Each vendor admin console/API/export | Vendor tenant, with source date and vendor definition retained |
| Purchased quantity, charges and payment | Vendor/distributor/accounting records | Issued invoice and accounting record; dashboard estimates are not invoices |
| Cross-vendor product/access/cost view | Controlled register initially; later a ledger only if justified | Reconciled view with source, observation date and estimate/invoice status |
| Customer training | Freshdesk knowledge base plus versioned internal materials | Delivery/completion record and material version |

The register should distinguish five facts that are often confused:

- **contracted:** what the customer agreed to;
- **purchased:** what the vendor or reseller sold;
- **assigned:** what the vendor/identity system allocated;
- **active:** vendor-defined activity over a stated period;
- **billed:** what an issued invoice charged.

An existing SaaS Management Platform may replace much of the controlled register. The current first candidate is 1Password SaaS Manager because it can combine finance transactions, contracts, licences, vendor usage and supported AI consumption, while exposing API/MCP access. Adoption remains gated by quote economics, client isolation and a proven MSP/delegated-administration model. See the [SaaS and AI cost-management platform investigation](../../11-technology-and-data/platform-evaluations/saas-cost-management-platform-investigation.md).

## Cost-control mechanism

Cost control in the base service is a reconciliation and decision process, not an observability dashboard.

1. Record product, plan, billing owner, seller of record, currency, quantity, term, renewal/cancellation dates and budget.
2. Collect native seat/activity exports or admin analytics at the supported cadence.
3. Reconcile purchased, assigned and active quantities without silently treating one as another.
4. Reconcile forecast/analytics against issued invoices and disclose delay or missing data.
5. Flag orphaned accounts, unassigned licences, low adoption, unexpected usage, overage risk and approaching renewal.
6. Create a Freshdesk work item for an approved correction; retain the native change evidence.
7. Report current cost, budget variance, forecast, renewal decision and recommended action monthly.

For advanced applications, add model-call cost, token/usage attribution, cloud infrastructure and application telemetry through the relevant gateway, Langfuse, Sentry, Datadog or cloud-native tools. Keep application estimates separate from issued vendor/cloud invoices.

## Billing choices

A **unified cost statement** is available in every model. A **single unified invoice** is conditional.

| Model | Customer receives | Advantage | Constraint/risk | Default state |
|---|---|---|---|---|
| Customer-direct | Vendor invoices plus one Dirtyworks.ai service invoice and a consolidated cost statement | Lowest working-capital, credit, tax, cancellation and resale risk; preserves customer ownership | More than one payable invoice | Launch default |
| Authorized resale/distribution | Dirtyworks.ai or an authorized channel invoices approved SKUs plus management services | Genuine purchasing convenience and possible margin | Requires product/geography authorization, support obligations, credit, tax and renewal economics | Use only when rights are documented |
| Contract-specific pass-through | Dirtyworks.ai purchases and rebills a defined cost | Can simplify a specific transaction | Dirtyworks.ai carries collection, FX, tax, vendor-change, usage, cancellation and insolvency exposure; may still lack resale rights | Exception requiring approval and protective terms |

Do not call a consolidated report a unified bill. Proposals must state seller of record, invoice path, variable-usage treatment, taxes/currency, overage responsibility, renewal/cancellation dates and what happens when the client does not pay.

## Training model

The base training programme should be deliberately light but repeatable:

- sponsor/admin orientation before launch;
- 45–60 minute role-based user onboarding;
- quick-start guide and supported-use examples;
- short safe-use, privacy and escalation module;
- Freshdesk knowledge articles and request path;
- office hours during stabilization, then scheduled or package-based sessions;
- completion and material-version record;
- adoption/support review that determines whether more training is useful.

A separate learning-management system is not needed until customers require formal assignments, attestations, recurring certification or cohort reporting that Freshdesk and a controlled register cannot support.

## Core monthly operating record

At minimum, report:

- purchased, assigned and active users by product, with definitions;
- additions, role changes, removals and access-review exceptions;
- product and management cost, budget variance and renewal exposure;
- support volume, themes, age, response performance and vendor escalations;
- onboarding/training completion and common knowledge gaps;
- product changes, incidents, risks and open customer decisions;
- adoption trend and agreed business context, without intrusive employee surveillance;
- actions completed, evidence references and next-month priorities.

Useful ratios include assigned/purchased seats, active/assigned users, cost per assigned user, cost per vendor-defined active user, joiner/leaver completion time, orphaned accounts, support requests per managed user and renewal decisions completed before the cancellation deadline. None should be presented as business value by itself.

## Advanced-workload boundary

Move an opportunity into a separately scoped advanced engagement when it includes one or more of:

- customer data ingestion, indexing, retrieval or knowledge pipelines;
- hosted/open models, vector databases or model gateways;
- production API applications, custom agents or system actions;
- bespoke identity, permissions, connectors or data pipelines;
- sensitive/regulated data or higher-impact decisions;
- availability, recovery, performance or application-level service commitments;
- prompt/model evaluation, model-call observability or cloud cost allocation;
- software development, testing, deployment and ongoing application maintenance.

Commercially, use a paid discovery/design step, a project with explicit acceptance criteria, and a higher recurring operations fee. Do not absorb this work into a per-user SaaS-management package.

## Agent-operated interface

The agent is a command surface over the systems above, not a new source of truth.

Early capabilities should be:

1. answer sourced questions about tickets, runbooks, products, access, costs and renewals;
2. draft work cards and client responses;
3. create Freshdesk requests with customer/operator approval;
4. produce onboarding/offboarding checklists and monthly report drafts;
5. never receive raw secrets or execute privileged vendor changes directly.

Later vendor actions require a typed connector, tenant/actor authorization, preview, approval, idempotency, read-after-write verification, audit and a truthful human-task fallback.

## Launch options and constraints

### Option A — operations-first base

Configure Freshdesk, one private Markdown repository per client, 1Password and a controlled register. Use personal-wiki for governed publication, optionally use a client-local kgmd graph for read/search, and use native vendor administration plus manual/CSV/API collection according to each product's capability. This best tests demand and service economics within the current founder/budget limits.

Use the [pre-launch readiness checklist](../../01-governance/planning/pre-launch-readiness-checklist.md), [pre-customer acceptance checklist](../customer-acceptance/pre-customer-acceptance-checklist.md) and [first-customer onboarding checklist](../onboarding/first-customer-onboarding-checklist.md) as the operating gates for this option.

### Option B — add ITSM/PSA depth

Use Freshservice, Halo, SuperOps or the partner's PSA when a real account requires change/assets/contracts/time/SLA/billing integration beyond Freshdesk. This adds structure but also implementation and reconciliation burden.

### Option C — build the control layer

Add the AI Operations Ledger and client self-service only after repeated workflow, multi-operator/partner needs, measured manual burden or funded demand meets the documented activation gate.

These options are sequentially compatible. Selecting the base does not prevent later platform depth.

## Validation and open decisions

Before publishing final packages or buying annual contracts, test:

- whether buyers value managed administration/training/support enough to pay separately from licences;
- which two or three AI SaaS products create repeatable admin and reporting work;
- available admin, identity, activity and invoice exports by vendor/plan;
- customer-direct versus authorized-resale preference;
- whether the MSP opportunity requires work inside its PSA;
- required support window, onboarding cadence and managed-user definition;
- whether Freshdesk Growth is sufficient or Pro portal/reporting features are needed;
- how customer approval and evidence will work for access changes.

There is no execution blocker. Commercial rights, vendor/plan admin capabilities and the live MSP system seam remain explicit validation gates rather than reasons to build a universal platform now.

## Current primary-source checks

- Freshdesk currently describes ticketing, shared inbox, customer portal, knowledge base, analytics and roles/permissions in its helpdesk plans: <https://www.freshworks.com/freshdesk/pricing/>
- Freshservice is positioned as IT service management with employee onboarding, incidents and asset lifecycle rather than the same product as Freshdesk: <https://www.freshworks.com/freshservice/>
- ChatGPT Enterprise workspace settings expose members, seat types, roles, groups, feature access, analytics, identity and billing controls: <https://help.openai.com/en/articles/8411955-what-security-settings-can-i-control-for-my-workspace>
- ChatGPT Enterprise workspace analytics exposes seats purchased/enabled, active users and per-user usage exports with vendor-specific definitions: <https://help.openai.com/en/articles/10875114>
- ChatGPT Enterprise billing exposes usage limits, reports and issued invoices; the documentation warns that analytics/report data may have a freshness delay and should be reconciled to invoice periods and contracted terms: <https://help.openai.com/en/articles/20001001>
