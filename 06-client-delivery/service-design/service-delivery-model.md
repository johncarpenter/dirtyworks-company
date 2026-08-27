# Service delivery operating model

**Version:** 0.1  
**Date:** 2026-08-25  
**Status:** Reference process; validate through first two production accounts

## Operating promise

Dirty Works operates a defined set of company knowledge and AI assets so approved users can obtain useful, verifiable answers and the customer can see quality, risk, use, and improvement opportunities over time.

Dirty Works owns the service process. The customer remains accountable for its policies, source truth, business decisions, access approvals, employee use, and compliance obligations.

## Service boundary

```text
Customer owns                         Dirty Works operates
──────────────────────────────────    ──────────────────────────────────
Business policy and source truth      Configured knowledge/AI service
System and data ownership             Managed connectors and settings
User/employment decisions             Evaluation and regression testing
Legal and regulatory accountability   Monitoring, support and reporting
Access approval                       Change and incident process
Final high-impact judgment            Adoption and improvement cadence
```

Traditional MSPs may own identity, endpoint, network, backup, cybersecurity, and tenant-wide administration. Dirty Works’ responsibility begins at the explicitly managed knowledge/AI configuration. Integration seams and escalation paths must be written per customer.

## Customer lifecycle

### 0. Qualification

**Inputs:** problem event, ICP data, sponsor, source hypothesis, risk screen.  
**Output:** reject, nurture, or paid-review proposal.  
**Control:** no sensitive sample data accepted through informal email or public AI tools.

### 1. Knowledge Reliability Review

**Activities:** map the question domain, people, sources, owners, permissions, baseline, failure consequences, and platform options. Create a representative evaluation set and classify risk.

**Gate:** proceed only when the source base, business value, ownership, and risk support a bounded launch.

### 2. Contract and launch planning

Record:

- managed assets and excluded assets;
- tenant/account ownership;
- data types, locations, subprocessors, retention, and deletion;
- users and permission groups;
- roles and customer dependencies;
- evaluation and acceptance criteria;
- support window and incident priorities;
- third-party costs and vendor limitations;
- change, suspension, termination, and offboarding terms.

Legal counsel must review production contract templates before the first customer signature. Dirty Works documentation is not legal advice.

### 3. Configure and evaluate

1. Inventory exact sources and owners.
2. Classify content and remove sources outside scope.
3. Establish least-privilege access.
4. Configure the customer-owned platform and connectors.
5. Run retrieval, answer, citation, contradiction, abstention, and permission tests.
6. Record failures by class and remediate source, configuration, prompt, or scope.
7. Repeat until acceptance thresholds and critical controls pass.

Do not average away a critical failure. Permission leakage and materially unsafe answers are release blockers even when the aggregate score is high.

### 4. Launch and stabilize

- Train users on supported questions, source verification, feedback, and escalation.
- Train administrators/owners on access, source updates, and incident reporting.
- Roll out to a small cohort before the full bounded group.
- Review telemetry and feedback at least weekly for 30 days.
- Hold a 30-day value and acceptance review.

### 5. Operate

Run the recurring controls described below. Maintain the customer record, service inventory, access map, evaluation set, change log, incident log, source-owner register, risk register, and offboarding package. The [client operations platform investigation](../client-operations-platform/client-operations-platform-investigation.md) defines systems of record, relationships, support workflows and the staged buy/configure/build approach.

### 6. Improve and expand

Classify observed gaps:

1. existing answer available;
2. source missing/stale/contradictory;
3. data belongs in a structured system;
4. AI can assist a person;
5. workflow can act with defined controls;
6. remain manual by design.

Only categories 4 and 5 are automation candidates. Each requires its own value, risk, exception, and operating analysis.

### 7. Offboard

- disable Dirty Works access;
- provide current configuration, inventories, runbooks, evaluation set, and change history in portable form;
- transfer or remove managed credentials;
- verify deletion/retention obligations;
- identify customer actions and vendor subscriptions;
- record completion and residual risk.

## Roles and accountability

| Role | Dirty Works responsibility | Customer responsibility |
|---|---|---|
| Executive sponsor | Value review, escalation, roadmap facilitation | Priority, budget, policy, conflict resolution |
| Knowledge owner | Facilitate source operations and gap backlog | Approve truth, freshness, contradictions, and changes |
| Access/security owner | Propose and test configuration | Approve identities, groups, access, and security exceptions |
| Users | Training, support, feedback path | Use within policy, verify sources, report problems |
| AI operations lead | Day-to-day service accountability | Named operational contact and timely dependencies |
| Subject-matter expert | Evaluation facilitation | Provide and approve representative questions/answers |

One person may hold multiple roles in a smaller customer, but no role may silently disappear.

## Recurring control cadence

| Frequency | Control |
|---|---|
| Continuous/alerted | Service availability, connector failures, material cost anomalies, reported incidents |
| Weekly during stabilization | New failures, permission issues, unanswered questions, user feedback, adoption blockers |
| Monthly | Evaluation regression sample, source freshness, open risks/incidents, usage, direct cost, value scorecard, change allowance |
| Quarterly | Full permission sample, owner review, vendor/subprocessor change, retention review, roadmap and service-fit review |
| Annual or material change | Risk assessment, contract/SLA fit, recovery/offboarding test, security/privacy specialist review as required |

The cadence is adjusted by risk. A source with high change rate or consequence needs more frequent evaluation.

## Quality model

Evaluate by question class rather than one accuracy number:

- **supported answer:** correct enough for the intended job and backed by relevant approved sources;
- **partial answer:** useful but incomplete, with limitations visible;
- **unsupported:** system should abstain or escalate;
- **contradictory sources:** system identifies conflict rather than selecting silently;
- **permission boundary:** user receives only authorized information;
- **high-impact:** requires explicit source verification and human decision;
- **adversarial/misuse:** attempts to override controls or extract unauthorized data.

Initial launch thresholds are set per customer. Critical permission tests require 100% pass. Targets for other classes must reflect consequence; a low-risk directory question and a safety instruction cannot share one threshold.

## Service levels

Use service targets until operational data supports contractual commitments.

| Priority | Example | Initial response target in support window | Operating action |
|---|---|---:|---|
| P1 Critical | Confirmed unauthorized disclosure, harmful action, or broad outage of a critical managed workflow | 1 business hour | Contain/suspend, notify designated customer contact, preserve evidence, coordinate incident process |
| P2 High | Materially wrong answer in an important supported class; source or connector unavailable for many users | 4 business hours | Triage, workaround/scope warning, remediation plan |
| P3 Normal | Individual access issue, wrong/poor answer with limited consequence, standard support request | 1 business day | Queue, investigate, update record |
| P4 Change | New source, prompt, report, training, or enhancement | 2 business days to acknowledge/plan | Schedule within allowance or quote change |

Response is not resolution. Third-party availability and customer-delayed dependencies must be excluded from resolution commitments.

## Security, privacy, and responsible-use baseline

Before production:

- identify the legal entity, accountable customer owner, intended purpose, and affected people;
- minimize personal and sensitive information;
- record data locations, subprocessors, retention, model-training terms, and customer ownership;
- use dedicated business/enterprise accounts, MFA, least privilege, and delegated access;
- prohibit shared credentials and local copies of customer content unless specifically controlled;
- test source and result permissions with representative roles;
- define logs, access to logs, employee transparency, and retention;
- define human review and challenge paths for consequential use;
- maintain an incident and breach-escalation process;
- complete proportional privacy/security/risk review and obtain specialists when required;
- preserve a kill switch or safe suspension path for managed actions.

Dirty Works should align its practical controls to NIST AI RMF concepts and Canadian/Alberta privacy guidance, but must not claim certification or legal compliance it has not independently established.

## Platform selection

Select the smallest platform that meets the job and control requirements.

| Criterion | Questions |
|---|---|
| Existing fit | Is the customer already standardized on Microsoft, Google, OpenAI, or a knowledge platform? |
| Access | Are source permissions preserved and testable? |
| Quality | Are citations, abstention, retrieval controls, and evaluations supportable? |
| Administration | Are identity, logs, roles, retention, and connector controls adequate? |
| Data | What is stored, where, for how long, and used for what? |
| Portability | Can the customer retain sources, configs, and operating records on exit? |
| Cost | Are licences and variable use understandable and controllable? |
| Workflow | Does the platform support required human approvals, exceptions, and auditability? |

Default sequence: native incumbent capability → configured cross-platform product → low-code integration → custom component. Move right only when the previous option fails a documented requirement.

## Delivery records required per customer

- account charter and contacts;
- signed scope/service schedule;
- managed asset and connector inventory;
- data and source register;
- permission map and test evidence;
- evaluation set, results, and release decisions;
- customer approvals and training record;
- risk, incident, problem, and change logs;
- value baseline and recurring scorecard;
- vendor/licence/cost record;
- current runbook and offboarding package.

These records are product assets. If they are missing, the service is not fully delivered even when the interface works.

The initial private operating records and runbooks follow the [Markdown client repository operating model](../client-operations-platform/markdown-client-repository-operating-model.md), with one private repository per customer; customer requests and communications remain in Freshdesk. The [pre-customer acceptance checklist](../customer-acceptance/pre-customer-acceptance-checklist.md) and [first-customer onboarding checklist](../onboarding/first-customer-onboarding-checklist.md) define the first operating gates. A proprietary [AI Operations Ledger](../../03-offers-and-products/product-strategy/ai-operations-ledger-concept.md) remains deferred until repeated client work meets its activation test.
