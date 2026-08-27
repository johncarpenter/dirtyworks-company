# Hudu client documentation structure — optional alternative

**Version:** 0.1  
**Date:** 2026-08-26  
**Owner:** Service operations  
**Status:** Superseded as the launch default by the [Markdown client repository operating model](markdown-client-repository-operating-model.md); retained as a migration/alternative specification

## Historical decision and current role

The original working decision placed customer onboarding and internal runbooks in Hudu. The sponsor subsequently selected one private Git-backed Markdown repository per client with an internal interface and derived knowledge graph. Hudu is therefore not required for launch. This document remains useful if later audit, permissions, collaboration, portal or maintenance evidence triggers a migration.

If Hudu is selected later, it should be the private operating manual and relationship map for each customer. It should not become a second ticketing system, password vault, contract repository, accounting ledger or replacement for a vendor's live administrative state.

```text
Customer conversation/request  -> Freshdesk
Private operating context      -> Hudu
Credential or secret           -> 1Password
Signed agreement               -> Contract repository
User/configuration/usage fact  -> Native vendor/identity system
Issued/paid financial fact     -> Vendor invoice + accounting/AP
Operational reconciliation     -> Hudu record / controlled register
```

Hudu records how Dirtyworks.ai operates the service, who owns it, when facts were verified and where authoritative evidence lives. Freshdesk ticket IDs, vendor record IDs and contract/invoice links connect the workflow without copying entire records between systems.

## What belongs where

| Record | Primary authority | Hudu treatment |
|---|---|---|
| Customer request, response and ticket status | Freshdesk | Link ticket and summarize durable operating learning only |
| Internal runbook and responsibility map | Hudu | Full internal operational record |
| Customer-facing help article | Freshdesk knowledge base | Link the published/versioned article; retain private source notes if needed |
| Password, recovery code, secret or token | 1Password | Record only item reference, purpose, role and owner |
| Signed MSA, Order or data schedule | Contract repository | Link, record operational metadata and obligations; do not treat summary as legal text |
| Product users, roles and current configuration | Native vendor / identity system | Record last verified snapshot, source and reconciliation result |
| Vendor invoice and payment | Vendor + accounting/AP | Record period, amount/source and reconciliation; do not overwrite source evidence |
| Product cost, renewal and licence operating view | Hudu/controlled register | Maintain normalized operational record with source links and observed date |
| Incident customer communications | Freshdesk / approved incident channel | Link timeline and retain private operational/technical summary as appropriate |
| Change request and approval | Freshdesk or chosen change authority | Link approval; store resulting configuration/runbook update and verification |

Do not enable a Hudu customer portal merely because it exists. Freshdesk is the initial customer-facing portal. A second portal adds identity, content-publication and record-conflict work; enable it only for a specific document-access need that Freshdesk cannot meet.

## Client workspace structure

Use the same numbered structure for every direct customer. For white-label or co-managed work, add a `Prime MSP and responsibility seam` record under section 01.

### 00 — Account charter

- client ID, legal/operating name and domain;
- service owner and backup;
- outcome, supported uses, exclusions and current lifecycle stage;
- product/user/service summary;
- key system record IDs and links;
- current risks, conditions and next review.

### 01 — Contacts and responsibilities

- executive sponsor;
- operating, access/security, finance/procurement and incident contacts plus alternates;
- Dirtyworks.ai and MSP contacts;
- RACI/responsibility seam;
- approval and emergency authority.

### 02 — Contracted service

- authoritative contract links and IDs;
- order dates, term, renewal, notice and payment metadata;
- scope, exclusions, service targets, change allowance and customer dependencies;
- operational obligations and evidence dates;
- open condition/exception register.

### 03 — Products and tenants

- one record per product/tenant/account;
- vendor, plan/SKU, seller of record and customer owner;
- tenant/admin URL, data-use/location/retention notes and support route;
- approved use, user groups, configuration baseline and last verification;
- export, suspension and exit path.

### 04 — Users and privileged access

- access model, identity provider/MSP seam and JML owner;
- administrator roles and customer approval;
- 1Password item references—never copied secrets;
- access review, exception, creation and revocation dates;
- last reconciled roster evidence.

### 05 — Support and runbooks

- support/service overview and Freshdesk company/policy IDs;
- product administration runbooks;
- JML, support triage/vendor escalation, change, incident and recovery runbooks;
- linked public Freshdesk knowledge articles;
- repeated-failure and problem records.

### 06 — Training and adoption

- administrator and role-based user training plans;
- approved materials, versions and Freshdesk article links;
- session/completion record and follow-up needs;
- approved adoption/outcome measures and privacy boundary.

### 07 — Costs, licences and renewals

- purchased, assigned and available active/usage definitions;
- price, currency, tax, billing period, invoice/accounting source and observed date;
- contract renewal, notice, cancellation, approval and budget owner;
- monthly reconciliation, variance and optimization action;
- vendor cost separate from Dirtyworks.ai service fee.

### 08 — Security, privacy and governance

- data classification/use summary and processing authority links;
- vendor/subprocessor, location, retention and training/data-use settings;
- security baseline, access review, risk/exception and next review;
- privacy/security assessment and specialist-review links;
- supported/prohibited use and human-accountability boundary.

### 09 — Changes and incidents

- durable change/configuration summaries linked to approval and native evidence;
- incident/problem summaries linked to Freshdesk/incident records;
- cause, correction, recurrence prevention and runbook impact;
- no unnecessary secrets or sensitive customer content.

### 10 — Reports and reviews

- onboarding/release decision;
- stabilization checkpoints;
- monthly cost/service report and customer decisions;
- quarterly access, renewal, vendor and service-fit review;
- measured effort, direct cost, exception and margin learning.

### 11 — Offboarding and portability

- access revocation and customer/vendor actions;
- product/export, configuration, register, runbook and evidence package;
- credential transfer/removal and 1Password cleanup;
- retention/deletion confirmation and residual risk;
- closure approval and final Freshdesk communication.

## Required structured record types

Configure these as structured assets/templates if Hudu supports the needed relationships; otherwise begin with controlled page templates and migrate only when search/reporting pain appears.

| Record type | Minimum fields |
|---|---|
| Client account | Client ID, owner/backup, lifecycle, scope summary, critical contacts, next review |
| Contact/role | Person, role, authority, channel, alternate, last verified |
| Contracted service | Order ID/link, start/renewal/end, services, users, targets, exclusions, dependencies |
| Product tenant | Product/vendor, plan, tenant ID, owners/admins, source URL, status, last verified |
| Access reference | Person/service identity, role/scope, approver, 1Password item reference, review/revoke dates |
| Cost and renewal | Product, quantity/definition, price/currency/tax, period, invoice source, renewal/notice, observed date |
| Runbook | Purpose, trigger, authority, prerequisites, steps, evidence, exceptions, escalation, rollback, owner/version/review |
| Training record | Audience, material/version, delivery date, completion owner, follow-up, evidence |
| Risk/exception | Description, consequence, owner, control, approval, expiry, status |
| Decision/change | Request/source, approver, implementation, verification, linked ticket/native evidence |
| Review/report | Period, cut-off, sources, findings, decisions, actions, customer delivery link |

Every structured record must include:

- client ID and classification;
- record owner and backup;
- status and lifecycle dates;
- primary source system and record/link;
- `last verified at` and verifier;
- next review/expiry;
- related Freshdesk ticket/change/incident where applicable.

## Runbook template

Every Hudu runbook should answer:

1. **Purpose and trigger:** why and when the procedure runs.
2. **Scope and authority:** customers/products covered and who may request, approve and execute.
3. **Prerequisites:** access, evidence, maintenance window, customer dependency and safety check.
4. **Procedure:** numbered actions with expected result; avoid embedding secrets.
5. **Verification:** authoritative system checked, expected/actual state and retained evidence.
6. **Exception and escalation:** when to stop, open a Freshdesk ticket, seek approval or involve the vendor/customer.
7. **Rollback or containment:** safe reversal, suspension or alternate path.
8. **Records updated:** Hudu, Freshdesk, native vendor, 1Password or finance record.
9. **Ownership:** author, approver, version, last test and next review.

## Initial runbook set

- [ ] New customer onboarding and release.
- [ ] Product approval and tenant baseline.
- [ ] User joiner, mover and leaver.
- [ ] Privileged access issue, review and revocation.
- [ ] Standard product configuration/change and rollback.
- [ ] Freshdesk support triage, priority and vendor escalation.
- [ ] P1 incident containment and customer escalation.
- [ ] Administrator/user training and material update.
- [ ] Monthly licence/cost reconciliation and variance review.
- [ ] Renewal, cancellation and budget decision.
- [ ] Vendor outage, material feature/term/subprocessor change.
- [ ] Quarterly access/service review.
- [ ] Customer offboarding, export, deletion and closure.

Product-specific runbooks should be added only for products Dirtyworks.ai actually supports. A generic `ChatGPT`, `Microsoft Copilot`, `Claude` or other template is not considered tested until run against the applicable business plan and customer configuration.

## Hudu configuration and acceptance checklist

- [ ] Global roles enforce least privilege and customer separation.
- [ ] MFA/SSO, recovery and operator offboarding are configured.
- [ ] Templates and relationships support the record types above without free-text duplication.
- [ ] Sensitive fields are minimized; secrets are represented only by 1Password references.
- [ ] Search returns the account charter, current product owner, access procedure and renewal record quickly.
- [ ] Links open the correct Freshdesk, vendor, contract and finance authority.
- [ ] Last-verified and next-review fields can produce a stale-record work queue.
- [ ] Export/backup produces a readable client operating package.
- [ ] A synthetic client passes onboarding, user removal, support escalation, monthly cost close and offboarding dry runs.
- [ ] Time to maintain the record is measured during the first customer; unused fields are removed and missing repeated facts are added.

## Governance rule

Hudu is valuable only if it is current. A runbook is not complete because prose exists; it is complete when an authorized operator can execute it, verify the result at the authoritative source, record exceptions and safely stop or reverse the work. Stale or duplicated records are operating risks and must surface in the review queue.
