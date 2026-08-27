# SaaS and AI cost-management platform investigation

**Version:** 0.1  
**Date:** 2026-08-26  
**Status:** Working buy/configure/build decision; vendor demonstrations and quotes required  
**Scope:** How Dirtyworks.ai can collect, normalize, reconcile and manage cost and usage across many customer-owned AI and SaaS products

## Executive finding

Systems already exist for this problem. The market category is usually called **SaaS Management Platform (SMP)**, **SaaS spend management**, or **software asset management**. The strongest products combine four incomplete views:

```text
Vendor admin/API             users, licences, product activity and consumption
Identity/SSO                 people, groups, access and login signals
Contracts + accounting/AP    commitments, invoices, booked spend and payment state
Cards/bank transactions      shadow purchases and settled cash movements
                  ↓
SaaS management platform     app/vendor mapping, reconciliation, utilization,
                             budgets, renewals and optimization workflows
                  ↓
Dirtyworks operating layer   client decisions, tickets, evidence and monthly reporting
```

No single input is sufficient. A transaction proves that money moved, not what was purchased or used. An invoice proves a charge, not adoption. SSO proves an authentication event, not useful activity or invoice cost. A vendor API provides the best product-specific usage, but only for that vendor and only where the customer's plan exposes it.

The current best first candidate is **1Password SaaS Manager**, formerly Trelica. It is unusually aligned with the selected 1Password access layer and already provides finance-system transaction mapping, contracts/renewals, direct application usage integrations, licence optimization, API access and an MCP interface. Its AI Spend and Consumption capability currently supports OpenAI Platform, ChatGPT Enterprise, Anthropic/Claude, Cursor and Amazon Bedrock.

Dirtyworks.ai should test this product before building an aggregation system. The custom opportunity is more likely to be a multi-client managed-service overlay—responsibility, source authority, customer decisions, service tickets, evidence and reports—than another generic transaction mapper.

## The data model Dirtyworks actually needs

For each client, product and reporting period, preserve separate facts:

| Fact | Meaning | Preferred authority |
|---|---|---|
| Contracted | Customer commitment, rate, term and notice requirement | Signed contract/order |
| Purchased | Product/SKU and quantity acquired | Vendor, distributor or marketplace record |
| Assigned | Seats/roles allocated to identities | Vendor tenant or identity system |
| Active | Product-specific activity over a stated period | Vendor usage API/export; definition retained |
| Consumed | Tokens, credits, calls, compute or other usage units | Vendor usage API/export |
| Estimated cost | Usage multiplied by a documented rate before billing | Vendor/SMP calculation with timestamp and rate version |
| Invoiced | Amount the seller of record charged for a defined period | Issued invoice/accounting/AP record |
| Paid | Settled cash or card transaction | Accounting/bank/card record |
| Valuable | Business outcome under the client's agreed method | Customer decision and evidence |

The system must never collapse these into one cost value. Timing, currency, tax, credits, refunds, minimum commitments, annual prepayment and vendor adjustments make the numbers legitimately different.

## Existing-system shortlist

### 1. 1Password SaaS Manager — first demonstration

**Mechanism**

- Discovers applications through identity providers, finance systems, direct application integrations and browser signals.
- Imports transactions from systems including QuickBooks, Xero, NetSuite, Expensify, Ramp, Brex, Sage Intacct and other finance/procurement systems.
- Maps transactions to applications and supports manual mapping/splitting where a vendor bundle is ambiguous.
- Stores contracts, entitlements, renewal dates and licence costs.
- Compares licence availability/assignment with app engagement where an integration exposes it.
- Provides AI consumption, budgets, burn-rate alerts and breakdowns by supported dimensions for OpenAI/ChatGPT Enterprise, Anthropic/Claude, Cursor and Bedrock.
- Exposes a REST API and an MCP server; the remote MCP mode is read-only.

**Fit for Dirtyworks.ai**

- Strong functional overlap with the core cost, access and renewal service.
- Reduces the number of vendors because 1Password is already the proposed privileged-access layer.
- An agent can query normalized data without Dirtyworks building every read connector immediately.
- Customer-owned instances would preserve client ownership and offboarding.

**Constraints to verify**

- Pricing is quote-only and may be designed for larger enterprises rather than 20–150-person SMBs.
- The public 1Password MSP documentation establishes multi-client management for Enterprise Password Manager; it does not clearly establish the same MSP console/wholesale model for SaaS Manager.
- Each client may require a separate SaaS Manager organization, finance connection and vendor authorization.
- AI coverage is still a limited and changing vendor set. Ordinary SaaS activity depends on each direct integration's available data.
- Vendor-derived AI cost remains part of a broader budget-monitoring process; issued invoices still require reconciliation.
- User/team-level reporting raises proportionality, employee-monitoring, contract and privacy questions.

**Commercial action:** request an SMB and MSP/service-provider quote, a trial, a Canadian data/subprocessor explanation, and a demonstration using one synthetic client plus one second isolated client.

### 2. CloudEagle.ai — broad enterprise comparator

CloudEagle describes a platform that combines SSO, finance, HRIS, contracts, browser/network discovery and direct SaaS integrations. Its core jobs include application discovery, spend, contracts, licences, renewals, procurement and optimization.

**Reason to demonstrate:** useful benchmark for how completely an enterprise SMP correlates finance and application signals.

**Constraints:** public material is demo-led rather than transparent SMB pricing; MSP multi-client operation, Canadian data posture, service-provider rights and cost at small account sizes must be proven.

### 3. Zylo — enterprise system-of-record comparator

Zylo combines user, usage, financial, contract and security data, supports direct integrations and file-based usage ingestion, and exposes an API and MCP connection.

**Reason to demonstrate:** strong reference model for normalized SaaS/AI data and agent access.

**Constraints:** enterprise positioning and quote-led economics may not fit early SMB accounts; the MSP operating model must be demonstrated rather than inferred from a partner programme.

### Other credible products

Torii, Zluri, BetterCloud and similar SMP/access-governance products may also fit. Spend/procurement products such as Cledara, Ramp, Brex, Vendr and Spendflo solve narrower purchasing, card, invoice or renewal jobs. They should enter the shortlist only when a customer's existing finance stack or an MSP partner makes the integration materially easier.

## CloudEagle comparison-list triage

CloudEagle's comparison pages are vendor marketing, not independent evaluations. The compared products also serve different primary buyers and should not be scored as though they all solve the same cost problem.

| Platform | Primary job supported by current vendor material | SaaS invoice/spend | Seat/app utilization | Model/token/credit consumption | Public commercial signal | Dirtyworks fit |
|---|---|---|---|---|---|---|
| **CloudEagle.ai** | SaaS management, procurement, identity and AI governance | Strong | Strong | **Explicit:** Claude, ChatGPT/OpenAI API, Cursor, Copilot and Gemini are named; token/credit/license cost is described | CloudEagle's current pricing article states SaaS Management starts at USD $2,500/month; orders/terms apply | Functionally strong comparator; likely uneconomic as a dedicated base platform for each early SMB unless an MSP/portfolio licence exists |
| **Zylo** | Enterprise SaaS/AI system of record and optimization | Strong | Strong | **Explicit:** OpenAI API, Anthropic API, Vertex, Snowflake and Databricks consumption drivers are named | Demo/quote-led; vendor's own index describes portfolios with median annual SaaS spend above $20M | Strong technical comparator; apparent enterprise economics and operating maturity exceed the initial ICP |
| **Productiv** | SaaS intelligence, engagement, spend, contracts and procurement | Strong | Strong, including feature-level engagement for supported apps | **Not established as token-level:** current material describes AI adoption, app behavior and shadow AI | Demo/quote-led | Useful for detailed app engagement; full value requires SSO, engagement connectors, contracts, org data and financial discovery |
| **BetterCloud** | SaaS operations, lifecycle automation and spend optimization | Strong within Spend Optimization | Strong via browser, SSO and direct integrations | **Not established as vendor consumption:** its own AI credits price BetterCloud features, not customer model spend | Custom quote based on licences, connected apps, modules/add-ons; Spend Optimization fees may be based on spend under management | Useful if lifecycle automation is equally important; not the first AI-consumption choice |
| **Zluri** | SaaS management plus identity/access governance | Strong | Strong for supported integrations | **Not established as token-level** in reviewed official material | Demo/quote-led | Possible access/lifecycle alternative; demonstrate only if its finance/identity connectors match the first client |
| **Lumos** | Autonomous identity governance, access requests and licence reclamation | Partial | Strong for access, last-login and inactive licences | No evidence of model/token cost tracking | Demo/quote-led; ROI material is framed around approximately 1,000 employees | Better identity/access alternative than cost platform; oversized for core cost-only use |
| **Vendr** | Procurement, contract analysis, price benchmarking and negotiation | Strong for contracts/ERP spend | Weak; usage may be gathered for renewal context rather than continuously measured | No | Vendor support lists Premium Intelligence at USD $35K–$95K/year | Potential later negotiation service/benchmark input; not an operations or AI-usage system |
| **Flexera One** | Enterprise ITAM, SaaS management, FinOps and AI cost management | Strong | Strong across SaaS/cloud/on-prem | **Explicit:** tokens, credits, models, agents, data platforms and infrastructure | Custom/demo-led enterprise platform | Technically most comprehensive; operationally and commercially disproportionate for the launch ICP unless an enterprise/MSP anchor funds it |
| **ServiceNow SAM** | Enterprise software asset management on the Now Platform | Strong | Strong for connected SaaS/SSO/publisher packs | Partial/adjacent through cloud/AI cost products; not the simplest cross-vendor AI-consumption route | Custom quote; requires SAM/SaaS plugins, integrations and sometimes collectors | Not a launch choice. It uniquely documents service-provider domain separation and could fit a large MSP/anchor already standardized on ServiceNow |
| **Nudge Security** | SaaS/AI discovery, security posture and shadow-spend discovery | Moderate: discovers invoice/receipt data from email, plus manual data | Strong for accounts, logins and adoption | No model/token cost; AI means discovery, activity and security governance | USD $750/month billed annually for up to 150 users | Most accessible transparent comparator for discovery/security, but CAD-equivalent cost is still material per SMB and it does not replace native AI consumption feeds |
| **Reco** | SaaS/AI/agent security, posture, permissions and threat detection | No meaningful cost-management evidence | Activity/security rather than financial utilization | Tracks security activity involving tokens/agents, not model-consumption cost | Demo/quote-led | Advanced security add-on, not cost platform |
| **Veza** | Authorization graph, identity security and access governance | No | Access/permission analysis | No | Demo/quote-led | Not relevant to the core cost requirement |
| **ConductorOne** | Identity governance, access reviews and lifecycle | No | Access/permission analysis | No | Demo/quote-led | Not relevant to the core cost requirement |

### Shortlist after triage

1. **1Password SaaS Manager** — first test because it combines the required functions, matches the privileged-access stack, documents current AI-consumption connectors and exposes API/MCP access.
2. **CloudEagle.ai** — best direct feature comparator for both ordinary SaaS spend/utilization and explicit token/credit usage.
3. **Zylo** — best enterprise data-model and consumption-management comparator.
4. **Nudge Security** — optional lightweight deployment/security comparator, not a token-cost comparator.
5. **ServiceNow SAM** — retain only for a large MSP/anchor already committed to ServiceNow and able to fund implementation.

Flexera is technically credible but should not consume validation time unless Dirtyworks moves upmarket into complex hybrid IT/cloud/AI estates. Productiv, BetterCloud, Zluri and Lumos should be pulled into a live opportunity only when their engagement, lifecycle or identity strengths are part of the customer's problem. Vendr, Reco, Veza and ConductorOne are not substitutes for the cost platform.

## Cost and integration reality

The suspicion that these products are expensive is supported by the available commercial signals:

- CloudEagle currently describes SaaS Management as starting at USD $2,500/month—before treating it as a multi-client Dirtyworks cost.
- Nudge Security publishes USD $750/month billed annually for organizations up to 150 users.
- Vendr publishes USD $35,000–$95,000/year for Premium Intelligence, although that product solves procurement rather than continuous usage.
- BetterCloud, Flexera, ServiceNow, 1Password SaaS Manager, Zylo, Productiv, Zluri and Lumos use custom/demo-led pricing in the material reviewed.

Even when implementation is advertised as fast, complete value normally requires several data paths:

| Data path | Why it is needed | Customer work/risk |
|---|---|---|
| Microsoft Entra/Google/Okta | people, groups, SSO app discovery and lifecycle | Directory read scopes, service account, group cleanup and role mapping |
| QuickBooks/Xero/ERP/AP/card | invoices, expenses, vendors and payment context | Financial read scope, GL/category selection, duplicate imports and vendor mapping |
| Contracts/CLM/shared drive | commitment, price, renewal and notice dates | Document collection, extraction review and ownership decisions |
| Direct SaaS admin connector | assigned licences and deeper vendor-defined activity | Admin/API credentials, plan-specific API availability and connector maintenance |
| AI consumption connector | tokens, credits, models, keys and cost estimates | Organization/admin keys, attribution limits, delayed data and invoice reconciliation |
| HRIS | joiner/mover/leaver and team/cost centre | Personal data, authoritative-field mapping and lifecycle quality |
| Browser/email discovery | shadow tools, activity or emailed invoices | Employee-monitoring/privacy review, extension deployment or mailbox authorization |

This is not necessarily difficult software integration—the vendors provide connectors—but it is meaningful onboarding and governance work for every client. Dirtyworks must price that work, minimize connected data and retain a manual/export fallback.

### Dirtyworks planning effort bands

These are internal planning ranges, not vendor implementation promises:

| Deployment depth | Typical scope | Initial effort per client | Ongoing implication |
|---|---|---:|---|
| Discovery | One IdP or email discovery plus contract/spend import | 1–3 operator days | Mapping review and monthly exception cleanup |
| Cost control | Finance/AP, contracts, identity and two or three direct AI/SaaS connectors | 1–3 weeks | Connector health, invoice reconciliation, renewals and vendor-definition changes |
| Full lifecycle | HRIS, browser discovery, many app connectors, provisioning/reclamation and write workflows | 4–12+ weeks | Privileged access, approval, audit, change testing and continuous connector maintenance |

Actual effort depends more on customer data quality, authorization and product-plan API support than on connector installation. A vendor's “minutes to connect” claim describes technical authorization, not a reconciled operating system.

## Three ingestion approaches

### Approach A — vendor and SaaS-management side

Connect the client's identity provider, finance system and important SaaS vendors to an SMP.

**Best information:** users, entitlements, vendor-defined activity, consumption, contracts, invoices/transactions and renewals in one operating view.

**Advantages:** purpose-built mapping and optimization; no new financial-data product to build; direct app usage can support seat reclamation.

**Constraints:** connector coverage and depth vary; pricing and minimum account sizes may be poor for SMBs; multi-client administration may be weak.

**Current fit:** preferred first route if the 1Password SaaS Manager quote and MSP/client-isolation model are workable.

### Approach B — accounting/AP-first

Read software-related accounts, vendors, bills, expenses and payments from the client's existing QuickBooks, Xero or other accounting/AP system. Attach contracts and vendor-native usage separately.

**Best information:** booked/invoiced spend, vendor identity, tax/currency, cost centre and payment status.

**Advantages:** finance has already approved and reconciled much of the data; less sensitive and ambiguous than raw access to every bank account; preserves invoice context better than a bank feed.

**Constraints:** accounting descriptions can still be ambiguous; annual/prepaid charges need period allocation; one vendor may cover many products; it does not show seats or meaningful use.

**Current fit:** best lightweight fallback. Start with CSV/export if clients will not authorize a live integration.

### Approach C — bank/card transaction side using Plaid

The customer uses Plaid Link to authorize a Dirtyworks application to receive bank or card transaction data. Plaid Transactions can return merchant/category information and identify recurring streams for supported institutions.

**Best information:** settled payments and discovery of recurring or previously unknown charges.

**Advantages:** common normalized feed across many institutions; useful for shadow-spend discovery when accounting/AP data is incomplete; Plaid supports US and Canadian institutions and recurring transaction data.

**Constraints:**

- a payment is not an invoice, contract, SKU, seat count, usage record or service period;
- merchant descriptors may be missing or ambiguous, and a vendor charge may bundle products;
- pending transactions change or disappear; even posted records can later be modified/refunded;
- customers must authorize highly sensitive bank/card access to Dirtyworks.ai;
- Dirtyworks would become responsible for financial-data connection security, consent, retention, support and deletion;
- coverage and available fields vary by institution;
- Plaid adds product/API cost while duplicating data that may already be present in QuickBooks, Xero or an SMP finance connector.

**Current fit:** reconciliation and shadow-spend input only—not the primary cost system. Do not build this first unless real customers lack usable finance feeds and explicitly prefer bank linking.

## Recommended source hierarchy

Use source authority by question:

1. **What did we agree to?** Contract/order.
2. **What did the seller charge?** Issued invoice/AP record.
3. **What was paid?** Accounting payment, then bank/card transaction as confirmation.
4. **Who has access?** Vendor tenant/identity provider.
5. **Who used it?** Vendor-native usage, with its definition and period.
6. **What is the current variable-cost estimate?** Vendor usage/cost API or SMP calculation.
7. **What should change?** Dirtyworks recommendation plus customer approval—not an automated metric alone.

This makes cost management a reconciliation process rather than an attempt to choose one universal source of truth.

## Buy, configure or build

### Option 1 — buy the SMP and operate it

Use a customer-owned 1Password SaaS Manager organization per client if commercial and delegated-admin terms work. Dirtyworks uses Freshdesk for customer work and one private [Markdown client repository](../../06-client-delivery/client-operations-platform/markdown-client-repository-operating-model.md) per client for its runbooks and reconciled operating record.

**Buy when:** quote economics fit the service price; supported products cover most client spend; client separation/delegated administration is safe; export/API access is sufficient.

### Option 2 — lightweight Dirtyworks cost register

Use accounting CSV/API data, vendor-native exports/APIs and contract records. Normalize only the minimum facts into a client-separated register and produce the monthly report.

**Configure/build when:** clients have small portfolios, SMP pricing is uneconomic, or direct integrations are unnecessary. Begin read-only and accept manual mapping/reconciliation as a supported task.

### Option 3 — Dirtyworks multi-client overlay

Use one or more customer-owned SMPs as data sources, then build a small Dirtyworks layer for cross-client operations: source/freshness, exceptions, tickets, service scope, customer approvals, monthly report and portfolio-level internal work queues.

**Build when:** at least three clients share the workflow; multi-client navigation/reconciliation consumes measurable time; a partner funds the requirement; or an existing product cannot safely provide the required service-provider view/export.

### Option 4 — full aggregator product

Build vendor, finance and bank connectors, a normalization engine, mapping rules, budgets, reporting and a customer portal.

**Build only when:** existing SMPs fail a repeated, valuable requirement and the connector/product maintenance economics are funded. This is a material software/security business, not a small internal tool.

## What could become defensible

Generic transaction aggregation and charts are already available. A stronger Dirtyworks asset would be:

- an AI-product capability and cost adapter library designed for managed-service use;
- source-aware reconciliation of contracted, purchased, assigned, active, consumed, invoiced and paid facts;
- client/partner responsibility and approval workflows;
- cost anomalies that create a documented support/change process;
- comparable monthly decision reports across vendors without manufacturing false equivalence;
- reusable onboarding, optimization, renewal and offboarding playbooks;
- an agent interface over isolated, customer-owned systems;
- permissioned benchmarks based on normalized portfolio facts and real operating outcomes.

The moat is the operating method and accumulated connector/reconciliation knowledge. It should not depend on captive customer data.

## Demonstration scorecard

Test 1Password SaaS Manager and one comparator using a synthetic two-client scenario:

| Criterion | Weight | Required demonstration |
|---|---:|---|
| Client isolation/MSP operation | 20 | Operators move between two unrelated customers without data leakage or shared configuration |
| AI product coverage | 15 | ChatGPT Enterprise/OpenAI and one second AI vendor show users, usage/cost, source and freshness |
| Finance reconciliation | 15 | Import QuickBooks or Xero-like transactions, map/split an ambiguous vendor and preserve invoice/expense distinction |
| Licence and usage | 10 | Purchased, assigned and active quantities remain separate and traceable |
| Contract/renewal | 10 | Record rate, term, notice date, commitment and renewal decision |
| API/MCP/export | 10 | Retrieve client/app/cost/usage/contract data and export the complete client record |
| Agent safety | 5 | Read-only service identity, scoped credentials, audit and no raw secret exposure |
| Privacy/security | 5 | Region/subprocessors, retention, user-level controls, SSO/MFA and incident terms |
| Service workflow | 5 | Create or link Freshdesk work from a cost/access exception |
| Commercial fit | 5 | Quote, minimums, implementation, client ownership, MSP rights and exit costs fit the package economics |

Reject a platform if it cannot isolate clients, export client records, identify data source/freshness, or keep estimated usage cost distinct from issued invoices.

## Recommended experiment

1. Request a 1Password SaaS Manager trial and quotes for one 25-user client, five separate SMB clients, and an MSP/service-provider structure.
2. Ask explicitly whether Enterprise Password Manager MSP multi-tenancy extends to SaaS Manager; request the contract/product documentation rather than relying on a sales assurance.
3. Connect only synthetic/test data first: one identity source, a QuickBooks/Xero sample, one ChatGPT Enterprise/OpenAI source and one second AI product.
4. Reconcile three cases: fixed seats, annual prepayment and variable consumption.
5. Test the REST API and read-only MCP surface through the planned agent interface.
6. Compare with one broad SMP such as CloudEagle or Zylo using the same script.
7. Measure quote cost, setup hours, mapping exceptions, connector gaps, monthly effort and report quality against the lightweight register.
8. Choose buy, lightweight register or overlay from evidence; do not authorize bank connectivity or production writes during this experiment.

## Research sources

### 1Password SaaS Manager

- Product and current capabilities: <https://1password.com/product/saas-manager>
- AI spend management: <https://1password.com/solutions/ai-spend-management>
- AI consumption setup, budgets and limitations: <https://support.1password.com/saas-manager-review-your-ai-spend-and-consumption/>
- Finance-system ingestion and transaction fields: <https://support.1password.com/saas-manager-connect-to-a-finance-system/>
- Spend mapping and invoice/expense distinctions: <https://support.1password.com/saas-manager-analyze-your-saas-spend/>
- Application/identity/finance discovery methods: <https://support.1password.com/saas-manager-discover-and-manage-more-apps/>
- API: <https://support.1password.com/saas-manager-1password-saas-manager-api/>
- MCP server: <https://support.1password.com/saas-manager-mcp-server/>
- Quote-only enterprise pricing: <https://1password.com/pricing/enterprise>
- Password-manager MSP scope: <https://1password.com/product/enterprise-password-manager-msp-edition>

### Comparators

- CloudEagle integrations and platform: <https://www.cloudeagle.ai/integrations>
- CloudEagle AI usage and token/credit scope: <https://www.cloudeagle.ai/product/ai-governance/ai-usage-control>
- CloudEagle current pricing description: <https://www.cloudeagle.ai/blogs/bettercloud-pricing-guide>
- Zylo integrations, API and MCP: <https://zylo.com/product/integrations>
- Zylo consumption cost management: <https://zylo.com/blog/consumption-cost-management>
- Productiv data sources and engagement model: <https://help.productiv.com/article/542-welcome-to-productiv>
- BetterCloud pricing mechanics and modules: <https://www.bettercloud.com/pricing/>
- BetterCloud spend optimization: <https://www.bettercloud.com/platform/spend-optimization/>
- Zluri/NetSuite spend example: <https://www.zluri.com/integrations/netsuite>
- Lumos discovery, usage and licence optimization: <https://www.lumos.com/blog/when-it-comes-to-saas-management-and-security-risks-you-cant-be-the-cool-mom>
- Vendr premium product/pricing scope: <https://help.vendr.com/en/articles/8432894-overview-premium-intelligence>
- Flexera SaaS and AI management: <https://www.flexera.com/products/flexera-one/saas-management>
- Flexera AI cost management: <https://www.flexera.com/products/ai-cost-management>
- ServiceNow SAM SaaS functions: <https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/saas-dashboard-workspace.html>
- ServiceNow service-provider domain separation: <https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/domain-separation-software-asset-management.html>
- Nudge Security pricing and scope: <https://www.nudgesecurity.com/pricing>
- Reco AI/SaaS security scope: <https://www.reco.ai/platform/ai-governance-security>
- Veza identity-security scope: <https://veza.com/>
- ConductorOne identity-governance scope: <https://www.conductorone.com/product-tour/>
- Torii API/custom integration model: <https://developers.toriihq.com/docs/introduction>

### Plaid transaction layer

- Transactions API: <https://plaid.com/docs/api/products/transactions/>
- Transaction timing and mutability: <https://plaid.com/docs/transactions/transactions-data/>
- US/Canada institution coverage: <https://plaid.com/docs/institutions/>

## Stuck / unable-to-continue record

No execution blocker was encountered. Public sources do not establish 1Password SaaS Manager's SMB/MSP pricing or a SaaS Manager multi-client console equivalent to Enterprise Password Manager MSP Edition. These are explicit quote and demonstration gates. Plaid production pricing, customer willingness to authorize financial accounts and required Canadian financial-data/privacy controls are also unknown; they do not block an accounting-first or SMP trial.
