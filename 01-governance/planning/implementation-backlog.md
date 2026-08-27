# Implementation backlog

**Date:** 2026-08-26  
**Current phase:** 0 — Foundation  
**Rule:** no more than three active items at once; sequence by evidence/risk removed, not novelty

## Priority definitions

- **P0:** required to pass the current phase gate.
- **P1:** needed soon or removes meaningful risk.
- **P2:** useful after validation.
- **Parked:** deliberately deferred until its trigger exists.

## Phase 0 backlog

| ID | Priority | Work item | Owner | Dependency | Completion evidence | Status |
|---|---|---|---|---|---|---|
| F-001 | P0 | Sponsor review of strategic choices and questions | Sponsor | Strategy v0.1 | Decisions/edits recorded in company-building log | Complete for brand, lanes, capacity, and budget |
| F-002 | P0 | Select the first concentrated direct subsegment | Sponsor + founder | Network and preference | Accounting, HR/advisory, or energy-service cohort selected with inclusion rules | Ready |
| F-003 | P0 | Create interview guide and evidence-capture form | Dirty Works | Strategy | Reusable scripts/templates in `documents/tactics/` | Complete |
| F-004 | P0 | Create ICP/qualification scorecard | Dirty Works | ICP decision | Reusable scorecard with scoring guidance | Complete |
| F-005 | P0 | Create a private one-page conversation brief | Dirty Works | Message architecture | Brief usable in introductions without unvalidated claims | Complete (generic draft) |
| F-006 | P0 | Define founder time and six-month experiment budget | Sponsor | Personal/capital constraints | Budget, hours/week, and approval thresholds recorded | Complete |
| F-007 | P0 | Define target-account research schema | Dirty Works | Initial cluster | Fields, evidence standards, and source method documented | Complete |
| F-008 | P1 | Create legal/security/privacy production preflight | Dirty Works + specialists later | Risk posture | Checklist plus identified counsel/insurance needs | Complete; specialist review still required before production |
| F-009 | P1 | Initialize version control and repository conventions | Sponsor authorization / Dirty Works | None | Git repository and ignore/readme conventions | Pending |
| F-010 | P1 | Build an 18-month cash and scenario model | Dirty Works + sponsor | F-006 capacity/budget | Base, downside, and upside cash/MRR/capacity model | Complete; extended to 36 months with unit/channel economics and checks |
| F-013 | P1 | Create investment-baseline narrative and financial-model guide | Dirty Works | F-010 plus strategy/brand documents | Investor-grade text deck, assumptions guide, explicit gaps, and workbook exhibit references | Complete |
| F-011 | P0 | Create brand/message strategy | Dirty Works | Sponsor brand decision | Brand line, segment messages, risks, and validation thresholds | Complete |
| F-012 | P0 | Create MSP channel strategy | Dirty Works | Live MSP opportunity | Partner models, economics, responsibilities, qualification, and pilot plan | Complete |
| F-014 | P1 | Define governed client product catalogue and commercial pathways | Dirty Works | Offer/pricing and customer-ownership policy | Need-based menu, candidate catalogue, customer-direct/resale/cloud/self-hosted pathways, controls, and validation plan | Complete; commercial rights remain quote-time gates |
| F-015 | P1 | Build client product configurator workbook MVP | Dirty Works | F-014 | Formula-driven mixed-product estimate with vendor/service separation, source register, and checks | Complete; pricing hypotheses require live quote validation |
| F-016 | P1 | Investigate client operations platform and proprietary control-layer opportunity | Dirty Works | Service delivery, catalogue and contract architecture | Systems of record, workflows, market map, build/buy decision, moat analysis and activation gates documented | Complete; platform selection intentionally deferred |
| F-017 | P1 | Define the agent-operated multi-system control plane and client self-service viability | Dirty Works | F-016 and AI Operations Ledger concept | System collection, connector/action contract, authorization levels, operating controls, phased gates, public-price cost model and build ranges documented | Complete; implementation remains evidence-gated |
| F-018 | P0 | Define the packaged AI SaaS launch core and advanced-workload boundary | Dirty Works | Sponsor operating-stack direction | Base systems, authority, support/training/cost controls, billing choices, agent seam and advanced triggers documented | Complete; vendor capabilities and commercial rights remain validation gates |
| F-019 | P0 | Investigate cross-vendor SaaS/AI cost-management systems and transaction approaches | Dirty Works | F-018 cost-control focus | SMP shortlist, source hierarchy, 1Password SaaS Manager fit, accounting/Plaid alternatives, build options, demonstration scorecard and blockers recorded | Complete; quotes and multi-client capability require validation |
| F-020 | P0 | Define pre-launch, pre-customer and first-customer operating checklists plus private-record structure | Dirty Works | F-008/F-018 and sponsor base-stack direction | Two-stage launch gate, customer acceptance gate, first-customer runbook, system boundaries, templates and evidence fields documented | Complete; revised for the Markdown source decision |
| F-021 | P0 | Define one-repository-per-client Markdown operating source and interface/graph contract | Dirty Works | Sponsor Markdown direction plus personal-wiki/kgmd inspection | Authority, page/relationship schema, templates, source ingestion, review, isolation, interface writes, security, acceptance tests and migration triggers documented | Complete; implementation and synthetic evidence remain V-020/P-003 |

## Phase 1 backlog

| ID | Priority | Work item | Owner | Dependency | Completion evidence | Status |
|---|---|---|---|---|---|---|
| V-001 | P0 | Build first 50-account target list in selected direct subsegment | Founder + Dirty Works | F-002, F-007 | Named, sourced accounts with fit/trigger data | Pending |
| V-002 | P0 | Map 30 warm introduction paths | Founder | V-001 | Contact/path and next action recorded | Pending |
| V-003 | P0 | Conduct and record 20 problem interviews | Founder | F-003 | Structured notes and aggregate evidence | Pending |
| V-004 | P0 | Test three positioning frames | Founder | F-005 | Message/reaction evidence across interviews | Pending |
| V-005 | P0 | Create Knowledge Reliability Review sales and delivery kit | Dirty Works | F-003/F-004 | SOW, intake, interview, analysis, output templates | Pending |
| V-006 | P0 | Sell and complete 3–5 paid reviews | Founder | Qualified opportunities | Signed work, payment, reports, decision data | Pending |
| V-007 | P1 | Perform local competitor/partner mystery-shopping research | Dirty Works | Initial cluster | Evidence table for offers, proof, price, controls | Pending |
| V-008 | P1 | Quantify target-account population and common systems | Dirty Works | Initial cluster | Sourced market-sizing note | Pending |
| V-009 | P0 | Conduct discovery with live MSP opportunity using completed discovery kit | Founder | F-012 | Partner score, required model, responsibilities, economics, and next action | Ready |
| V-010 | P0 | Identify and qualify one MSP-sourced pilot account | MSP + founder | V-009 | Named customer enters qualification or paid review | Pending |
| V-011 | P1 | Draft partner pilot term sheet and responsibility schedule | Dirty Works + counsel later | V-009 | Commercial draft ready for legal review | Pending |
| V-012 | P1 | Test the product menu and transparent management layer in 10 buyer/partner conversations | Founder | F-014/F-015 | Product-selection behaviour, objections, requested vendors, and preferred commercial model recorded | Ready |
| V-013 | P1 | Produce five real portfolio estimates and time the work | Founder + Dirty Works | Qualified prospects | Versioned estimates, accepted/rejected structure, quoting time, exceptions, and errors | Pending |
| V-014 | P2 | Obtain one Microsoft/Google distributor or vendor-partner commercial proposal | Founder | Confirmed client or MSP demand | Written authorization requirements, price/margin, credit, support, renewal, and cancellation economics | Pending |
| V-015 | P1 | Run two client-operations platform demonstrations using the synthetic-client scorecard | Founder + Dirty Works | Live MSP seam understood or explicit direct-only assumption | Recorded weighted scores, commercial/security/API facts, trial exceptions and backbone decision | Pending |
| V-016 | P1 | Test agent-operability in the two platform demonstrations | Founder + Dirty Works | V-015 demonstration access | Five read questions and five request/work-card flows tested for API coverage, service identity, custom objects, approval, audit/export, tenant isolation and verification | Pending |
| V-017 | P0 | Test the Managed AI SaaS Operations core in 10 buyer/MSP conversations | Founder + Dirty Works | F-018 plus catalogue/configurator | Evidence on service value, products, managed-user definition, training/support demand, customer-direct versus consolidated billing, willingness to pay and objections | Ready |
| V-018 | P0 | Demonstrate and quote 1Password SaaS Manager for Dirtyworks's SMB/MSP use case | Founder + Dirty Works | F-019; vendor trial/sales access | Synthetic two-client isolation test; ChatGPT/OpenAI plus second AI connector; finance mapping; licence/usage/contract reconciliation; API/MCP/export; Canadian data facts; one-client/five-client/MSP quotes | Ready |
| V-019 | P1 | Compare CloudEagle and optionally Zylo using the same cost-management scorecard | Founder + Dirty Works | V-018 script | CloudEagle scored against identical synthetic jobs, quote, multi-client/service-provider and exit requirements; add Zylo only if enterprise consumption depth remains material | Pending |
| V-020 | P0 | Build and test two synthetic Markdown client repositories | Founder + Dirty Works | F-009/F-021; personal-wiki and kgmd adaptation | Current schema validates; source-to-finding review/promotion works; authored-page operational lint passes; kgmd excludes reserved/frontmatter noise and separates declared/inferred edges; ten sourced questions pass; secrets are rejected; graph is client-local; cross-client query denied; recovery and offboarding tested; time/errors recorded | Ready for tool/template implementation |

## Phase 2 backlog

| ID | Priority | Work item | Owner | Dependency | Completion evidence | Status |
|---|---|---|---|---|---|---|
| P-001 | P0 | Select platform per pilot requirements | Dirty Works + customer | Paid review | Documented decision matrix | Pending |
| P-002 | P0 | Complete legal contract and insurance review | Sponsor + specialists | Business-draft contract stack plus real pilot scope | Counsel-approved templates aligned to actual coverage | Business drafts complete; counsel and insurance review pending |
| P-003 | P0 | Configure customer operating record and launch/support playbook across the selected base systems | Dirty Works | F-020/F-021/V-020 plus V-017 and paid engagement evidence; V-015 only if a broader platform/MSP seam is required | Freshdesk/private Markdown repository/1Password/native-vendor/register records built from the checklist pack, linked source authority, support/training workflow, cross-client isolation and successful synthetic onboarding/monthly-close/offboarding dry run | Pending |
| P-004 | P0 | Launch two production pilots | Dirty Works | P-001/P-002/P-003 | Acceptance evidence and 30-day review | Pending |
| P-005 | P0 | Implement time, cost, quality, and outcome measurement | Dirty Works | Pilot scope | Account-level scorecard and margin data | Pending |
| P-006 | P0 | Convert successful pilots to recurring service | Founder | Acceptance/value review | Managed-service contracts active | Pending |
| P-007 | P1 | Produce first approved case study | Founder + customer | Outcome evidence | Claim-approved asset | Pending |
| P-008 | P1 | Create standard deployment/offboarding runbooks for the first supported product set | Dirty Works | Products selected in paid reviews | Commercial, admin, data/security, delivery, operations, and exit gates complete | Pending |
| P-009 | P1 | Implement and reconcile client product and access register | Dirty Works | Selected backbone plus first deployed mixed-product portfolio | Product owner, billing path, users, admins, renewal, support, value, source/freshness, authoritative state, and offboarding fields reconciled | Pending |
| P-010 | P0 | Resolve pre-signature contract decisions | Sponsor + counsel | Contracting framework | Legal entity, liability/indemnity position, dispute path, incident notice, data-location posture, IP defaults, renewal, and insurance limits approved | Pending |
| P-011 | P1 | Draft MSP partner agreement and responsibility schedule | Sponsor + counsel | Live partner delivery model selected | Prime/subcontractor roles, support seams, data roles, claims, economics, customer ownership, liability, and exit approved | Pending |
| P-012 | P1 | Prototype the internal read-first operations agent with a synthetic client | Dirty Works | V-020 plus selected systems; V-015/V-016 only for an added platform/PSA | Sourced answers across Freshdesk, published Markdown/kgmd, the controlled register and one native vendor read surface; page/freshness citations; request work cards; tenant/role enforcement; redacted action log; no direct vendor writes | Pending |

## Phase 3 backlog

| ID | Priority | Work item | Trigger | Status |
|---|---|---|---|---|
| R-001 | P1 | Build private website preview, then public website | Direct cohort selected; publish after five interviews and MSP message check | Parked |
| R-002 | P1 | Implement CRM and sales reporting | Pipeline can no longer be reliably managed in a simple table | Parked |
| R-003 | P1 | Implement Hudu or PSA/ITSM depth beyond the Freshdesk/Markdown base | A real account or MSP requires read audit, granular permissions, portal, change/assets/contracts/time/SLA/billing integration or lower measured TCO beyond P-003 | Parked; the base configuration now belongs to P-003 |
| R-004 | P1 | Build evaluation regression runner | Repeated manual evaluation cost is measured | Parked |
| R-005 | P1 | Build monthly value-report generator | Two reports show stable repeated structure | Parked |
| R-006 | P2 | Generalize the MSP partner offer beyond the live design pilot | One successful partner pilot or two credible partner requests | Parked |
| R-007 | P2 | First delivery hire plan | Contracted recurring margin and capacity data support it | Parked |
| R-008 | P2 | Replace the product configurator workbook with an internal or client-facing application | Five real quotes establish a stable schema and 3 portfolios need reconciliation, or a signed opportunity requires it | Parked; application specification complete |
| R-009 | P2 | Build the first internal AI Operations Ledger slice | At least four documented activation conditions, including repeated production workflow and measurable value | Parked; application concept complete |
| R-010 | P2 | Build the first client read/request self-service portal | Three active clients share the workflow, a funded MSP/client requires it, or manual request/reconciliation work exceeds the documented effort/profit threshold | Parked; capability levels and release gates defined |

## Marketing and design implementation

| ID | Priority | Work item | Dependency | Completion evidence | Status |
|---|---|---|---|---|---|
| M-001 | P0 | Define detailed brand platform and voice | Sponsor boldness direction | Voice rules, copy bank, story, claims, and quality check | Complete |
| M-002 | P0 | Define creative territories and design-engine brief | Brand platform | Recommended direction, tokens, type, image, layout, motion, accessibility, and review criteria | Complete |
| M-003 | P0 | Define website and presentation content systems | M-001/M-002 | Page/slide narrative, example copy, components, branches, and acceptance tests | Complete |
| M-004 | P1 | Run design-engine exploration for three mark routes and `PROOF / WORK` system | M-001/M-002/M-003 | Reviewable vector, web, deck, motion, and accessibility concepts | Ready |
| M-005 | P1 | Select and refine the final identity route | M-004 plus buyer/MSP reactions | Recorded decision and production-ready brand system | Pending |
| M-006 | P1 | Build private website prototype | M-005 or approved provisional system | Responsive prototype using real copy and accessibility checks | Pending |
| M-007 | P1 | Build editable customer/MSP/investor deck master | M-005 | Slide archetypes and three narrative branches in editable format | Investor text narrative complete; editable designed master pending identity selection |
| M-008 | P1 | Validate brand trust and comprehension | M-004/M-006 | Five buyer reactions, MSP reaction, comprehension and objection evidence | Pending |
| M-009 | P0 | Reframe website content around the full AI MSP offer | Product catalogue plus sponsor clarification | Page architecture, homepage and secondary-page copy, design-system mapping, responsive notes, claims, and handoff checklist | Complete; offer names and launch scope remain sponsor choices |
| M-010 | P1 | Approve the website launch scope and broader commercial offer names | M-009 plus sponsor review | Focused/full site decision and public review/deploy/operate naming recorded | Ready |
| M-011 | P1 | Complete founder, legal, privacy, contact, and supported-product publication inputs | M-009/M-010 | Approved production content with legal and evidence review | Pending |
| M-012 | P1 | Establish human-centred photography direction and initial image library | Design system plus website layout | Four project-created generated candidates, licensed-stock shortlist, placement/provenance/licence rules, and reusable prompts | Complete; final public selections pending |
| M-013 | P2 | Commission a local founder/operations photography shoot | Public-launch scope and final page compositions | Released Calgary/Alberta founder and work imagery with responsive crops and provenance | Pending sponsor decision |
| M-014 | P0 | Define the promotion and demand-generation operating plan | GTM, offer, brand, capacity, website and current-channel research | Campaigns, channels, capital gates, founder capacity, measurement, compliance and 90-day programme | Complete |
| M-015 | P0 | Execute the first 13-week cohort campaign | Sponsor selects direct cohort; basic tracking and conversion path functional | 50-account cohort, 30 intro requests, recent-event conversations, first roundtable, proposals, channel decisions and recorded losses | Pending cohort selection |
| M-016 | P1 | Produce the first campaign conversion artifacts | M-014 plus cohort/public-offer naming | Answer Desk Diagnostic, Product and Account Register, Launch Control Register, MSP Responsibility Seam, offer sheet and editable sources | Ready after cohort selection; generic drafts can begin earlier |
| M-017 | P1 | Establish CASL-compliant outreach and consent operations | Legal entity/contact inputs plus outbound/email tool selection | Contact-source/consent record, compliant identity/footer/unsubscribe, suppression process, privacy notice and legal review | Pending |
| M-018 | P1 | Evaluate an intent-signal prospecting tool such as GojiBerry against manual research | Cohort selected; M-017 contact-basis controls; vendor source/platform/privacy diligence | 30-day, 25–50-account paired test measuring research time, signal quality, conversations, qualification, cost and risk | Designed; do not connect automated LinkedIn actions under current policy |
| M-019 | P0 | Align website and proposal copy to the Managed AI SaaS Operations launch core | F-018 plus M-010 offer naming | Base service, advanced-workload seam, consolidated-statement/single-invoice distinction and support/training/cost-control claims reflected in production handoff | Ready; existing full AI MSP copy remains the broader capability architecture |

## Product/application parking lot

| Idea | Why it is not active | Activation evidence |
|---|---|---|
| Multi-tenant knowledge platform | Native products already cover much of the interface; requirements unknown | Same unmet requirement in 3+ customers and funded lifecycle case |
| Customer portal / self-service control plane | No repeated client workflow yet; PSA/documentation portals may cover early read/request needs | Three active clients share the workflow, funded MSP/client need, more than eight manual hours/month or 10% recurring gross-profit burden, or a signed requirement existing portals cannot safely meet |
| Connector framework | Vendor/source mix unknown | Same unsupported connector causes repeated delivery cost |
| AI Operations Ledger / governance registry | Market investigation supports configuration first; custom normalization/evidence layer may become defensible after delivery evidence | Four activation conditions, including 3+ shared production workflows and measurable value; see application concept |
| Automated opportunity miner | Premature and creates surveillance/quality risk | Sufficient permissioned usage data and clear customer-approved method |
| Client product configurator application | Workbook is enough to learn the workflow; approval/versioning/integration needs are unmeasured | Five real quotes plus 3 deployed portfolios, 2 concurrent operators, a measurable quoting problem, or signed portal requirement |

## Next three actions

1. Select the first concentrated direct subsegment: accounting, HR/advisory, or energy services.
2. Run the live MSP partner-discovery session and determine referral, co-managed, or full white-label requirements.
3. Build the first 50-account list and adapt the interview brief to the selected subsegment.
