# Production readiness preflight

**Version:** 0.1  
**Date:** 2026-08-25  
**Use:** before accepting or launching any customer production scope  
**Status:** Internal control checklist; requires qualified legal, privacy, insurance, accounting, and security advice where indicated

This checklist does not establish legal compliance or certification. Its purpose is to prevent a commercial pilot from quietly outrunning the company’s contracts, insurance, security, privacy, service, and financial capability.

Use the [pre-launch readiness checklist](../../01-governance/planning/pre-launch-readiness-checklist.md) for company-level market and production gates, the [pre-customer acceptance checklist](../customer-acceptance/pre-customer-acceptance-checklist.md) for a specific opportunity, and the [first-customer onboarding checklist](../onboarding/first-customer-onboarding-checklist.md) for execution. This preflight remains the detailed production release control when customer data, knowledge sources, integrations or higher-risk use are in scope.

## 1. Company and commercial authority

- [ ] Contracting legal entity, registration, banking, tax, invoicing, and signing authority are established; record the decision in the [client contracting framework](../../09-legal-risk-and-compliance/commercial-contracts/frameworks/client-contracting-framework.md).
- [ ] Dirtyworks.ai name/domain use is consistent with the legal entity and customer contract.
- [ ] Founder authority and spend/commitment limits are documented.
- [ ] Customer credit/payment terms, deposits, milestone billing, taxes, refunds, and collections are defined.
- [ ] Production-specific costs and working capital fit the approved tranche.

## 2. Contract package — counsel review required

- [ ] Counsel has approved the business-draft [master services agreement](../../09-legal-risk-and-compliance/commercial-contracts/templates/draft-master-services-agreement.md) or a separate partner/subcontractor agreement for the actual deal.
- [ ] The [client order form](../../09-legal-risk-and-compliance/commercial-contracts/templates/draft-client-order-form.md) records managed assets, exclusions, responsibilities, customer dependencies, acceptance, commercial terms, and change rules.
- [ ] The [data, security and AI schedule](../../09-legal-risk-and-compliance/commercial-contracts/templates/draft-data-security-and-ai-schedule.md) records processing instructions, roles, locations, subprocessors, retention, deletion, assistance, incident cooperation, and implemented control status.
- [ ] Confidentiality, IP, customer-content ownership, generalized-method ownership, and licence terms.
- [ ] Service targets/levels, third-party exclusions, maintenance, suspension, support window, and force majeure.
- [ ] Warranties and explicit limitations: no perfect accuracy, legal/professional judgment, or unsupervised high-impact use.
- [ ] Liability caps, exclusions, indemnities, insurance obligations, and prohibited uses.
- [ ] Term, renewal, price change, termination, transition, portability, and deletion evidence.
- [ ] Customer approval and accountability for sources, permissions, policies, decisions, and employee use.
- [ ] For MSP delivery: prime/subcontractor role, brand/claims, customer contact, tier handoff, payment, non-solicitation, data roles, and no unsupported exclusivity.

## 3. Insurance — broker and counsel confirmation required

- [ ] Commercial general liability appropriate to customer and partner contracts.
- [ ] Technology errors and omissions / professional liability appropriate to advice, implementation, and managed operations.
- [ ] Cyber/privacy coverage addressing incident response and contractual exposure.
- [ ] Coverage territory, subcontractors, AI exclusions, data/privacy events, limits, deductibles, and retroactive dates reviewed.
- [ ] Customer/partner certificate and additional-insured requirements are supportable.
- [ ] No contract promise exceeds coverage without an approved risk decision.

## 4. Privacy and responsible-use screen

Canadian privacy regulators call for necessity/proportionality, data minimization, transparency, accountability, impact assessment, lifecycle accuracy, traceability, and human review for consequential decisions. Alberta’s OIPC advises private-sector organizations to verify PIPA compliance when using AI with personal information. [Canadian privacy commissioner guidance](https://www.priv.gc.ca/en/privacy-topics/ai-technology-and-innovation/artificial-intelligence/gd_principles_ai/) and [Alberta OIPC responsible AI comments](https://oipc.ab.ca/wp-content/uploads/2025/08/AI-Comments-from-the-OIPC-Regarding-Responsible-AI-Governance-in-Alberta-July-15-2025.pdf)

- [ ] Intended purpose and why AI/knowledge retrieval is necessary and proportionate are recorded.
- [ ] Applicable privacy laws, contractual requirements, sector duties, and customer/controller accountability are identified by qualified advisers as needed.
- [ ] Personal, confidential, privileged, regulated, safety, and high-impact data are inventoried and minimized.
- [ ] First scope excludes client/employee/candidate records and professional/employment decisions for professional-services firms unless separately approved.
- [ ] First scope excludes safety, engineering, operational-control, environmental/regulatory, and field-action decisions for energy-service firms unless separately approved.
- [ ] Collection, use, disclosure, access, logging, retention, and deletion purposes/authority are documented.
- [ ] Employee/user transparency and any monitoring/analytics implications are approved by the customer.
- [ ] Privacy or algorithmic impact assessment requirement is screened; qualified review is obtained when warranted.
- [ ] Human verification, challenge, correction, escalation, and accountability are visible for consequential outputs.

## 5. Platform and vendor due diligence

- [ ] Customer owns production tenant/accounts, licences, sources, and business data by default.
- [ ] Vendor terms permit the proposed business and MSP/subcontractor use.
- [ ] Model-training/default data-use behavior is known and acceptable.
- [ ] Data storage/processing locations, subprocessors, retention, deletion, encryption, and incident terms are recorded.
- [ ] Identity supports named accounts, MFA, least privilege, delegated administration, and prompt revocation.
- [ ] Logs, roles, connector administration, cost controls, backups/exports, and offboarding meet the use case.
- [ ] Vendor availability and changing features are not misrepresented as Dirtyworks.ai guarantees.
- [ ] A replacement/exit path and customer-readable configuration record exist.

## 6. Security baseline

- [ ] Dedicated business accounts and managed devices/profiles are used; no personal consumer accounts.
- [ ] Password manager, MFA, recovery, role separation, and joiner/mover/leaver process are operating.
- [ ] Customer access is time-bound, least-privilege, approved, logged, and reviewed.
- [ ] No shared credentials; secrets are not stored in documents, tickets, source code, or prompts.
- [ ] Customer information is not copied locally or into test tools without explicit control and purpose.
- [ ] Secure file exchange, communication, backup, patching, anti-malware/EDR, and incident contact paths are defined.
- [ ] Permission tests include representative roles and attempts to retrieve unauthorized information.
- [ ] Adversarial/prompt-injection and data-exfiltration risks are assessed proportionally to sources and actions.
- [ ] Managed workflows have approval, least privilege, audit, exception, rollback, and kill-switch controls.

## 7. Delivery readiness

- [ ] Paid review completed with proceed decision and bounded first domain.
- [ ] Executive sponsor, knowledge owner, access/security owner, and SMEs are named.
- [ ] Sources, owners, freshness, contradictions, and exclusions are recorded.
- [ ] Evaluation set covers supported, partial, unsupported, contradictory, permission, high-impact, and misuse classes.
- [ ] Critical permission tests require 100% pass; other thresholds match consequence.
- [ ] Baseline and outcome measurement do not create disproportionate employee surveillance.
- [ ] User training includes limitations, source verification, prohibited use, feedback, and incidents.
- [ ] Acceptance, launch, stabilization, monthly operations, change, and offboarding plans exist.
- [ ] Delivery hours and direct cost fit price/margin and half-time founder capacity.

## 8. Service and incident readiness

- [ ] Support intake, priorities, response targets, hours, exclusions, and customer/partner tier handoffs are documented.
- [ ] Named contacts and an alternate exist for Dirtyworks.ai, customer, MSP, and critical vendors.
- [ ] P1 containment can suspend access, connector, answer domain, or workflow safely.
- [ ] Incident record preserves timeline, scope, decisions, evidence, communications, cause, correction, and recurrence prevention.
- [ ] Privacy/security breach assessment and notification decisions remain with appropriately accountable parties and qualified counsel.
- [ ] Third-party incidents and customer delays have clear communication and SLA treatment.
- [ ] Recovery/offboarding/export steps have been tested in the selected platform.

## 9. Release decision

The release record must state:

- scope and customer;
- checklist owner and review date;
- open exceptions, risk owner, compensating control, expiry, and approval;
- legal/privacy/security/insurance specialist advice obtained;
- evaluation and permission-test evidence;
- go, conditional go, remediate, or no-go decision;
- signer for Dirtyworks.ai and customer/prime MSP.

Any unresolved permission leakage, prohibited data/use, missing accountable owner, uninsured/uncapped material exposure, unsupported contract promise, or inability to suspend/offboard is a no-go condition.
