# DRAFT — Data, Security and AI Schedule

**NOT FOR SIGNATURE — BUSINESS DRAFT FOR QUALIFIED PRIVACY/TECHNOLOGY COUNSEL AND SECURITY REVIEW**  
**Version:** 0.1  
**Date:** 2026-08-25  
**Applies to:** Master Services Agreement dated `[date]` and Order(s) `[IDs]`

This Schedule describes how `[Dirtyworks legal entity]` (**Dirtyworks**) processes and protects Customer Data for `[Customer legal entity]` (**Customer**). It must be completed for the actual products, locations, data, and use case. It is not a representation of controls that have not been implemented and evidenced.

## 1. Role and scope

1.1 Each Party is responsible for compliance with Applicable Law for Personal Information under its control and according to its actual role.

1.2 For Personal Information Customer provides or makes accessible for Dirtyworks to process solely on Customer's documented instructions, Customer acts as the accountable organization/controller and Dirtyworks acts as its service provider/processor, using those functional terms even where Applicable Law uses different terminology.

1.3 Dirtyworks may be independently accountable for Personal Information it collects for its own contracting, billing, security, legal, personnel, and business-administration purposes. This Schedule does not convert independently controlled information into Customer-controlled information.

1.4 If the actual processing requires joint control, independent determination of purposes, public-body, health-custodian, regulated-professional, or other statutory roles, the Parties will obtain specialist review and amend the Schedule before processing.

## 2. Processing details

Complete Annex A for every Order before production. Dirtyworks will process Customer Data only:

- to provide, configure, secure, support, evaluate, monitor, maintain, improve for Customer, and offboard the Services;
- on documented Customer instructions in the Agreement and approved tickets/changes;
- as required by Applicable Law, with notice where lawful; and
- for the duration and retention periods identified in Annex A.

Dirtyworks will notify Customer if it reasonably believes an instruction violates Applicable Law or the Agreement and may pause the affected processing pending resolution.

## 3. Customer obligations

Customer will:

3.1 identify Applicable Law, contractual/sector requirements, information classifications, and authorized purposes relevant to Customer Data;

3.2 ensure it has lawful authority, notices, consents, employment policies, contracts, and rights necessary for the processing;

3.3 minimize Customer Data and exclude information not approved in Annex A;

3.4 approve sources, users, permissions, products, locations, subprocessors, retention, monitoring/logging, and Supported Uses;

3.5 ensure Customer Data is sufficiently accurate, current, and appropriate for the Supported Use;

3.6 respond to individuals, regulators, employees, customers, and other third parties unless this Schedule expressly assigns Dirtyworks a task;

3.7 maintain Customer-controlled identity, endpoints, tenant, networks, backups, access approvals, policies, and incident responsibilities; and

3.8 not provide health, financial-client, employee/candidate, safety-critical, biometric, children's, criminal, or other sensitive/high-impact information unless expressly listed, risk-assessed, and approved.

## 4. Confidentiality and personnel

Dirtyworks will:

- limit access to personnel and approved subcontractors with a need to know;
- bind them to confidentiality duties appropriate to the information;
- provide role-appropriate privacy/security and AI-use training;
- remove access promptly when no longer required;
- maintain an access/role record proportionate to the Service; and
- not disclose Customer Data except as instructed, permitted by the Agreement, or legally required.

## 5. Security programme

5.1 Dirtyworks will implement the controls marked **Implemented** in Annex B and maintain evidence appropriate to the Service and risk. Controls marked **Planned**, **Inherited**, or **Not Applicable** are not contractual promises unless an Order expressly says otherwise.

5.2 Security will be proportionate to sensitivity, volume, distribution, availability/integrity consequence, threat, product architecture, and Dirtyworks' role. The Canadian Centre for Cyber Security SMB baseline is a design reference, not a certification claim.

5.3 Dirtyworks may update controls to address threats, technology, law, and operations, provided it does not materially reduce the agreed protection without notice and risk treatment.

5.4 Customer acknowledges that no service can guarantee absolute security. This does not reduce Dirtyworks' duty to perform express controls and respond to Incidents.

## 6. Access and administration

- named accounts and delegated administration where supported;
- multi-factor authentication for privileged access where supported;
- least privilege and separation of customer environments appropriate to the product;
- no shared credentials unless expressly approved with compensating controls;
- access review at launch and `[quarterly/contract-specific]` thereafter;
- prompt revocation on role change, termination, offboarding, or suspected compromise;
- privileged activity logging where supported and proportionate;
- Customer approval for permission groups and exceptions.

## 7. Subprocessors and Third-Party Services

7.1 Approved subprocessors are listed in Annex C with purpose, data, location, and material terms/status.

7.2 Customer authorizes listed subprocessors. New or replacement subprocessor handling in-scope Customer Data requires `[general authorization with 15/30 days' prior notice and objection for reasonable data-protection grounds / specific written approval]`.

7.3 Dirtyworks will impose written privacy, confidentiality, security, incident, and deletion obligations appropriate to the subprocessor's role where Dirtyworks contracts the subprocessor. Where Customer contracts a Third-Party Service directly, Customer accepts its terms and Dirtyworks' obligations are limited to the express selection/configuration/administration duties.

7.4 Dirtyworks remains responsible for its subcontractors as stated in the MSA, but does not rewrite or guarantee Customer-direct Third-Party Service terms.

7.5 If a subprocessor change creates a material unmitigated risk or violates an Order requirement, the Parties will consider configuration, replacement, scope reduction, or termination of affected processing. An objection is not a right to require an upstream vendor to change its global service.

## 8. Processing locations and government access

8.1 Known locations are recorded in Annex A/C. “Hosted in Canada” does not imply that all support, telemetry, backups, subprocessors, model inference, or legal access is Canadian unless expressly verified.

8.2 Dirtyworks will provide reasonably available information to support Customer's cross-border transparency and risk assessment.

8.3 Customer is responsible for notices or policies required for its use of service providers outside Canada, with Dirtyworks providing factual location/contact information it controls.

8.4 A Canada-only processing commitment applies only when expressly stated in the Order, technically verified across the full chain, and priced for ongoing verification/change response.

## 9. AI and model data use

9.1 Dirtyworks will not intentionally use Customer Data to train a generalized Dirtyworks model without a separate express written agreement describing data, purpose, rights, retention, safeguards, opt-out, and compensation if applicable.

9.2 For each AI product, Annex D records:

- provider/product/model/service tier;
- customer-direct or Dirtyworks contract owner;
- input/output retention;
- provider training/data-improvement terms and selected settings;
- locations/subprocessors where reasonably available;
- human review, logging, evaluation, and use limits;
- export/deletion/offboarding path;
- material vendor-change monitoring owner.

9.3 Dirtyworks will configure provider training/history/retention controls according to the Order where the product supports them. If the required control is unavailable or cannot be verified, Dirtyworks will disclose the limitation and will not process the affected Customer Data until Customer approves a lawful alternative or another product is selected.

9.4 Prompts and Outputs are Customer Data when they contain or derive from Customer Data, subject to third-party terms and IP law.

9.5 Outputs must not be treated as verified fact or professional judgment merely because they are source-linked or generated by an enterprise product. Required human review and acceptance rules remain in the Order.

9.6 Dirtyworks will maintain evaluation, permission, contradiction, unsupported-question, feedback, and incident controls stated in the Order. Changes to models, material configuration, sources, or Supported Uses may require regression testing before release.

## 10. Aggregation and de-identification

Dirtyworks may use operational data across customers only if the Order expressly permits and the information is aggregated/de-identified using reasonable measures so it cannot reasonably identify Customer, an individual, confidential content, or a customer-specific system. Dirtyworks will:

- not attempt re-identification;
- limit access and purpose;
- exclude raw Customer content and credentials;
- assess small-cell/linkage risk;
- maintain retention/deletion rules; and
- obtain separate approval for public statistics, benchmarks, case studies, quotes, or identifiable patterns.

The conservative default is **no cross-customer Customer Data use**, while allowing generalized know-how that does not contain Customer Confidential Information.

## 11. Incident response and notice

11.1 Dirtyworks will maintain an incident-response process with named contacts, containment, evidence preservation, severity classification, communication, remediation, and lessons-learned steps.

11.2 Dirtyworks will notify Customer without undue delay and no later than `[24/48]` hours after confirming an Incident affecting Customer Data. A security event that is investigated and reasonably determined not to affect Customer Data is not an Incident, but material ongoing uncertainty may warrant precautionary notice.

11.3 Initial notice will include, to the extent known:

- date/time discovered and confirmed;
- nature and scope;
- systems, data, and people potentially affected;
- known or likely consequences;
- containment/actions taken;
- information required from Customer;
- contact and next update time.

11.4 Dirtyworks will provide periodic updates and a reasonable final report including root cause and corrective actions, subject to security, privilege, confidentiality, law enforcement, and other-customer restrictions.

11.5 Customer leads statutory and contractual notification decisions for Personal Information under its control unless Applicable Law expressly requires Dirtyworks to notify. Dirtyworks will provide reasonably available assistance. Neither Party will name the other publicly without prior consultation where lawful and practicable.

11.6 Incident response costs are allocated according to breach and control: each Party bears its own ordinary response duties; additional assistance is chargeable except to the extent caused by Dirtyworks' breach. Indemnity, cap, insurance, and regulatory-cost treatment require counsel.

## 12. Individual and regulator requests

12.1 Dirtyworks will promptly forward requests from individuals or regulators relating to Customer-controlled Personal Information unless legally prohibited.

12.2 Taking account of the Service, Dirtyworks will provide reasonable assistance for access, correction, deletion, consent withdrawal, complaint, investigation, or assessment requests that Customer cannot reasonably fulfil itself.

12.3 Customer is responsible for verifying the request, deciding the response, and meeting deadlines. Assistance beyond included service or caused by Customer configuration/data may be charged at agreed rates, except where required because of Dirtyworks' breach.

## 13. Assessments, evidence, and audits

13.1 On reasonable request, Dirtyworks will provide available information needed to assess its contractual controls, such as completed questionnaires, policies, control evidence, vendor records, incident summaries, or independent reports, subject to confidentiality and security.

13.2 Customer audit rights are `[once annually and after a material Incident]`, on reasonable notice, during business hours, scoped to relevant systems/records, and conducted without accessing other-customer information, creating security risk, disrupting operations, or waiving privilege.

13.3 The Parties should use existing independent evidence before an on-site audit. Customer pays audit costs unless the audit identifies a material Dirtyworks breach or Applicable Law requires another allocation.

13.4 Penetration testing, vulnerability scanning, social engineering, facility access, or production testing requires a separate written authorization, scope, qualified tester, insurance, confidentiality, safe-harbour, timing, and remediation process.

13.5 Dirtyworks will support a Customer PIA/security assessment with factual information. Dirtyworks does not warrant legal adequacy, regulator acceptance, certification, or Customer compliance.

## 14. Retention, return, and deletion

14.1 Annex A identifies retention by data class and system. Dirtyworks will not retain Customer Data longer than needed for the approved purpose, security/legal records, or agreed backup cycle.

14.2 During the Order, Customer may export Customer Data using supported methods. Dirtyworks will provide the agreed portable Deliverables and operating records at offboarding.

14.3 On termination or Customer instruction, Dirtyworks will return or delete in-scope Customer Data within `[30/60/90]` days, except:

- information Customer retains in its own tenant/account;
- legal, tax, insurance, dispute, security, or professional records required to be retained;
- secure backups that cannot reasonably be selectively deleted, remain protected, and expire through the normal cycle;
- de-identified information validly retained under section 10.

14.4 Dirtyworks will provide `[written confirmation / system evidence / officer certificate]` appropriate to the risk and Order. Customer is responsible for deletion in Customer-owned and customer-direct vendor systems, with Dirtyworks performing only assigned administration.

## 15. Business continuity and recovery

The applicable Order/Annex B states:

- systems and records Dirtyworks backs up versus those inherited from Customer/vendors;
- backup frequency, location, encryption, access, and retention;
- recovery method and test cadence;
- manual fallback/safe suspension;
- upstream vendor continuity dependencies;
- recovery objectives, if any, that have been tested and expressly committed.

No recovery-time or recovery-point objective applies merely because backups exist.

## 16. Term and priority

This Schedule continues while Dirtyworks processes Customer Data and through return/deletion. If it conflicts with the MSA on privacy, security, incident, subprocessor, retention, or AI-data use, this Schedule controls for that subject unless a signed Order expressly and specifically identifies the deviation.

## Annex A — Processing inventory

| Field | Required detail |
|---|---|
| Order/Service | `[ ]` |
| Purpose | `[ ]` |
| Duration | `[ ]` |
| Customer/Data owner | `[ ]` |
| Individuals | `[employees, contractors, customers, suppliers, other]` |
| Data categories | `[ ]` |
| Sensitive/excluded categories | `[ ]` |
| Sources/systems | `[ ]` |
| Processing operations | `[access, retrieve, index, transmit, host, generate, evaluate, log, support, delete]` |
| Dirtyworks access roles | `[ ]` |
| Authorized Users/permission groups | `[ ]` |
| Products/subprocessors | `[Annex C/D]` |
| Processing/storage/support locations | `[ ]` |
| Retention by system/data class | `[ ]` |
| Return/export format | `[ ]` |
| Deletion/evidence | `[ ]` |
| Legal/contractual requirements | `[customer/counsel supplied]` |
| PIA/security assessment status | `[ ]` |
| Risk owner/acceptance | `[ ]` |

## Annex B — Security control statement

Status values: **Implemented**, **Planned**, **Inherited — Customer**, **Inherited — Vendor**, **Not Applicable**, **Exception Accepted**.

| Control | Working requirement | Status/evidence/owner |
|---|---|---|
| Governance | named security/privacy owner; policies; risk register; annual review | `[ ]` |
| Asset/service inventory | customer, vendor, device, account, connector and data inventory | `[ ]` |
| Access control | named accounts, least privilege, joiner/mover/leaver process | `[ ]` |
| Strong authentication | MFA for privileged and supported business accounts | `[ ]` |
| Privileged administration | delegated access; no unnecessary standing privilege; activity record | `[ ]` |
| Endpoint security | supported devices, patching, encryption, screen lock, malware protection | `[ ]` |
| Encryption | transit and at-rest controls appropriate to systems/data | `[ ]` |
| Secure configuration | hardened settings, change approval, secrets handling | `[ ]` |
| Logging/monitoring | access, admin, connector, incident and cost events as supported | `[ ]` |
| Vulnerability/patching | inventory, severity-based remediation, vendor advisories | `[ ]` |
| Backups/recovery | defined ownership, protected backups, restoration tests | `[ ]` |
| Incident response | contacts, priorities, containment, evidence, notice, exercises | `[ ]` |
| Vendor management | terms, data use, locations, subprocessors, security, exit review | `[ ]` |
| Secure development | repository/access, review, dependency/secret scanning if custom code | `[ ]` |
| Data minimization | approved sources/classes; no unnecessary local copies | `[ ]` |
| Retention/deletion | per-system rule and offboarding evidence | `[ ]` |
| Training | privacy/security/AI use and incident reporting | `[ ]` |
| Physical/remote work | workspace, device, printing, portable media controls | `[ ]` |
| Business continuity | critical process/fallback/communications/restore plan | `[ ]` |

## Annex C — Subprocessor and service-provider register

| Provider/legal entity | Service/purpose | Customer-direct or Dirtyworks | Data | Locations | Contract/data terms date | Security evidence | Notice/exit owner |
|---|---|---|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

## Annex D — AI product/model register

| Provider/product/tier | Supported Use | Contract owner | Inputs/Outputs | Retention/history | Training/improvement setting | Human review/evaluations | Material change/exit |
|---|---|---|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

## Signatures / incorporation acknowledgement

**`[Dirtyworks.ai legal entity]`**

By: __________________________  
Name/Title: `[ ]`  
Date: `[ ]`

**`[Customer legal entity]`**

By: __________________________  
Name/Title: `[ ]`  
Date: `[ ]`

