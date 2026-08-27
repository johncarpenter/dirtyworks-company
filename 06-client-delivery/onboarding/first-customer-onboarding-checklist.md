# First-customer onboarding checklist

**Version:** 0.1  
**Date:** 2026-08-26  
**Owner:** Service owner  
**Status:** First-customer working runbook; revise after every onboarding checkpoint  
**Use:** move the first signed customer from internal handoff through controlled go-live and the first monthly review

The first customer is both a delivery engagement and an operating-system test. Do not hide exceptions or automate around them. Time every phase, preserve evidence, and turn repeated steps into governed Markdown templates only after their meaning is understood.

## Definition of done

Onboarding is complete when the agreed products and users are operating; support and escalation are live; access, product, cost and training records reconcile to authoritative sources; acceptance evidence is recorded; no release blocker remains; and the customer has completed the first monthly/30-day review.

## Indicative sequence

| Window | Milestone | Gate |
|---|---|---|
| T-10 to T-7 business days | Signed handoff and records created | Scope, authority and payment confirmed |
| T-7 to T-4 | Discovery, baseline and access | Named owners and least-privilege access work |
| T-4 to T-2 | Product configuration and testing | Critical access/security tests pass |
| T-2 to T-1 | Training and support launch | Users know boundaries and help path |
| T0 | Bounded go-live | Joint release decision recorded |
| D+2 to D+10 | Stabilization | Defects, access and adoption reviewed frequently |
| D+30 | First service and cost review | Baseline reconciled; next plan approved |

Dates are targets, not promises. Customer access, vendor provisioning and unresolved security/legal issues move the gate, not the control standard.

## Phase 0 — signed work handoff

- [ ] [Pre-customer acceptance checklist](../customer-acceptance/pre-customer-acceptance-checklist.md) decision is `GO` or approved `CONDITIONAL GO`.
- [ ] MSA, Order Form and Data/Security/AI Schedule are signed by authorized parties.
- [ ] Initial payment/deposit and customer PO requirements are satisfied.
- [ ] Products, users, managed activities, exclusions, advanced work, service targets and start date match the signed order.
- [ ] Open conditions have owners, due dates and explicit go-live effect.
- [ ] Sales-to-service handoff identifies promises, objections, desired outcomes and unpriced assumptions.

**Gate:** no access request or configuration work begins without signed authority and the agreed payment condition.

## Phase 1 — create the customer operating record

### Private Markdown client repository

- [ ] Create a separate private Git-backed customer repository using the [Markdown client repository operating model](../client-operations-platform/markdown-client-repository-operating-model.md) and [template pack](../../90-templates/client-operations-repository/README.md).
- [ ] Assign customer ID, service owner, executive sponsor, operating, security, finance and incident contacts.
- [ ] Link signed contract documents from their authoritative repository; record only the operational summary and extracted approved requirements in Markdown.
- [ ] Create service, product/tenant, access-reference, cost/renewal, onboarding and offboarding records.
- [ ] Create decision, risk, exception and evidence locations.
- [ ] Configure personal-wiki proposal/review rules and restrict kgmd, if enabled, to this client's published `wiki/` pages.
- [ ] Confirm imported-source retention/provider eligibility and cross-client isolation before ingesting customer information.

### Freshdesk

- [ ] Create company and approved customer contacts; verify their domains and portal visibility.
- [ ] Assign service group, priority/SLA policy, business hours and escalation contacts.
- [ ] Send a controlled welcome/portal activation message and open the onboarding ticket.
- [ ] Test that this customer cannot see another customer's tickets or articles.

### 1Password and internal systems

- [ ] Create least-privilege client vault/collection and authorized team membership.
- [ ] Store only approved credentials/recovery material; link Markdown to item references, never secret values.
- [ ] Create time/cost code and finance/customer record.
- [ ] Record the client repository/customer ID, Freshdesk company ID, contract ID and finance ID in the account page/global minimum portfolio index.

**Evidence:** linked client index, successful separation test and named record owner.

## Phase 2 — kickoff and operating discovery

- [ ] Hold kickoff with executive sponsor and operational, access/security and finance owners.
- [ ] Confirm outcome, in-scope products/users, supported uses, exclusions and human-accountability boundary.
- [ ] Confirm customer and Dirtyworks.ai responsibility matrix, approval authorities and escalation contacts.
- [ ] Confirm launch cohort, locations, time zone, accessibility/language needs and important business dates.
- [ ] Confirm current joiner/mover/leaver process and identity/MSP seam.
- [ ] Confirm support intake, priority examples, hours, response targets and vendor/customer-delay treatment.
- [ ] Confirm training audience, administrator session, user session, attendance ownership and materials.
- [ ] Confirm monthly report recipients and cost/usage evidence sources.
- [ ] Record every variance from the signed scope as clarification, accepted assumption or change request.

**Evidence:** kickoff record, responsibility matrix, contact map, scope confirmation and open-actions list.

## Phase 3 — product, licence and cost baseline

For every product:

- [ ] Record vendor, seller of record, plan/SKU, tenant/account ID and authoritative admin URL.
- [ ] Record customer owner, Dirtyworks.ai service owner and vendor/MSP support path.
- [ ] Record purchased quantity, assigned users, administrators and how active/used status is defined.
- [ ] Record unit/usage price, currency, tax treatment, billing period, invoice source and finance mapping.
- [ ] Record contract/effective date, renewal type/date, notice period, cancellation path and price-review date.
- [ ] Record vendor data-use/training setting, location, retention, subprocessors and export/deletion capability where material.
- [ ] Capture baseline invoice/export with collection date and source link.
- [ ] Explain that the monthly consolidated cost statement reconciles source evidence but is not the customer's vendor invoice or a guaranteed real-time view.

**Manual first-customer method:** reconcile vendor admin/export and issued invoice to the published Markdown product/cost record once per month. Add accounting/AP evidence only with customer authorization and the approved repository/source-retention policy. Do not require Plaid or a SaaS-management platform for launch.

**Evidence:** complete product/cost register and baseline reconciliation with variances explained.

## Phase 4 — privileged access and security

- [ ] Customer creates named delegated admin/operator account; shared credentials require documented exception and remediation date.
- [ ] Apply least privilege, MFA and customer-approved recovery/escalation path.
- [ ] Record who approved access, purpose, scope, creation date, review date and revocation owner.
- [ ] Store credential/token only in 1Password; store its item reference and role scope in Markdown.
- [ ] Confirm customer information will not be copied to local notes, public AI tools or unapproved systems.
- [ ] Test audit log, support impersonation/delegation rules, safe suspension and account revocation.
- [ ] Test one normal user, one administrator and one unauthorized path.
- [ ] Record vendor limitations and compensating controls.

**Gate:** any permission leakage, unresolved shared privileged access, missing MFA where available or inability to revoke is a no-go unless formally risk-accepted within contract/insurance limits.

## Phase 5 — configure and verify products

- [ ] Preserve the customer's existing configuration baseline before changes.
- [ ] Apply only signed-scope settings using change/approval records.
- [ ] Configure identity, domains, roles/groups, data-use controls, retention and sharing settings as supported.
- [ ] Configure budget/usage alerts and administrative notifications where available.
- [ ] Configure approved integrations/connectors only after separate permission and data-flow review.
- [ ] Run product-specific functional, access, export, support and rollback tests.
- [ ] Verify actual state against the change request; retain native evidence.
- [ ] Publish the verified Markdown fact/runbook update through the approved review path with the native evidence and last-verified date.

**Evidence:** configuration baseline, approved change, test result, native verification and exception list.

## Phase 6 — users, training and acceptable operation

- [ ] Receive customer-approved user roster through a controlled method.
- [ ] Reconcile purchased, assigned and planned licences before provisioning.
- [ ] Provision named users and groups; record exceptions and failed invitations.
- [ ] Administrator training covers roles, JML, audit, cost/usage, vendor support, incidents and offboarding.
- [ ] User training covers approved jobs, prohibited data/use, limitations, verification, feedback and help.
- [ ] Customer confirms who owns attendance and policy acknowledgement.
- [ ] Publish customer-approved Freshdesk knowledge articles and quick-start material.
- [ ] Record session date, material version, attendees/completion and follow-up needs without excessive employee monitoring.

**Evidence:** reconciled roster, training record, published material version and unresolved user actions.

## Phase 7 — support and incident readiness

- [ ] Customer submits a test Freshdesk request from the approved channel.
- [ ] Assignment, acknowledgement, priority, internal note, customer reply, resolution and closure work end to end.
- [ ] Test vendor escalation and link the vendor case to the Freshdesk ticket.
- [ ] Run a P1 tabletop: unauthorized disclosure, unsafe output or broad critical outage.
- [ ] Confirm Dirtyworks.ai and customer containment, notification, evidence and decision owners.
- [ ] Confirm after-hours message accurately states the contracted coverage.
- [ ] Confirm secrets and sensitive diagnostic content are not copied into ticket prose.

**Evidence:** closed synthetic ticket, escalation result and P1 tabletop actions.

## Phase 8 — go-live decision

- [ ] Signed scope, contacts, product baseline, access, configuration, users, training and support records are complete.
- [ ] Critical permission/security tests pass; non-critical exceptions have owner, control and expiry.
- [ ] Customer dependencies and known vendor limitations are acknowledged.
- [ ] Rollback/suspension and offboarding path have been tested or credibly demonstrated.
- [ ] Dirtyworks.ai service owner records founder capacity and coverage for stabilization.
- [ ] Dirtyworks.ai and customer authorized owners record `GO`, `CONDITIONAL GO`, `REMEDIATE` or `NO-GO`.

**Evidence:** dated release record, approvers, tests, conditions and next checkpoint.

## Phase 9 — 30-day stabilization

- [ ] D+2: check invitations/access, support path, critical incidents and immediate confusion.
- [ ] D+5: reconcile licences, training gaps, early tickets and vendor issues.
- [ ] D+10: review repeated support, poor-fit use, cost anomalies and scope/change signals.
- [ ] Weekly: review open risks, incidents, user feedback and customer dependencies.
- [ ] Track Dirtyworks.ai time, direct cost, manual reconciliation effort, errors and exceptions by activity.
- [ ] Update Markdown runbooks only from verified fixes; link the originating Freshdesk/change record.
- [ ] Keep customer-facing communications and requests in Freshdesk, not private repository notes.

## Phase 10 — first monthly and 30-day review

- [ ] Reconcile vendor invoices/exports, purchased licences, assignments and available usage through the same cut-off date.
- [ ] Explain missing, stale, estimated or disputed values; do not create false precision.
- [ ] Report vendor cost separately from Dirtyworks.ai service invoice and explain material variance.
- [ ] Review support volume, response performance, unresolved tickets and recurring causes.
- [ ] Review training completion, adoption evidence, policy/support gaps and outcome signals.
- [ ] Review access exceptions, incidents, risks, renewals and upcoming customer/vendor actions.
- [ ] Compare actual onboarding/operating hours and direct costs to the priced assumptions.
- [ ] Agree continue, remediate, change scope, expand, reduce or offboard decision with owners and dates.
- [ ] Update this checklist and the applicable Markdown schema/templates with the first-customer learning.

**Evidence:** customer-issued review pack, meeting record, decisions, approved changes and next monthly date.

## First-customer learning record

| Measure | Planned | Actual | Learning / change |
|---|---:|---:|---|
| Onboarding elapsed business days | | | |
| Dirtyworks.ai onboarding hours | | | |
| Customer dependency hours/delay | | | |
| Products / managed users | | | |
| Manual cost-close hours | | | |
| Training preparation/delivery hours | | | |
| Tickets in first 30 days | | | |
| Configuration/access exceptions | | | |
| Direct delivery cost | | | |
| Gross-margin implication | | | |
