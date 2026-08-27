# Dirtyworks AI Operations Ledger — application concept

**Version:** 0.1  
**Date:** 2026-08-25  
**Status:** Concept only; implementation deferred behind the activation test  
**Parent decision:** [Client operations platform investigation](../../06-client-delivery/client-operations-platform/client-operations-platform-investigation.md)

> **Launch-scope note (2026-08-26):** This application is not required to deliver the core managed AI SaaS offer. The first clients should use a controlled product/access/cost register and native vendor administration. Build this normalization layer only when repeated reconciliation work, multiple operators/partners, or a funded requirement meets the activation test.

## Product thesis

The Dirtyworks AI Operations Ledger would be a multi-tenant normalization, reconciliation and evidence layer for managed AI services. It would connect existing PSA/ITSM work records with customer-owned AI vendors, identity systems, observability tools and evidence repositories.

It is not intended to replace:

- the PSA/service desk for contracts, tickets, time, SLA and billing work;
- the customer's identity provider or AI tenant;
- accounting;
- secrets management;
- source-document systems;
- an enterprise security, DLP or GRC platform; or
- human legal, privacy, security, professional or business judgment.

## Primary jobs

| User | Job |
|---|---|
| AI operations lead | See every managed client/service, stale record, failed check, budget/renewal risk and next action |
| Support operator | Open a ticket with the exact product, supported use, source/integration, responsibility seam and runbook context |
| Customer sponsor | Review service health, cost, adoption context, quality, risk and decisions without operational noise |
| Customer approver | Approve access, use, product, source, workflow, change, exception or renewal with durable context |
| MSP partner | Route and track agreed work while preserving client separation, brand and prime/subcontractor responsibilities |
| Compliance/security reviewer | Retrieve current inventory, controls, evidence, evaluation history, incidents and unresolved exceptions |
| Finance/operations | Reconcile contracted, assigned, active, billed and valuable products without treating estimates as invoices |

## Core domain graph

```text
Partner ── responsibility seam ── Client ── Contracted Service
                                      │              │
                                      │              ├── Supported Use Case ── Risk / Control / Approval
                                      │              │          │
                                      │              │          ├── Evaluation Suite ── Evaluation Run
                                      │              │          └── Outcome / Value Measure
                                      │              │
                                      │              ├── Product Tenant ── Subscription / Cost Meter / Renewal
                                      │              │         │
                                      │              │         └── User / Group Entitlement
                                      │              │
                                      │              └── Source / Connector / Managed Action
                                      │
                                      └── Support Event ── Incident / Problem / Change / Task

Every governed object ── Evidence Reference / Version / Owner / Review / External System ID
```

## Principal entities

### Tenant and commercial context

- `Partner`: relationship model, prime role, brand mode, escalation and external PSA.
- `Client`: legal/display identity, contacts, region, data/risk profile and lifecycle state.
- `ContractedService`: Order ID, covered scope, quantities, support window, term, allowances and service targets.
- `Responsibility`: accountable/operating/approving/support role by domain and escalation path.

### Managed portfolio

- `VendorProduct`: catalogue fact/version, supported admin/usage/export capabilities and review status.
- `ProductTenant`: customer-owned tenant/account/workspace/project, admins, plan, commercial path and data locations.
- `Subscription`: SKU/quantity, estimate/invoice references, renewal/cancellation dates and seller-of-record.
- `Entitlement`: person/group/service account, role/licence, approver, lifecycle dates and reconciled state.
- `CostMeter`: vendor, account/project/key, period, units, currency, source class and allocation.

### Use, knowledge and action boundary

- `UseCase`: purpose, roles, supported/unsupported actions, risk class, outcome baseline and human control.
- `DataSource`: system, owner, classification, permission model, freshness and retention.
- `Connector`: source/destination, scopes, credential reference, sync state, error and last success.
- `ManagedAction`: tool/action, inputs, authorization, precondition, approval, exception, rollback and kill switch.

### Assurance and operation

- `Control`: obligation/risk, control statement, owner, implementation class and review cadence.
- `EvidenceReference`: source URI/object ID, checksum/version, classification, collected/effective dates and retention.
- `EvaluationSuite`: supported-use version, test classes, thresholds and critical blockers.
- `EvaluationRun`: system/config/model versions, test result, exception, reviewer and release decision.
- `ServiceEvent`: request/incident/problem/change/task with external PSA ID and affected-object relationships.
- `Approval`: decision, decision maker, authority, evidence considered, time and expiry/review.
- `ValueMeasure`: baseline, method, measured/estimated flag, period, result and sponsor decision.
- `LifecycleEvent`: launch, suspension, expansion, renewal, retirement and offboarding milestones.

## Source and evidence semantics

Every normalized observation should carry:

```text
client_id
source_system
source_record_id
source_capability
observed_at
effective_start / effective_end
collection_method: api | export | webhook | manual_attestation
confidence / reconciliation_state
schema_version / adapter_version
evidence_reference
```

Values are not interchangeable:

- `contracted` is what the customer agreed to;
- `assigned` is what an admin or identity system says is allocated;
- `active` is defined by a vendor-specific usage source;
- `billed` is invoice-reconciled;
- `valuable` is a customer/business decision supported by an agreed measure.

The product should never collapse these into one “licence health” value without showing the mechanism.

## Connector capability contract

Each adapter must declare rather than imply support:

| Capability | States |
|---|---|
| Authentication | supported scopes and credential class; customer authorization state |
| Identity | read users/groups/roles; provision/change/revoke; unavailable |
| Product structure | organization/workspace/project/key/agent or product-specific hierarchy |
| Usage | dimensions, period, delay, pagination, limits and vendor definition |
| Cost | estimate or invoice-reconciling source, currency and exclusions |
| Configuration | readable/writable fields and unsupported console-only settings |
| Events | webhooks/alerts available, polling interval or manual review |
| Evidence | returned IDs/timestamps and retention |
| Region/data | processing implications and customer-approved state |
| Health | last success, partial data, retry, disable and manual fallback |

A connector failure creates a visible exception and, when material, a PSA ticket. It must not silently reuse stale values.

## Event architecture

The ledger should not become a second service desk. It emits or consumes stable events:

```text
Order accepted → create managed objects and PSA launch work
Identity change → request/approve/vendor action/reconcile/evidence
Vendor observation → normalize/compare/exception → PSA ticket if needed
Change requested → impact/evaluation/approval → release/reconcile
Incident raised → containment/evidence/notification seam → regression/release
Monthly close → cost/use/licence/evaluation/service/value snapshot → review report
Renewal window → decision work and cancellation deadline
Offboarding → export/revoke/delete checks → completion evidence
```

All write actions must be idempotent, attributable, least-privilege and reversible where the target supports reversal. High-impact or destructive vendor actions require explicit approval and a preview of affected objects.

## Minimum useful product slice

The first custom slice should be internal and read-mostly:

1. Client, service, use-case, product-tenant and source/integration registry.
2. External IDs linking those records to the selected PSA/ITSM.
3. Read-only adapter for one vendor's identities/projects and cost/usage.
4. Manual/CSV import path using the same normalized observation contract.
5. Reconciliation exceptions and renewal/budget reminders.
6. Evidence links and current-review status.
7. Monthly internal/client report export.
8. Complete per-client structured export.

Not in the first slice: universal provisioning, raw-prompt warehouse, full customer portal, billing engine, custom ticketing, automated compliance conclusions or cross-client benchmark product.

## Security architecture requirements

- Tenant identity must be part of every database key, authorization decision, queue job, cache key, object path and audit event.
- Use row-level and application-level authorization with automated cross-tenant isolation tests.
- Separate interactive users, background services and connector credentials; use short-lived or rotatable secrets where supported.
- Store secrets in a dedicated secrets service; the database holds only credential references and scope metadata.
- Encrypt transport and storage; define region, backup, recovery, retention and deletion before production.
- Apply least-privilege role sets for Dirtyworks.ai operators, customer reviewers, approvers, MSP partners and auditors.
- Treat evidence and telemetry classifications separately; metrics may still be personal information when tied to named users.
- Maintain immutable audit events for access, approval, connector actions, export and deletion.
- Perform threat modelling, privacy assessment, dependency review, incident exercise and recovery test before the first customer tenant.
- Keep a customer-readable subprocessor and connector inventory.

## Portability contract

Every client must be able to receive, subject to the agreement:

- current portfolio, tenant and entitlement inventory;
- supported-use and responsibility records;
- source/connector/configuration register without Dirtyworks.ai secrets;
- evaluation suites/results and release decisions;
- client-specific runbooks, approved deliverables and change/incident history;
- cost/usage/value reports and source definitions; and
- offboarding actions and completion evidence.

Use common structured formats plus readable reports. Dirtyworks.ai's reusable methods, normalized schemas, adapter software and cross-client insights remain its background materials, while client records remain portable. The moat is better operation, not hostage data.

## Application activation and acceptance

Implementation remains deferred until the parent investigation's build activation test is met.

For a first production slice, acceptance requires:

- no cross-client data exposure in automated authorization tests;
- every displayed observation shows source and freshness;
- stale/partial/failed sync states are visible and cannot appear current;
- a manual import and an API connector produce the same normalized schema;
- exceptions create or link PSA work without duplicates;
- totals preserve estimate versus invoice/telemetry distinctions;
- the monthly report can be reproduced from versioned records;
- one client can be completely exported and removed according to the retention rule;
- operator effort and prevented errors are measured against the manual baseline; and
- operating savings or contracted value support continued maintenance cost.

## Open product questions

- Which PSA/ITSM owns client, agreement and work IDs?
- Does the live MSP partner require a shared instance, federation or ticket/API handoff?
- Which first two vendor products produce enough recurring work to justify adapters?
- What user-level usage is proportionate and contractually permitted versus aggregate reporting?
- Which evidence must be immutable, and where should large artifacts live?
- What Canadian region/residency and subprocessor constraints will initial customers require?
- Is the eventual buyer Dirtyworks.ai operations, the client, an MSP partner, or all three through different views?
- Will customers pay separately for the ledger/control layer, or is it a delivery-margin and retention asset inside the managed service?
