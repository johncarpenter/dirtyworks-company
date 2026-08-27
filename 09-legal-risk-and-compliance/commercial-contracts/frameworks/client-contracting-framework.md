# Dirtyworks.ai client contracting framework

**Version:** 0.1  
**Date:** 2026-08-25  
**Status:** Internal working framework; requires Alberta/Canadian counsel before use  
**Jurisdiction assumption:** Alberta-based provider contracting primarily with Canadian private-sector SMBs  
**Not legal advice:** This document and the linked drafts are business instructions for qualified counsel. They are not approved legal documents and must not be signed or presented as counsel-reviewed terms.

## Executive direction

Dirtyworks.ai should use a modular contract stack rather than a single proposal containing every legal and technical term:

```text
Master Services Agreement (stable legal/commercial rules)
        ↓
Order Form / Statement of Work (customer, scope, price, timing, acceptance)
        ↓
Data, Security and AI Schedule (processing and control obligations)
        ↓
Service/Product Schedules (support, vendor portfolio, workflows, MSP seam)
```

The agreement must make operational responsibility visible. It should not attempt to shift every risk to the customer, guarantee results that depend on customer data and third-party products, or promise controls Dirtyworks.ai cannot yet demonstrate.

## Initial contract set

1. [Draft Master Services Agreement](../templates/draft-master-services-agreement.md) — stable relationship terms.
2. [Draft Client Order Form](../templates/draft-client-order-form.md) — review, launch, recurring, and expansion scope.
3. [Draft Data, Security and AI Schedule](../templates/draft-data-security-and-ai-schedule.md) — processing instructions, security baseline, incidents, subprocessors, data lifecycle, and AI-specific controls.
4. Future MSP Partner Agreement/Addendum — referral, co-managed, or white-label commercial and responsibility terms; do not adapt the client MSA by simply changing party names.
5. Future public website terms/privacy notice — separate from negotiated client contracts.

## Contract hierarchy

Counsel should approve an order of precedence. Working order:

1. a signed amendment expressly identifying what it changes;
2. the applicable Order Form/SOW for scope, price, timing, acceptance, and expressly identified commercial deviations;
3. the Data, Security and AI Schedule for personal information, security, incident, subprocessor, and AI-data terms;
4. a service/product schedule for its stated subject;
5. the MSA;
6. proposals, websites, presentations, emails, or purchase orders only when expressly incorporated.

Customer purchase-order boilerplate should not modify the agreement merely because a PO is issued or accepted for administration.

## What belongs where

| Subject | MSA | Order/SOW | Data/Security/AI Schedule | Product/service schedule |
|---|---:|---:|---:|---:|
| Legal parties, confidentiality, IP, liability, disputes | Primary | deviations only | privacy/security-specific allocation | no |
| Offer, users, sources, permissions, workflows | reference | Primary | processing detail | optional detail |
| Fees, milestones, term, renewal | framework | Primary | no | possible vendor charges |
| Acceptance tests and customer dependencies | framework | Primary | security/privacy gates | product tests |
| Privacy roles and instructions | incorporate | processing summary | Primary | vendor specifics |
| Security controls and incident cooperation | incorporate | risk-specific additions | Primary | vendor specifics |
| Support priorities and windows | general | Primary | incident-specific | detailed SLA if needed |
| Third-party products, billing, resale and exit | allocation | selected products/path | subprocessor/data treatment | Primary register |
| AI intended use, prohibited use, human review | general | Primary | Primary data safeguards | product capability limits |
| Offboarding | general rights | deliverables/timing/fees | return/deletion | product export/cancellation |

## Primary legal and compliance perimeter

### Alberta private-sector customers

Alberta's Personal Information Protection Act (PIPA) is the provincial private-sector privacy law. It generally applies to provincially regulated Alberta businesses that collect, use, or disclose personal information. Federally regulated organizations and some interprovincial or international processing may bring federal PIPEDA into scope; sector, province, data subject, and activity must be assessed per customer. [Government of Alberta PIPA overview](https://www.alberta.ca/personal-information-protection-act), [OPC provincial/federal overview](https://www.priv.gc.ca/en/about-the-opc/what-we-do/provincial-and-territorial-collaboration/provincial-and-territorial-privacy-laws-and-oversight/)

PIPEDA's accountability principle states that an organization remains responsible for personal information transferred to a third party for processing and should use contractual or other means to provide comparable protection. The contract therefore cannot tell the customer that outsourcing transfers all privacy accountability to Dirtyworks.ai. [OPC accountability interpretation](https://www.priv.gc.ca/en/privacy-topics/privacy-laws-in-canada/the-personal-information-protection-and-electronic-documents-act-pipeda/pipeda-compliance-help/pipeda-interpretation-bulletins/interpretations_02_acc/)

### Public-sector and health customers

Alberta public bodies are governed by the Protection of Privacy Act (POPA), which came into force June 11, 2025 and has additional PIA, privacy-management, data, and contracting implications. Health custodians may be governed by the Health Information Act. These are not initial standard-form customers. Use a separately reviewed public-sector or health-sector addendum and procurement/security response. [Alberta POPA overview](https://oipc.ab.ca/legislation/popa/), [Alberta privacy laws](https://oipc.ab.ca/resource/privacy-laws-in-alberta/)

### Privacy impact assessments

PIPA does not generally require a private-sector organization to submit a PIA, but Alberta's OIPC recommends PIAs as a risk-management practice where electronic systems or practices process personal information. Dirtyworks.ai should offer factual cooperation without promising legal adequacy or regulator acceptance. [Alberta OIPC PIA guidance](https://oipc.ab.ca/privacy-impact-assessments/)

### Breach notification

Under Alberta PIPA, an organization with personal information under its control must notify the Commissioner without unreasonable delay when a reasonable person would consider that a breach creates a real risk of significant harm. The customer and Dirtyworks.ai need an incident-notice and cooperation seam, but the contract should not casually assign statutory notification decisions to a service provider that may lack the full facts or legal role. [Alberta OIPC breach guidance](https://oipc.ab.ca/breach-notification/)

### Cross-border processing

Canadian privacy law does not universally prohibit processing outside Canada, but the accountable organization must assess safeguards, transparency, foreign-law access, and contractual controls. Alberta PIPA has specific policy/notice considerations for service providers outside Canada. Each Order should identify known processing locations and subprocessors rather than promise “Canadian data residency” by default. [OPC outsourcing guidance](https://www.priv.gc.ca/en/privacy-topics/employers-and-employees/outsourcing/02_05_d_57_os_01/), [Alberta OIPC foreign-service-provider finding](https://oipc.ab.ca/p2010-ir-02/)

### AI-specific law and guidance

Bill C-27, which contained the proposed Artificial Intelligence and Data Act, did not complete committee stage in the 44th Parliament; the relevant ISED AIDA page is archived. Do not contract as though AIDA is currently a certification regime. Existing privacy, human-rights, employment, professional, intellectual-property, competition, consumer, contract, sector, and safety laws still apply. Canada's voluntary generative-AI code and privacy-commissioner principles are useful governance inputs, not a substitute for applicable law. [Parliament Bill C-27 record](https://www.parl.ca/legisinfo/en/bill/44-1/c-27), [ISED voluntary code](https://ised-isde.canada.ca/site/ised/en/voluntary-code-conduct-responsible-development-and-management-advanced-generative-ai-systems), [Canadian privacy regulators' generative-AI principles](https://www.priv.gc.ca/en/privacy-topics/technology/artificial-intelligence/gd_principles_ai)

### Electronic contracting

Alberta's Electronic Transactions Act provides legal recognition for electronic records and supports electronic contracting/signatures subject to its conditions and exclusions. Counsel should confirm execution mechanics, notice addresses, counterparts, and any excluded document types. [Government of Alberta legislation description](https://www.alberta.ca/lookup/imt-policy-tools-portal.aspx)

## Business principles the agreement must preserve

1. **Customer ownership by default.** Customer owns its tenant, accounts, source information, access decisions, and business truth.
2. **Dirtyworks.ai owns its method.** Pre-existing tools, generalized templates, evaluation methods, know-how, and improvements remain Dirtyworks.ai property; paid customer-specific deliverables receive the agreed ownership or licence.
3. **One bounded scope.** Every Order lists the supported business domain, users, sources, permission groups, products, workflows, and excluded use.
4. **Human accountability.** AI outputs assist; the customer remains responsible for business, professional, employment, safety, engineering, legal, accounting, tax, regulatory, and other consequential decisions.
5. **No invisible vendor risk.** Product owner, contract/billing path, data terms, locations, subprocessor role, usage exposure, renewal, support, and exit are recorded.
6. **No unsupported resale.** Customer-direct subscriptions are default. Resale, referral, marketplace, or bundled supply applies only when an Order identifies valid authorization and seller-of-record duties.
7. **No perfect-performance promise.** Acceptance is by agreed tests and supported question classes; response targets are not resolution guarantees; third-party uptime is not Dirtyworks.ai uptime.
8. **Customer dependencies matter.** Source accuracy, lawful authority, permissions, stakeholder availability, approvals, user behaviour, and customer systems affect delivery and dates.
9. **Exit is designed.** Data, configurations, records, access revocation, subscriptions, transition work, retention, and deletion evidence are defined before launch.
10. **Risk follows control.** A party should not accept unlimited exposure for facts, systems, decisions, or third parties it cannot control.

## Essential clause map

| Clause | What it must resolve | Dirtyworks.ai issue |
|---|---|---|
| Parties and authority | correct legal names, addresses, signing authority | Dirtyworks.ai legal entity is not yet recorded |
| Agreement documents/precedence | which document wins | prevent proposal/PO/web copy conflict |
| Services and Orders | no work outside signed scope | separate review, launch, operations, expansions |
| Customer responsibilities | access, authority, truth, approvals, users | source/permission failures cannot become provider warranties |
| Change control | scope/date/fee/risk effects | prevent “small AI request” from becoming unlimited development |
| Fees/taxes/expenses | CAD, GST, deposits, milestones, late/suspension | preserve review in advance and launch milestones |
| Third-party products | customer/vendor/Dirtyworks roles and pass-through terms | no assumed reseller rights or upstream guarantees |
| Access and credentials | delegated access, MFA, least privilege, no shared passwords | required for managed operations |
| Confidentiality | two-way protection, exclusions, compelled disclosure, duration | protect customer data and Dirtyworks methods |
| Privacy/data processing | roles, instructions, purposes, laws, requests | use separate schedule |
| Security | stated controls, customer controls, changes, evidence | do not claim ISO/SOC certification unless obtained |
| Incident cooperation | definition, reporting trigger/time, containment, evidence, notification decisions | align contract with achievable response process |
| Customer data | ownership, permitted processing, return/deletion | no generalized training without express agreement |
| IP/deliverables | background IP, customer-specific deliverables, feedback, AI output uncertainty | avoid assigning reusable operating method |
| AI use | intended use, limitations, human review, prohibited use, model/vendor changes | core differentiation and risk boundary |
| Warranties | authority, professional performance standard, material conformity | avoid perfect accuracy/availability/security/compliance promises |
| Disclaimers | AI variability, customer data, third parties, professional advice | conspicuous and consistent with general impression |
| Suspension | security, illegal use, risk, non-payment | safe kill switch with notice where practicable |
| Term/renewal | project versus six-month recurring term, renewal and price changes | align with offer model |
| Termination | cause, insolvency, convenience options, accrued fees | preserve committed capacity and customer exit |
| Transition | exports, access removal, deletion, paid assistance | avoid hostage dynamics and unlimited free transition |
| Indemnity | third-party IP, customer data/instructions/use, misconduct | match control and insurance |
| Liability | direct damages, exclusions, caps, supercaps, carve-outs | sponsor/counsel decision; match insurance and pricing |
| Insurance | CGL, technology E&O, cyber/privacy, proof | coverage must exist before promise |
| Publicity | logos, case studies, quotes, generated imagery | opt-in only |
| Disputes/governing law | Alberta courts, mediation/arbitration option | keep process accessible and proportionate |
| General | assignment, subcontractors, force majeure, notices, survival, amendments | preserve operational flexibility without hidden responsibility |

## Risk allocation decisions

### Liability cap

The draft preserves alternatives for counsel. Do not choose by habit.

| Option | Mechanism | Benefit | Constraint |
|---|---|---|---|
| A — affected Order fees | cap at fees paid/payable under the affected Order in prior 12 months | strongest provider protection; aligns with small engagements | may be unacceptable for security/privacy-heavy customers and too low early in term |
| B — greater-of floor | greater of prior-12-month fees and $50,000 or insured amount | credible minimum recovery | exposure may exceed revenue and deductible/cash capacity |
| C — base cap plus supercap | base cap for general claims; 2×/3× or fixed supercap for confidentiality, privacy/security, or IP indemnity | differentiates ordinary and sensitive risk | more negotiation and aggregation complexity |
| D — uncapped categories | fraud, wilful misconduct and liabilities that law does not permit limiting | expected carve-out | counsel must prevent broad wording from swallowing the cap |

The commercial price, risk class, insurance, product control, data sensitivity, and customer contribution should determine the result. A $2,500 review should not silently carry enterprise-scale exposure.

### Indemnity

Possible balanced structure:

- Dirtyworks.ai defends third-party claims that paid Dirtyworks.ai-created deliverables, when used as authorized, infringe Canadian IP rights; remedies may include modification, replacement, rights procurement, or termination/refund for the affected deliverable.
- Customer defends third-party claims arising from Customer Data, customer instructions, unlawful collection/use, excluded/high-risk use, customer decisions, customer-selected materials, or combination/modification outside scope.
- Security/privacy claims should be allocated based on each party's breach of its schedule obligations, not a blanket provider indemnity for every incident in a customer-owned environment.
- Exclusions, notice, control of defence, cooperation, settlement consent, cap treatment, and insurance alignment require counsel.

### Dispute resolution

| Option | Benefit | Constraint |
|---|---|---|
| Alberta courts after executive negotiation | simple, transparent, preserves urgent remedies | public and potentially expensive |
| negotiation → mediation → Alberta courts | encourages commercial resolution without blocking court access | mediation adds step/time |
| negotiation → proportionate Alberta arbitration | private and potentially specialized | fees and procedure can be disproportionate for small claims; clause must remain realistically accessible |

The draft uses executive negotiation followed by Alberta courts as the simplest working option, with optional mediation. Counsel may recommend arbitration for larger enterprise/MSP agreements. Standard terms should avoid inaccessible foreign forums or excessive upfront costs.

## AI-specific contract rules

### Intended and excluded uses

Each Order must state:

- intended users and business purpose;
- supported question/domain classes;
- information and systems permitted;
- decisions or actions that remain human;
- prohibited sensitive/high-impact uses;
- verification, abstention, escalation, approval, and rollback rules;
- whether any output may trigger a system action.

Initial standard exclusion should cover autonomous or authoritative health, legal, tax/accounting, employment, credit, eligibility, safety, engineering, environmental/regulatory, control-system, surveillance, biometric, or other material decisions unless separately risk-assessed, insured, reviewed by specialists, and expressly ordered.

### Accuracy and acceptance

The contract should not say “AI may be wrong” and stop there. It should define the positive operating mechanism:

- representative evaluation set by supported question class;
- source visibility/verification requirements;
- contradiction and unsupported-question behaviour;
- critical permission tests;
- human approval for consequential work;
- documented thresholds and release decision;
- regression tests and change treatment.

### Customer data and model training

Working position:

- Dirtyworks.ai does not use Customer Data to train a generalized Dirtyworks.ai model without express written agreement.
- Third-party product training/retention follows the disclosed product terms and selected settings.
- If no configuration can meet the approved data-use requirement, the product is not activated or the customer explicitly approves a lawful alternative after disclosure.
- Anonymized/aggregated operational learning is used only when contractual, technical, and legal conditions prevent re-identification and unauthorized disclosure; customer case-study use remains separate opt-in.

### AI outputs and IP

Do not guarantee that AI-generated material is unique, non-infringing, copyright-protected, or suitable for an authoritative decision. The Order should identify whether outputs are drafts, operational records, customer deliverables, or reusable method assets. Customer-specific paid deliverables can be assigned or licensed to the customer while Dirtyworks.ai retains background methods and generalized know-how.

## Commercial mechanics by offer

| Offer | Contract form | Payment | Acceptance/exit |
|---|---|---|---|
| Knowledge Reliability Review | MSA + short Order | 100% in advance | delivery of map/readout; outcome may be proceed, remediate, simpler solution, or stop |
| Managed Knowledge Launch | MSA + detailed Order + schedules | 50/40/10 working milestones | permission/evaluation/source/training/operations tests; 30-day stabilization |
| Knowledge Operations | MSA + recurring Order + schedules | monthly in advance; six-month working initial term | ongoing controls/response targets; renewal/termination/transition |
| Product portfolio management | Order + product register | separate vendor/pass-through and service charges | authorization, user/account, renewal, support, cost and exit records |
| Workflow expansion | new/change Order | fixed milestone or scoped recurring change | risk/rollback/approval/acceptance specific to action |

## Negotiation positions

### Normally hold

- bounded scope and change control;
- customer responsibility for source truth, lawful authority, permissions, and decisions;
- no perfect accuracy, security, compliance, outcome, or third-party uptime guarantee;
- customer-owned tenant/data/accounts by default;
- no hidden vendor/reseller commitment;
- human review for consequential use;
- right to suspend unsafe, unlawful, unauthorized, or insecure use;
- liability proportionate to fees, control, and insurance;
- paid transition outside included offboarding;
- no logo/case-study rights without express approval in either direction.

### Can vary by price and risk

- liability cap/supercap;
- incident notice target;
- audit evidence and frequency;
- support window/response targets;
- data residency and approved subprocessors;
- ownership versus licence for custom deliverables;
- convenience termination and minimum commitment;
- insurance limits;
- mediation/arbitration;
- escrow, source transfer, or enhanced transition for custom components.

### Decline or separately price

- unlimited liability unrelated to Dirtyworks.ai control;
- uncapped consequential/lost-profit exposure;
- perfect security/accuracy/compliance or guaranteed ROI;
- all-law compliance warranties for the customer's business or data;
- customer audit access to other customers' information or systems;
- unrestricted penetration testing;
- provider responsibility for customer, MSP, or upstream-vendor systems;
- silent acceptance of customer PO terms;
- free unlimited transition or perpetual support;
- broad work-made-for-hire/assignment that captures background methods and tools;
- exclusivity, most-favoured pricing, or partner non-compete without committed economics;
- unsupported data residency or subprocessor pre-approval that upstream vendors cannot meet.

## Pre-signature decision register

| ID | Decision | Options | Required before |
|---|---|---|---|
| L-001 | Contracting legal entity | Alberta corporation; sole proprietor/trade name; other | any external contract |
| L-002 | Registered/legal and notice addresses | physical/mailing plus contract email | any external contract |
| L-003 | Insurance programme | CGL; technology E&O; cyber/privacy; limits/deductibles/territory | production promise and liability decision |
| L-004 | Base liability architecture | Order-fee cap; greater-of floor; cap + supercap | counsel finalizes MSA |
| L-005 | Dispute path | Alberta courts; mediation then courts; arbitration | counsel finalizes MSA |
| L-006 | Incident initial-notice commitment | without undue delay with 24h, 48h, or contract-specific maximum | security schedule and incident runbook |
| L-007 | Default recurring renewal | fixed six months then monthly; auto-renew term; new order at expiry | recurring Order |
| L-008 | Data location posture | disclosed multi-region; Canada-only where available; use-case-specific | vendor selection and DPA |
| L-009 | Deliverable IP posture | assignment after payment; perpetual customer licence; per-deliverable | first Order |
| L-010 | Privacy/security accountable contacts | named Dirtyworks.ai privacy/security lead(s) | production access |
| L-011 | First-customer risk class | low-risk internal knowledge only; broader confidential commercial data | first Order and insurance review |
| L-012 | Contract execution system | approved e-sign platform and retention/export process | sending first agreement |

## Counsel review brief

Ask Alberta/Canadian technology counsel to:

1. confirm legal entity, trade-name, GST, authority, and execution blocks;
2. identify PIPA/PIPEDA and any sector/province/customer-specific application;
3. redraft rather than merely “approve” privacy roles and statutory-notification allocation;
4. test MSA/Schedule/Order precedence and purchase-order exclusion;
5. align warranties, disclaimers, indemnities, exclusions, caps, and insurance;
6. review AI-output, IP, open-source, vendor, and customer-data clauses;
7. assess employment, professional, safety, human-rights, and automated-decision exclusions;
8. confirm electronic signature, notices, governing law, dispute, limitation-period, and survival terms;
9. create separate partner/referral/co-managed/white-label terms;
10. identify Quebec, BC, public-sector, health, cross-border, or enterprise addenda when a customer requires them;
11. produce a clean signature version and a clause playbook showing fallback positions;
12. confirm whether the privacy/security schedule should be a DPA, service-provider schedule, or both for the initial customer set.

## Sources and status notes

Primary sources were checked on 2026-08-25. Laws and guidance can change; counsel must re-check before use.

- [Alberta PIPA overview](https://www.alberta.ca/personal-information-protection-act)
- [Alberta OIPC privacy laws](https://oipc.ab.ca/resource/privacy-laws-in-alberta/)
- [Alberta OIPC breach notification](https://oipc.ab.ca/breach-notification/)
- [Alberta OIPC PIA guidance](https://oipc.ab.ca/privacy-impact-assessments/)
- [Federal PIPEDA, current official text](https://laws-lois.justice.gc.ca/eng/acts/P-8.6/index.html)
- [OPC accountability interpretation](https://www.priv.gc.ca/en/privacy-topics/privacy-laws-in-canada/the-personal-information-protection-and-electronic-documents-act-pipeda/pipeda-compliance-help/pipeda-interpretation-bulletins/interpretations_02_acc/)
- [OPC outsourcing guidance](https://www.priv.gc.ca/en/privacy-topics/employers-and-employees/outsourcing/02_05_d_57_os_01/)
- [Canadian privacy regulators' generative-AI principles](https://www.priv.gc.ca/en/privacy-topics/technology/artificial-intelligence/gd_principles_ai)
- [ISED voluntary generative-AI code](https://ised-isde.canada.ca/site/ised/en/voluntary-code-conduct-responsible-development-and-management-advanced-generative-ai-systems)
- [Canadian Centre for Cyber Security SMB baseline controls](https://www.cyber.gc.ca/en/guidance/baseline-cyber-security-controls-small-and-medium-organizations)
- [Parliament of Canada Bill C-27 record](https://www.parl.ca/legisinfo/en/bill/44-1/c-27)

