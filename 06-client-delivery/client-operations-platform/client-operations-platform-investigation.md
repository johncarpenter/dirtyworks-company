# Client operations platform investigation

**Version:** 0.1  
**Date:** 2026-08-25  
**Status:** Working decision memo; validate through product demonstrations and the first two production accounts  
**Decision owner:** Sponsor  
**Scope:** How Dirtyworks.ai records, supports, operates, reports on, and offboards managed AI clients—and when proprietary software becomes justified

> **2026-08-26 scope clarification:** The launch core is managed packaged AI SaaS, not hosted/custom AI infrastructure. For that core, use Freshdesk as the client support surface, one private Git-backed [Markdown client repository](markdown-client-repository-operating-model.md) per end customer as the private operating source, 1Password for privileged access, and native vendor administration/invoices plus a controlled product/access/cost register. Hudu and PSA/ITSM-grade backbones remain conditional alternatives for partner, permission, audit, portal or workflow requirements; LLM observability, application monitoring and the AI Operations Ledger remain conditional layers for advanced workloads or repeated operational pain. See the [core managed AI SaaS operating model](../service-design/core-managed-ai-saas-operating-model.md).

## Executive finding

Dirtyworks.ai needs a client operations system, but it should not begin by building a PSA, RMM, service desk, documentation vault, or enterprise AI-governance suite.

The working architecture is:

```text
Customer and vendor systems       Authoritative identity, configuration, usage and billing facts
            ↓
PSA / ITSM backbone               Clients, contracts, tickets, changes, time, SLA and billing work
            ↕
AI operations registry            Products, use cases, sources, controls, evaluations, cost and evidence
            ↓
Customer reporting / portal       Status, decisions, value, risks, renewals and export
```

For the first accounts, the AI operations registry should be configured inside a flexible PSA/ITSM asset model or documentation platform. Dirtyworks.ai should add an integration and reporting layer only after repeated delivery shows which records, rules and reconciliations are stable. A multi-tenant proprietary control plane becomes a rational product investment when it removes measured recurring work, supports multiple operators or MSP partners, or materially improves evidence and customer retention.

This is a **buy the service backbone, configure the operating model, then selectively build the differentiated layer** direction. It is a working recommendation under the current half-time-founder and $5,000–$50,000 experiment constraint—not an irreversible platform selection.

## What must be operated per client

Traditional MSP systems centre on devices, infrastructure, tickets, contracts and technician work. Dirtyworks.ai needs those mechanics plus records that describe whether an AI-supported capability is approved, bounded, useful and still behaving as intended.

### Minimum client operating record

| Record | Minimum contents | Operational decision enabled |
|---|---|---|
| Account charter | legal/customer name, sponsor, operational contacts, MSP seam, support window, criticality | Who owns the relationship and escalation? |
| Contracted service | Order, included/excluded work, quantities, service targets, term, allowance, dependencies | Is the request covered and billable? |
| AI product/tenant | vendor, product/plan, tenant owner, commercial path, admins, renewal, support path, terms snapshot | What is deployed, who owns it and when must it be reviewed? |
| Supported use case | purpose, users, question/action domain, outcome baseline, exclusions, risk class, human decision point | What may the service do, and where must it stop? |
| User/access entitlement | named user/group, role, licence, approver, start/review/end date, provisioning evidence | Does the right person have the right access? |
| Knowledge/data source | source, owner, classification, connector, permissions, freshness, retention, location | What information can the service use and trust? |
| Integration/action | systems, credential owner, permissions, inputs/outputs, approval, exception, rollback, kill switch | Can a workflow act safely and be stopped? |
| Control/evidence | obligation, control statement, owner, implementation status, evidence link, test/review date | Can Dirtyworks.ai demonstrate rather than merely assert the control? |
| Evaluation suite/run | test class, expected behaviour, version, environment, result, exception, approver | Is the supported service still performing within its release boundary? |
| Request/incident/problem/change | affected service/use case/product, priority, timeline, actions, cause, approval, outcome | What happened, how was it handled and what must change? |
| Cost and usage meter | source period, vendor/account/project/key, quantity, currency, cost, allocation, budget, variance | Is spend understood, attributable and controlled? |
| Training/approval | audience, version, completion, acknowledgement, policy or release decision | Were users and owners enabled and accountable? |
| Value scorecard | baseline, current measure, adoption context, support burden, benefit evidence, decision | Should the service continue, change, expand or stop? |
| Renewal/offboarding | notice date, decision date, export, transfer, revocation, deletion/retention evidence, residual action | Can the client renew deliberately or leave cleanly? |

The record must be relationship-based. A ticket should point to the affected client, service, use case, product, source or integration; a change should point to the evaluation run and approval that released it; a renewal should point to cost, use, value and open risk.

## Systems of record

One product should not be declared authoritative for every fact. Use explicit ownership:

| Information | Authoritative system | Dirtyworks.ai copy |
|---|---|---|
| Customer identities and groups | Customer identity provider | IDs, entitlement state, approver and reconciliation result—not passwords |
| Vendor tenant configuration and usage | Customer-owned vendor tenant/API | Normalized snapshots, exceptions and evidence timestamps |
| Contract, covered work, time and ticket state | Dirtyworks.ai or prime MSP PSA/ITSM | Direct record or stable external ID |
| Invoices and payment | Accounting system / PSA billing | Status and reference, not a shadow ledger |
| Customer source truth | Customer source systems | Register, metadata and approved evidence only; no unnecessary duplicate content |
| AI operating scope and control history | AI operations registry | Primary Dirtyworks.ai operating record, exportable to the customer |
| Secrets and privileged credentials | Approved secrets manager/customer vault | Reference and owner only |
| Large evidence artifacts | Controlled document/object repository | Immutable link, checksum/version, owner and retention class |

This prevents the future control plane from becoming an uncontrolled copy of prompts, personal information, customer documents and credentials.

## Core support and maintenance workflows

### 1. Contract-to-onboarding

1. Convert the signed Order into a client, contracted service, supported-use and product record.
2. Create dependencies, launch tasks, owners, acceptance tests and recurring review dates.
3. Record the MSP/Dirtyworks.ai/customer responsibility seam.
4. Block production until required control, access and evaluation gates pass.

### 2. Joiner, mover and leaver

1. Receive a named request or identity event.
2. Confirm customer approval and contracted product/use scope.
3. Provision, change or revoke in the customer-owned platform.
4. Reconcile the authoritative vendor/identity state.
5. Save outcome and exception evidence; never treat a closed task as proof that access changed.

### 3. Support request

1. Intake by portal/email/partner handoff and identify affected service/use case/product.
2. Classify P1–P4 and coverage; route out-of-scope work to change/quote.
3. Triage across source, permission, product, prompt/configuration, integration and user-learning failure classes.
4. Resolve or escalate to the customer, prime MSP or vendor.
5. Link recurring or systemic failures to a problem record and evaluation-set update.

### 4. Incident

1. Contain through the documented suspension or kill-switch path.
2. Preserve timeline, actors, affected information, evidence and decisions.
3. Trigger the contractual privacy/security notification seam.
4. Correct the service, run regression/permission tests and obtain release approval.
5. Produce the incident record and recurrence-prevention actions.

### 5. Vendor or configuration change

1. Capture a vendor release, model change, term/subprocessor change, configuration request or detected drift.
2. Assess affected clients, supported uses, controls, costs and tests.
3. Test in the appropriate environment; record results and exceptions.
4. Approve, schedule, release and verify—or suspend/retire the product.

### 6. Monthly operation and review

1. Reconcile contracted, assigned, active and valuable licences/products.
2. Import or review usage, cost, service, evaluation, source-freshness and risk signals.
3. Create work for anomalies rather than hiding them in a report.
4. Record decisions: continue, train, remediate, right-size, expand, replace or retire.
5. Publish a client-readable service and value report from the same records.

### 7. Renewal or offboarding

1. Start before the cancellation deadline.
2. Review use, cost, value, overlap, risk, operational ownership and alternatives.
3. If exiting, export the current register, configuration, runbooks, evaluations and history permitted by contract.
4. Transfer/revoke access, handle vendor subscriptions and complete return/deletion evidence.

## Existing product categories

The market has capable components, but no reviewed category covers Dirtyworks.ai's complete operating promise.

| Category and examples | Strong at | Missing or constrained for Dirtyworks.ai |
|---|---|---|
| MSP PSA: Halo, ConnectWise PSA, Autotask/Kaseya BMS, SuperOps | clients, agreements, service desk, SLA, projects, time, products, invoicing and profitability | AI-use boundaries, evaluation lineage, source reliability, model/vendor normalization and human-control evidence are not the native centre |
| ITSM/CMDB: Freshservice for MSPs, Jira Service Management Assets | requests, incidents, problems, changes, flexible assets, relationships, workflow, portal and reports | PSA finance/reseller reconciliation may be weaker; AI schema and vendor collection must be configured |
| MSP documentation: Hudu, IT Glue | client-separated documentation, assets, SOPs, relationships, credentials, review/version history | Not the primary ticket, SLA, change, time or billing engine; operational status can become stale without reconciliation |
| SaaS management: BetterCloud, Zluri, Zylo | app discovery, licences, access lifecycle, shadow SaaS/AI, spend, renewals and some automation | Often buyer-internal/enterprise-oriented; does not prove use-case quality, knowledge correctness or Dirtyworks.ai service work |
| AI governance: Credo AI, IBM watsonx.governance | AI inventory, risk/policy workflow, factsheets, lifecycle evidence and assessments | Enterprise complexity/pricing; does not replace MSP ticketing, billing, product administration or customer success |
| AI/data security: Microsoft Purview DSPM, Netskope, Cisco AI Defense | AI discovery, sensitive-data exposure, runtime/security controls, model/application validation | Environment-specific and security-centred; not a cross-vendor customer/service ledger |
| LLM observability/gateway: Langfuse, LangSmith, Portkey | traces, evaluations, prompts, model calls, latency, cost, budgets, routing and alerts | Covers instrumented API applications, not every seat-based SaaS tool, user, contract, source or support process |

### Evidence from current products

- Halo currently presents one per-agent platform with service, incident, change, CRM, contracts, CMDB, projects, billing, reporting, portal and data export. [Halo pricing/capabilities](https://www.usehalo.com/pricing)
- ConnectWise PSA agreements link covered assets, recurring revenue and per-agreement SLAs; its product also spans tickets, projects, procurement and billing. [ConnectWise agreements](https://docs.connectwise.com/ConnectWise_Documentation/080/017), [ConnectWise capability comparison](https://www.connectwise.com/platform/psa/request-pricing/compare-features)
- Freshservice for MSPs provides multi-client service delivery, client-specific workflows/portals, automation and reporting; Freshservice also supports incident/problem/change, contracts, SaaS management and CMDB capabilities by plan. [Freshservice for MSPs](https://www.freshworks.com/freshservice/msp/), [Freshservice features](https://www.freshworks.com/freshservice/features/)
- Jira Service Management Assets permits flexible object schemas and links objects to requests, incidents and changes, making it a plausible host for an early AI registry. [Atlassian Assets](https://www.atlassian.com/software/jira/service-management/features/asset-and-configuration-management)
- Hudu explicitly distinguishes its documentation role from PSA work and RMM devices; it supports structured client records, relationships, audit/version history, API and export. [Hudu product overview](https://www.hudu.com/product/overview)
- BetterCloud and Zluri demonstrate that SaaS/AI-app discovery, user lifecycle, access, licence/spend and renewal management are established categories rather than capabilities Dirtyworks.ai should recreate. [BetterCloud platform](https://www.bettercloud.com/), [Zluri SaaS management](https://www.zluri.com/saas-management)
- Credo AI and IBM demonstrate that AI registries, use-case workflows, risk/control mapping, factsheets, evaluation and lifecycle evidence are also established enterprise categories. [Credo AI platform](https://www.credo.ai/product), [IBM watsonx.governance planning](https://www.ibm.com/docs/en/watsonx/saas?topic=ai-planning-governance)
- Microsoft Purview and Netskope demonstrate environment-specific AI discovery and data/security governance. [Microsoft Purview DSPM for AI](https://learn.microsoft.com/en-us/purview/dspm-for-ai), [Netskope AI Command Center](https://docs.netskope.com/en/ai-command-center)
- Langfuse, LangSmith and Portkey provide instrumented application telemetry, evaluations, cost tracking or gateway limits; this data should be referenced or normalized, not rebuilt from raw inference. [Langfuse cost tracking](https://langfuse.com/docs/observability/features/token-and-cost-tracking), [LangSmith observability](https://docs.langchain.com/langsmith/observability), [Portkey AI Gateway](https://portkey.ai/docs/product/ai-gateway)

## Vendor integration reality

The control layer must use an adapter model with explicit capability states:

`API current` · `export current` · `manual attestation` · `unavailable` · `not contracted`

Examples as of the document date:

- OpenAI's official API documents organization/project users, keys, usage and costs. Admin credentials are elevated and should be isolated per customer; the interface does not make every separate seat product or business outcome automatically observable. [OpenAI Admin API](https://developers.openai.com/api/reference/resources/admin/subresources/organization/subresources/admin_api_keys), [OpenAI usage API](https://developers.openai.com/api/reference/python/resources/admin/subresources/organization/subresources/usage)
- Anthropic's Admin API covers organization members, workspaces, keys and reports for supported organization types; its documentation identifies different availability and credential paths across Claude Platform, Claude Enterprise and AWS. [Anthropic Admin API](https://platform.claude.com/docs/en/manage-claude/overview), [Anthropic usage and cost API](https://platform.claude.com/docs/en/manage-claude/usage-cost-api)
- OpenRouter supports management APIs for creating keys and applying usage limits, making per-workload keys a practical attribution mechanism where that commercial path is approved. [OpenRouter management keys](https://openrouter.ai/docs/guides/overview/auth/management-api-keys)
- Microsoft 365 provides its own Copilot readiness, licence, usage and agent reports, but Microsoft distinguishes official usage reporting from audit-log data intended for security/compliance. The control layer should preserve each source's meaning rather than manufacture a universal “active user” metric. [Microsoft 365 Copilot reports](https://learn.microsoft.com/en-us/copilot/microsoft-365/microsoft-365-copilot-reports-for-admins), [Microsoft Copilot usage-report caveat](https://learn.microsoft.com/en-us/microsoft-365/admin/activity-reports/microsoft-365-copilot-usage?view=o365-worldwide)

Therefore every connector requires a capability contract: facts provided, plan prerequisites, permissions, freshness, pagination/rate limits, retention, failure handling, financial reconciliation authority and last successful sync. Manual review is a supported collection method—not a hidden integration failure.

## Real implementation options

### Option A — MSP-native PSA as the backbone

**Mechanism:** Configure client, agreement, ticket, change, asset and custom-field structures in Halo, SuperOps, ConnectWise or Autotask. Attach Hudu/IT Glue only if its stronger documentation/credential model is required.

**Best fit:** Direct managed service with recurring billing, or an MSP partner that already operates one of these systems.

**Advantages:** Mature MSP economics, service desk, SLA, time, contract and billing flow; partner familiarity; less custom back-office work.

**Constraints:** Implementation effort, possible minimums/contract terms, uneven custom-object experience, and risk that the PSA remains device/product-centred. White-label deals may require Dirtyworks.ai to work in the prime MSP's tenant rather than its own.

### Option B — Flexible ITSM/asset platform as the backbone

**Mechanism:** Use Freshservice for MSPs or Jira Service Management with a custom AI object schema and linked request/incident/change workflows; keep accounting external.

**Best fit:** The first priority is controlled service delivery and an adaptable AI registry rather than mature MSP procurement/billing.

**Advantages:** Flexible relationships, workflows and portals; faster schema experimentation; Jira Service Management has a free tier up to three agents, while paid plans add stronger asset/control capability. [Atlassian plan overview](https://support.atlassian.com/jira-cloud-administration/docs/explore-jira-cloud-plans/)

**Constraints:** More finance, agreement-profitability and licence-reconciliation work may remain outside the platform. Multi-client isolation and MSP functionality must be demonstrated, not assumed from general ITSM features.

### Option C — Documentation-led early system

**Mechanism:** Use Hudu structured assets/processes for the client operating record and a lightweight ticket tool or the partner's PSA for work.

**Best fit:** One operator, very few clients, strong need for client-separated runbooks and evidence, and no recurring billing complexity yet.

**Advantages:** Low entry cost, no user minimum, API/export, self-hosted or hosted option; public pricing was USD $30/user monthly or $27/user/month billed annually on the document date. [Hudu pricing](https://www.hudu.com/pricing)

**Constraints:** Two-system reconciliation begins immediately; Hudu should not be made into a substitute PSA. This is a bridge, not likely the scaled architecture.

### Option D — Proprietary multi-tenant platform now

**Mechanism:** Build the complete system of record, service desk, adapters, workflow, portal and reporting application before repeated customer operation.

**Best fit:** Only if a signed anchor customer or MSP funds it and defines requirements that existing platforms cannot configure.

**Advantages:** Exact experience and data model; potential future product/channel asset.

**Constraints:** Highest security, privacy, multi-tenancy, support, migration and maintenance exposure. Under the current budget, an MVP could cover a registry and a few read-only integrations—not credible PSA, enterprise governance and universal vendor control parity.

## Working platform selection scorecard

Do not choose from a logo comparison. Demonstrate these jobs using a synthetic client:

| Criterion | Weight | Demonstration |
|---|---:|---|
| Multi-client isolation and partner seam | 15 | Separate direct, co-managed and white-label records/portals with least privilege |
| Relationship model | 15 | Link customer → service → use case → product/source/control → ticket/change/evaluation |
| Service operations | 15 | Intake, priority, SLA clock, escalation, incident/problem/change and approval |
| Contract, time and profitability | 10 | Covered/out-of-scope work, allowance, time, cost, invoice handoff and margin |
| API, webhooks and export | 10 | Create/read/update required records, receive events and export the complete client record |
| Evidence and documentation | 10 | Version, review, approval, immutable artifact link and audit history |
| Security/privacy | 10 | SSO/MFA, role isolation, audit, retention, region, backup and subprocessor facts |
| Customer experience | 5 | Request, approval, status, report and export without exposing other clients |
| Implementation burden | 5 | Time to usable workflow and ongoing administration |
| Commercial fit | 5 | Current total cost, minimums, term, implementation and exit terms |

Reject a platform if it fails tenant/client isolation, usable export, API access, auditability or the actual support workflow even when its aggregate score is high.

## What Dirtyworks.ai may eventually build

Working name: **Dirtyworks AI Operations Ledger**. It is a normalization, control and evidence plane—not an RMM agent and not the customer's source of truth.

### Initial differentiated capabilities

1. A multi-vendor AI product, use-case, source, integration and responsibility graph.
2. Versioned supported-use boundaries and customer approvals.
3. Vendor capability adapters for identity, usage, cost, key/project/workspace and configuration facts.
4. Contract-to-control mapping: show which operational evidence supports which customer commitment.
5. Evaluation lineage from release through incident, remediation and regression.
6. Reconciliation that creates PSA tickets for drift, missing evidence, approaching budgets/renewals and failed checks.
7. A monthly client read model combining service, cost, use, quality, risk and value without copying unnecessary raw content.
8. A portable customer exit package.

### Explicit non-goals

- General endpoint/network RMM, antivirus, patching or remote-control functionality.
- Replacing the prime MSP's PSA when Dirtyworks.ai is a subcontractor.
- Storing customer administrator passwords or universal master credentials.
- Capturing all employee prompts by default.
- Claiming legal compliance or model accuracy from a dashboard state.
- Universal automated control of products whose plans or APIs do not support it.
- Customer lock-in through inaccessible records or proprietary export.

## Does the software create a moat?

Potentially—but only some layers are defensible.

| Asset | Defensibility | Why |
|---|---|---|
| Generic tickets, dashboards and portal | Low | Mature PSA/ITSM platforms already provide them |
| Custom AI inventory fields | Low–medium | Easy to copy once visible; useful operationally but not sufficient |
| Normalized cross-vendor schema and adapters | Medium | Requires sustained maintenance across changing plans, APIs and semantics |
| Product runbooks and control/evidence mappings | Medium–high | Encode repeated deployment and incident experience |
| Evaluation sets, failure taxonomy and regression history by use class | High if rights permit | Improves release and support quality from accumulated operating evidence |
| De-identified/permissioned cost, support, quality and outcome benchmarks | High if legally and statistically sound | Hard to obtain without a managed customer base and consistent data definitions |
| Embedded MSP workflow, responsibility seams and partner APIs | Medium–high | Distribution plus operational integration raises replacement effort |
| Customer data captivity | Negative | Creates trust, contract, privacy and sales risk; it is not a durable or acceptable moat |

The strongest barrier is a compounding service-learning loop:

```text
More managed scopes
      ↓
More normalized exceptions, failures, costs and outcomes
      ↓
Better runbooks, evaluations, catalogue rules and benchmarks
      ↓
Faster and safer launches + clearer monthly value
      ↓
Better retention, partner confidence and managed-scope growth
```

The software makes that loop scalable. It does not create the loop before customers and disciplined delivery exist.

## Phased implementation and capital gates

Planning ranges below include licences, configuration and external implementation/development help where needed. They are not vendor quotes.

### Phase 0 — Operating schema and demos

**Timing:** now through first paid review  
**Capital:** approximately CAD $0–$2,000  
**Action:** finalize the minimum record, synthetic-client demo script and scorecard; run PSA/ITSM demonstrations; use the current workbook and documentation for discovery.

**Gate:** sponsor selects a backbone only when the live direct or MSP operating model is known.

### Phase 1 — Configured operations backbone

**Timing:** before first production account  
**Capital:** approximately CAD $2,000–$8,000 first year  
**Action:** configure the chosen PSA/ITSM, intake and support workflows, client record, access/product register, launch/change/incident templates, time/cost capture and portable evidence repository. Use vendor dashboards/exports before building adapters.

**Gate:** one complete synthetic dry run and production-readiness preflight pass.

### Phase 2 — Reconciliation and reporting prototype

**Trigger:** three active portfolios, repeated monthly reconciliation, or one signed MSP integration requirement  
**Capital:** approximately CAD $10,000–$25,000  
**Action:** build a small internal data service with stable IDs, read-only adapters for the two or three most-used vendors, reconciliation status, ticket creation and monthly report generation. Keep PSA, accounting and customer tenants authoritative.

**Gate:** saves at least eight operator hours per month, prevents a material error, or supports contracted partner capacity; security/privacy design approved before customer data ingestion.

### Phase 3 — Multi-tenant AI Operations Ledger

**Trigger:** at least 8–12 active managed clients or two operating MSP partners, stable shared schema, and a measured workflow existing tools cannot economically support  
**Capital:** approximately CAD $30,000–$75,000 for a narrow production MVP; broader connector/control-plane scope will exceed the current experiment budget  
**Action:** multi-tenant registry, approvals, connector capability contracts, evidence lineage, partner/API access and client reporting/export.

**Gate:** explicit product owner, security model, support budget, recovery plan, unit economics and paid design partners.

## Build activation test

Begin proprietary application development when at least four conditions are true:

- three or more production customers share the same record and workflow;
- two operators or an MSP partner need concurrent controlled access;
- monthly reconciliation/reporting consumes more than eight hours or 10% of recurring service gross profit;
- the same fact is manually copied between three or more systems;
- a missed/stale record creates a material support, renewal, cost, access or evidence risk;
- at least two important vendors expose stable APIs/exports that can be normalized;
- a customer or partner will pay for, co-fund or make a purchase contingent on the capability;
- the control-plane feature improves measured launch time, incident response, margin, renewal or audit-readiness.

Stop or narrow the build if an existing platform can configure the validated workflow for less than one year of build/maintenance cost, connector access is unavailable, customers will not grant the required data access, or the result merely duplicates tickets and dashboards.

## Security and data-design constraints before software

- Strong tenant isolation must be enforced and tested at every query and background job boundary.
- Privileged vendor credentials must use a secrets manager, per-customer isolation, minimum scopes, rotation and revocation; never store them in PSA notes.
- Store raw prompts/responses only when the supported use, customer instruction, retention and access model require it. Prefer metrics, IDs, classifications and evidence pointers.
- Every imported fact needs source, collection time, effective period, customer/product ID and reconciliation status.
- Financial totals must distinguish estimate, usage telemetry and invoice-reconciled cost.
- Manual and inherited controls must never appear as automatically verified.
- Changes to schema, rules, adapters and derived metrics require versioning and auditable release.
- Customer export, retention and deletion must be designed before ingestion.
- The application becomes a subprocessor/security-critical system; contracts, privacy schedule, incident plan, insurance and production preflight must cover it.

## Metrics for the operating platform

Do not measure success by record count alone:

- percentage of managed products reconciled on schedule;
- percentage of access changes verified against authoritative state;
- percentage of production services with current owner, scope, evaluation and offboarding record;
- operator minutes per user/product/client per month;
- ticket linkage to affected service/use/product and recurring-failure capture;
- time to retrieve evidence for a customer question or incident;
- cost variance between telemetry, estimate and invoice;
- renewal decisions completed before cancellation deadlines;
- customer-record export/offboarding test success;
- gross-margin and response-quality improvement attributable to the system.

## Immediate next decisions

1. Determine whether the live MSP partner requires work inside its PSA or will accept Dirtyworks.ai's system and API/email handoff.
2. Decide which backbone lane to demonstrate first: MSP-native PSA or flexible ITSM/Assets.
3. Run two scripted product demonstrations with the synthetic client and weighted scorecard.
4. Configure—not code—the minimum AI operations registry for the first paid review/production pilot.
5. Measure monthly record/reconciliation work from the first account so the software gate has evidence.

## Research basis and limitations

This is a capability and architecture investigation, not a completed procurement. Vendor sites describe available functionality but do not establish customer-specific price, contract, Canadian data treatment, API entitlement, reseller/MSP rights, implementation quality or fit. Those require demonstrations, security/privacy diligence, contract review and trial evidence. Product features and pricing should be reverified at purchase.

The operating record aligns with NIST AI RMF's voluntary emphasis on continuous governance, AI-system inventory, lifecycle monitoring, documented evaluation and decommissioning. It also reflects the FinOps Foundation's treatment of AI cost as a cross-category practice requiring allocation, reporting, forecasting, governance and business-value linkage. [NIST AI RMF Core](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/), [FinOps for AI](https://www.finops.org/framework/technology-categories/ai/)
