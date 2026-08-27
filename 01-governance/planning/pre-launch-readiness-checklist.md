# Pre-launch readiness checklist

**Version:** 0.1  
**Date:** 2026-08-26  
**Owner:** Founder  
**Status:** Working operational checklist  
**Use:** establish that Dirtyworks.ai can market the offer and then safely accept production work

This checklist deliberately has two gates. **Market launch** permits publishing, interviews, proposals and non-production demonstrations. **Production launch** permits signing a production engagement, receiving privileged access and handling customer information. A market launch may proceed while specialist production work is unfinished, provided public claims and data handling remain inside the market-launch boundary.

## How to use this checklist

- Assign one owner and due date to every unchecked blocking item.
- Store evidence at the authoritative source; put the evidence link and decision in the company record.
- Mark conditional items `N/A` only with a reason and approver.
- Record exceptions with risk owner, compensating control, expiry and approval.
- Use the more detailed [production readiness preflight](../../06-client-delivery/quality/production-readiness-preflight.md) before any customer production release.

## Gate A — market launch

### Company and offer

- [ ] Contracting entity approach and the public relationship between that entity and Dirtyworks.ai are decided.
- [ ] Business address, monitored contact address, domain ownership and signing authority are recorded.
- [ ] Initial customer profile, excluded customer/use classes and geographic scope are explicit.
- [ ] Core offer, advanced-work boundary and customer responsibilities are reflected consistently in website, deck, proposal and sales language.
- [ ] Pricing is labelled appropriately as fixed, starting at, estimate or custom; vendor licence cost and Dirtyworks.ai service fees are separated.
- [ ] Customer-direct vendor billing is the default; no resale, consolidated-invoice or partner authority is claimed without written authorization.
- [ ] Support hours, response **targets**, exclusions and emergency path are described without promising untested resolution levels.

### Marketing, privacy and outreach

- [ ] Website contains accurate company identity, contact path, privacy notice and applicable terms or disclaimers.
- [ ] Public claims have an evidence state: established fact, working method, target or hypothesis.
- [ ] No generated or stock image is presented as a customer, employee, endorsement or delivered result.
- [ ] Customer names, logos, quotes and results require written publication approval.
- [ ] Lead forms collect only necessary information and do not invite confidential, personal or production data.
- [ ] Outreach records the source, business relevance, consent/contact basis, required sender identity and suppression status.
- [ ] Unsubscribe requests can be actioned promptly and persist across tools.
- [ ] A human reviews outbound messages; automated LinkedIn actions remain disabled under the current policy.

### Sales process

- [ ] Lead intake, qualification, discovery, proposal, approval and loss/reason stages are defined.
- [ ] Qualification excludes unsupported high-impact, safety-critical, employment-decision, regulated or sensitive first uses.
- [ ] Proposal template states assumptions, customer dependencies, third-party costs, exclusions and next gate.
- [ ] No sample customer content is accepted through ordinary email, forms or public AI tools.
- [ ] A safe synthetic demonstration is available if product proof is needed before contracting.
- [ ] Pipeline, next action, owner and source can be maintained in a simple controlled register until CRM complexity is justified.

### Market-launch decision

- [ ] Founder records `GO`, `CONDITIONAL GO` or `NO-GO`, date, scope and open conditions.
- [ ] Public launch has a named person monitoring contact, privacy and support channels.

**Market-launch blockers:** false or unsupported claims; no identifiable contracting/business party; collection of sensitive data without a controlled process; unmanageable outreach consent/suppression; or a public offer that implies unsupported resale, compliance or service guarantees.

## Gate B — production launch

### Legal, finance and insurance

- [ ] Legal entity, registration, banking, accounting, tax/GST treatment and invoice process are operating.
- [ ] Canadian counsel has approved the MSA, Order Form and Data/Security/AI Schedule for the actual first scope.
- [ ] The contract records supported uses, exclusions, acceptance, customer dependencies, third-party services, change, suspension, termination and offboarding.
- [ ] Liability, indemnity, confidentiality, IP, privacy/data roles, incident cooperation, renewal and dispute positions are approved.
- [ ] Technology E&O/professional, cyber/privacy and commercial general liability requirements have been reviewed with a broker; coverage does not conflict with promises.
- [ ] Payment timing, deposit/setup fee, collections, vendor pass-through prohibition/exception and purchasing authority are defined.
- [ ] The first engagement fits available cash and half-time founder capacity under downside assumptions.

### Service definition and operating controls

- [ ] Core service catalogue states exactly what Register, Manage and Operate include and exclude.
- [ ] Supported product list and product-approval process are defined; every product has an owner and commercial pathway.
- [ ] Support priorities, response targets, hours, escalation and third-party/customer-delay treatment are defined.
- [ ] Customer onboarding, user joiner/mover/leaver, support, change, incident, access review, cost close, renewal and offboarding runbooks exist.
- [ ] Manual SaaS cost reconciliation has an owner, monthly cut-off, evidence source, currency/tax rule and variance process.
- [ ] Training materials cover permitted use, limitations, verification, data handling, help and incident reporting.
- [ ] Time, direct cost, exceptions, support volume and customer outcome can be measured per account.

### Freshdesk readiness — customer-facing service record

- [ ] Dirtyworks.ai domain, support address, branding and monitored business hours are configured.
- [ ] Companies, contacts, groups, roles and least-privilege operator access are tested.
- [ ] Priority definitions, response targets, assignment/escalation and after-hours messaging are configured.
- [ ] Ticket categories cover access, product administration, training, usage/cost, incident, change and general support.
- [ ] Customer portal and knowledge articles expose only client-approved content; cross-customer visibility is tested.
- [ ] Templates exist for acknowledgement, dependency wait, vendor escalation, resolution, incident update and closure.
- [ ] MFA/SSO, audit/report access, retention and export/recovery approach are documented.
- [ ] Synthetic request-to-resolution and P1 escalation dry runs pass.

### Markdown client repository readiness — private operating knowledge

- [ ] Internal structure follows the [Markdown client repository operating model](../../06-client-delivery/client-operations-platform/markdown-client-repository-operating-model.md) and [template pack](../../90-templates/client-operations-repository/README.md).
- [ ] One private Git-backed repository, personal-wiki workspace and derived graph/index boundary exist per synthetic client.
- [ ] Account, requirement, service, product, access, process, training, cost, risk, decision, change, incident and review templates validate.
- [ ] Every active record has an owner, source authority/evidence, classification, updated date and next review.
- [ ] Repository isolation, named roles, MFA, protected publication and operator access are tested.
- [ ] No secrets are present in Markdown, Git history, prompts, logs or graph; records link to the correct 1Password item where necessary.
- [ ] Imported-source retention and deletion rules and approved LLM provider/data classifications are documented.
- [ ] Fresh-clone recovery, readable export and customer offboarding/deletion package can be produced.
- [ ] Synthetic onboarding, monthly close, cross-client denial and offboarding dry runs pass.

### Identity, security and privacy

- [ ] 1Password business vaults, named operator accounts, MFA, recovery, emergency access and access logging are configured.
- [ ] Managed devices, patching, endpoint protection, encrypted storage and secure communications are operating.
- [ ] Customer access is named, approved, least-privilege, time-bounded where possible and promptly revocable.
- [ ] Secrets are not stored in Freshdesk, Markdown/Git, source code, prompts, graph/index state or local notes.
- [ ] Data classification, approved transfer/storage methods, retention/deletion and subprocessor records are defined.
- [ ] Incident response names containment authority, customer contacts, evidence handling and counsel/insurance escalation.
- [ ] A tabletop exercise tests unauthorized disclosure, vendor outage and lost privileged access.
- [ ] Privacy/security impact screening and specialist review triggers are defined for new uses.

### Vendor and product administration

- [ ] Customer-owned tenant and billing are the documented default.
- [ ] Vendor terms, business-plan eligibility, MSP/delegated administration, data use/training, location, retention and offboarding have been reviewed for the supported product.
- [ ] Named admin accounts, MFA, roles, logs, export and safe suspension/revocation are tested.
- [ ] Vendor support path, service-status source and escalation limitations are recorded.
- [ ] Product, purchased quantity, assigned users, billing source, renewal/cancellation dates and last verification can be recorded manually.

### Production-launch decision

- [ ] [Pre-customer acceptance checklist](../../06-client-delivery/customer-acceptance/pre-customer-acceptance-checklist.md) is ready for the actual first prospect.
- [ ] [First-customer onboarding checklist](../../06-client-delivery/onboarding/first-customer-onboarding-checklist.md) has named owners and a synthetic dry run.
- [ ] Founder records `GO`, `CONDITIONAL GO`, `PAID DISCOVERY ONLY` or `NO-GO`, date, scope, open exceptions and approvals.

**Production-launch blockers:** unsigned or unreviewed production contract; material uninsured/uncapped exposure; missing authority to access or process; unsupported prohibited use; unresolved cross-customer or permission leakage; secrets handled unsafely; no containment/offboarding path; or founder/cash capacity below the promised service obligation.

## Completion record

| Field | Value |
|---|---|
| Checklist owner | |
| Market-launch decision/date | |
| Production-launch decision/date | |
| Open conditions and owners | |
| Evidence/package link | |
| Next review date | |
