# Dirtyworks.ai marketing website — content and layout handoff

**Version:** 0.2  
**Date:** 2026-08-25  
**Status:** Content and layout direction ready for design/coding handoff; claims, commercial names, legal copy, and product availability require final approval before publication  
**Design system:** [`PROOF / WORK`](../design-system/production-guide.md)  
**Relationship to prior work:** Supersedes the website portion of the [website and presentation blueprint](website-and-deck-content-blueprint.md). The presentation material in that document remains active.

> **Design-system authority:** Use the supplied design system only for visual foundations, tokens, components, interaction patterns, and layout behavior. All words, page structures, navigation, offers, examples, metrics, and calls to action contained in its UI kits, templates, slides, and component specimens are filler and must be ignored. This document is the authoritative website content and information-architecture source.

## 1. Strategic frame

### What the website must now say

Dirtyworks.ai is an **AI managed service provider**. It gives a company one operating partner across its AI products, people, information, integrations, controls, support, and costs.

The product catalogue is the selectable technology layer inside the service. Knowledge reliability is a differentiated operating capability inside the service. Neither is the whole proposition.

```text
DIRTYWORKS.AI / MANAGED AI OPERATIONS
       │
       ├── AI product portfolio and access
       ├── account, licence, and user lifecycle
       ├── onboarding, training, adoption, and support
       ├── company knowledge and data reliability
       ├── application integration and managed automation
       ├── governance and compliance-readiness controls
       ├── monitoring, incidents, and vendor change
       └── usage, licence, and cost control
```

### Recommended public positioning

**Category descriptor**

> Managed AI operations for Alberta businesses.

**Plain-language definition**

> Dirtyworks.ai is the AI MSP for companies that need more than licences. We select and deploy approved AI products, manage users, train teams, support integrations, operate controls, monitor the service, and keep costs visible.

**Brand promise**

> We do the work behind AI that works.

**Differentiator**

> One accountable operating layer across the tools, people, company information, controls, and costs behind business AI.

### Important claim boundaries

- `Provide access` means either authorized resale or administration of a customer-direct account. It does not mean Dirtyworks.ai can resell every product.
- `Compliance` means proportional controls, records, monitoring, and specialist coordination. It is not a certification or legal guarantee.
- `Monitoring` includes service condition, access, integrations, usage, quality, cost, incidents, and vendor change within the contracted scope. It is not universal surveillance or a guarantee of vendor uptime.
- `Support` applies to the managed AI scope and agreed support window. It is not general endpoint or IT support unless an MSP/customer contract says otherwise.
- Customer-owned tenants, data, billing recovery, and exportable records are the default.
- Public prices, quantified savings, accuracy, customer logos, testimonials, and outcome metrics remain unpublished until verified and approved.

## 2. Website job and conversion strategy

The site should help a qualified buyer answer four questions in order:

1. **Is this an AI MSP, a consultancy, or a software product?**  
   An AI MSP: an ongoing operating service with review, deployment, support, control, and improvement work.
2. **What does it actually manage?**  
   Products, users, training, knowledge, integrations, policies, monitoring, incidents, licences, and costs within a defined scope.
3. **Can I trust it with company systems and information?**  
   Trust comes from customer ownership, named responsibilities, least privilege, visible records, tested boundaries, honest limitations, and portable exit.
4. **What should I do next?**  
   Map the current AI stack and the last event that exposed a gap.

### Primary conversion

`MAP YOUR AI STACK`

This is a diagnostic conversation, not an automated checkout. It can lead to a paid scoped review, a managed deployment, an MSP partner pilot, or a decision not to proceed.

### Secondary conversions

- `SEE WHAT WE MANAGE`
- `COMPOSE A PRODUCT MIX`
- `READ THE TRUST MODEL`
- `DESIGN A PARTNER PILOT`

### Calls to action not to use

`GET STARTED` · `LEARN MORE` · `BOOK A DEMO` · `CONTACT US` · `TALK TO SALES`

## 3. Information architecture

### Primary navigation

| Label | Route | Job |
|---|---|---|
| `SERVICES` | `/services` | Explain the complete managed-service scope |
| `CATALOGUE` | `/catalogue` | Show the governed product mix and commercial routes |
| `METHOD` | `/method` | Explain review, design, deployment, adoption, operation, and improvement |
| `TRUST` | `/trust` | State boundaries, ownership, controls, incident practice, and exit |
| `FOR MSPs` | `/msps` | Explain referral, co-managed, and white-label delivery |
| Primary action | `/start` | `MAP YOUR AI STACK` |

`ABOUT` and `NOTES` belong in the footer and may be promoted into navigation after real founder/proof content exists. A six-link header plus action is already dense; do not add separate Pricing, Products, Solutions, Industries, Resources, Company, and Login menus.

### Page inventory

| Page | Purpose | Primary action |
|---|---|---|
| Home | Establish category, scope, differentiation, and next step | Map your AI stack |
| Services | Detail what Dirtyworks.ai operates | Map the managed scope |
| Catalogue | Explore a governed mix without implying open resale | Compose a product mix |
| Method | Show how the service moves from uncertainty to operation | Start with a scoped review |
| Trust | Make responsibilities and limitations inspectable | Review a responsibility seam |
| For MSPs | Establish partner models and one-customer pilot | Design a partner pilot |
| About | Establish operator credibility and company posture | Bring us the operating problem |
| Notes | Publish evidence-led point of view | Read a specific note |
| Start | Capture a safe diagnostic event and current stack | Submit the stack map |

## 4. Global layout and component direction

Use the supplied design system for visual execution only. This document specifies the authoritative content, information architecture, order, and composition. Do not copy or reconcile against filler content embedded in design-system specimens.

The [photography direction and image library](../brand/photography-direction-and-image-library.md) supplies four original human-centred candidates, a real-stock shortlist, placement guidance, provenance, and production constraints. Photography may warm the experience, but it must never be presented as customer proof unless it is an approved real customer image.

### Header

**Component:** `SiteHeader`  
**Layout:** sticky, bone ground, wordmark left, primary navigation centred/right, orange primary action, version marker.  
**Version marker:** `SITE / 0.2` or deploy date. It is a visual folio, not a certification mark.

Mobile order:

1. wordmark;
2. menu control;
3. persistent primary action inside the opened menu, not as a floating screen button.

### Footer

**Component:** `SiteFooter`

Required content:

- wordmark and brand promise;
- Calgary, Alberta / Canada;
- Services, Catalogue, Method, Trust, For MSPs, About, Notes;
- privacy, terms, accessibility;
- business email and approved professional channel;
- `Customer-owned by default. Human accountability stays human.`
- legal entity and copyright once approved.

Do not place a newsletter form in the footer until there is a real publishing cadence and consent workflow.

### Page rhythm

Every major page should alternate:

1. oversized declaration;
2. compact operating/evidence register;
3. quiet explanatory passage;
4. full-width method, comparison, or responsibility field;
5. hard conversion band.

Do not turn the eight service capabilities or seven catalogue categories into identical rounded feature cards. Use registers, owner rows, annotated comparisons, work orders, article rows, and bounded fields.

### Design-system component map

| Content job | Approved component/pattern |
|---|---|
| Hero interruption | `Declaration` plus `ProofLabel` and a compact register |
| Service capability | `OwnerRow` or an editorial row with scope/owner/status |
| Product/category list | `ControlRegister`, `ArticleRow`, or evidence rows—not a logo cloud |
| Tool versus service | `AnnotatedComparison` |
| Lifecycle | `WorkOrder` |
| Controls/responsibilities | `ControlRegister` and `OwnerRow` |
| Fit/non-fit | `FitField` |
| Evidence or limitation | `EvidenceRail`, `ProofLabel`, `Redaction`, `PullQuote` |
| Conversion | `CTABand` or `DiagnosticForm` |
| Metrics later | `CaseMetric` only with source/method or `HYPOTHESIS — NOT MEASURED` |

## 5. Homepage content and layout

### HOME / 01 — Hero

**Folio**

`DIRTYWORKS.AI / MANAGED AI OPERATIONS`

**Display copy**

> AI IS ALREADY AT WORK.  
> IS ANYONE OPERATING IT?

**Support copy**

> Dirtyworks.ai is the AI MSP for companies that need more than licences. We select and deploy approved AI products, manage users, train teams, support integrations, operate controls, monitor the service, and keep costs visible.

**Primary action:** `MAP YOUR AI STACK`  
**Secondary action:** `SEE WHAT WE MANAGE`

**Layout**

- Desktop: 7-column declaration left; 5-column operating register right.
- Mobile: declaration, support, actions, then register.
- One grid violation: crop or offset the word `OPERATING`, not the body copy or action.
- No product screenshot, stock image, animated particles, or vendor-logo strip.

**Hero register**

Label it `AI PORTFOLIO / ILLUSTRATIVE`, because it is not customer evidence.

| PRODUCT / USE | OWNER | ACCESS | COST | STATUS |
|---|---|---|---|---|
| Workforce assistant | Operations | Company account | Known | `MANAGED` |
| Image generation | Marketing | Named users | Known | `REGISTERED` |
| Model API | Development | Scoped keys | Budgeted | `MONITORED` |
| Personal AI account | Unknown | Unknown | Unknown | `GAP / OPEN` |

The register demonstrates the job without pretending the website knows the visitor’s tools.

### HOME / 02 — Problem

**Folio:** `02 / THE UNMANAGED STACK`

**Heading**

> ANOTHER LICENCE IS NOT AN OPERATING MODEL.

**Opening copy**

> AI tools arrive one person, one team, and one expense claim at a time. Soon the company has accounts nobody inventories, data rules nobody can explain, integrations nobody monitors, overlapping subscriptions, and employees asking one another what is safe to use.

> The cost appears as abandoned licences, repeated work, support interruptions, uncontrolled consumption, failed connections, and risk that remains invisible until something happens.

**Evidence rail — `ILLUSTRATIVE EVENTS`**

- A new employee still has no approved AI account after two weeks.
- A former employee still appears on a vendor seat list.
- Marketing and operations bought different tools for the same job.
- An automation stopped after a vendor changed an API.
- A public AI account is being used with company information.
- Nobody can explain the current monthly AI spend.
- A team received an answer, but nobody knows which source it relied on.

**Layout**

- 5-column heading/copy; 7-column `EvidenceRail`.
- Fragments begin misaligned and resolve into a register on scroll.
- Every fragment is marked `ILLUSTRATIVE`, not presented as a customer metric.

### HOME / 03 — Complete offering

**Folio:** `03 / WHAT WE OPERATE`

**Heading**

> THE TOOL IS ONE LINE ITEM. THIS IS THE SERVICE.

**Lead**

> Dirtyworks.ai manages the operating work around a defined AI portfolio. The scope can begin with one product or one team and expand only when ownership, controls, value, and support remain clear.

**Capability register**

| Label | Public copy | Typical records |
|---|---|---|
| `PORTFOLIO / SELECTED` | Compare products, prerequisites, overlap, commercial routes, and fit with the systems you already use. | approved catalogue, decision record, vendor/renewal register |
| `ACCESS / MANAGED` | Create the company-owned account structure, assign licences, manage roles, and handle joiners, movers, and leavers. | tenant owner, user register, admin roles, recovery path |
| `TEAM / ENABLED` | Onboard people, teach supported use, provide role-specific guidance, and give them somewhere to get help. | training record, use guidance, support path, adoption issues |
| `KNOWLEDGE / OWNED` | Connect approved company information, name source owners, test permissions, and make unsupported answers visible. | source register, owner map, evaluation set, gap log |
| `SYSTEMS / CONNECTED` | Integrate approved applications and build assisted or automated workflows with tests, exceptions, and rollback. | connection inventory, workflow runbook, approvals, recovery procedure |
| `CONTROL / OPERATED` | Maintain practical policy, privacy, security, data, and compliance-readiness controls for the managed scope. | use-case register, access evidence, risk/decision log, control review |
| `SERVICE / WATCHED` | Monitor supported services, integrations, incidents, material quality failures, and vendor changes. | health record, incident log, change log, escalation path |
| `COST / CONTROLLED` | Track licences and usage, set budgets and alerts, remove abandoned access, and review overlap before renewal. | spend view, budget/alert record, licence reconciliation, renewal decision |

**Closing line**

> You keep the company decisions. We keep the operating work from disappearing between vendors, employees, IT, and policy.

**Layout**

- Use eight `OwnerRow`/register rows, not feature cards.
- Alternate full and offset rows to preserve controlled irregularity.
- Each row may expose one example record so the claim has a mechanism.

### HOME / 04 — Product mix

**Folio:** `04 / THE GOVERNED CATALOGUE`

**Heading**

> CHOOSE THE TOOLS. KEEP ONE OPERATING MODEL.

**Copy**

> A client can choose from a governed mix of workforce AI, research, creative, developer, automation, data, and monitoring products. We assess the fit, confirm how the account can be purchased, deploy it into the company, and attach the operating work it requires.

> When Dirtyworks.ai is authorized to resell a product, it can be quoted through that channel. Otherwise the client contracts with the vendor and Dirtyworks.ai administers the account. Customer ownership remains the default either way.

**Menu rows**

| Menu | Job | Candidate examples | Operating emphasis |
|---|---|---|---|
| `WORK` | General workforce assistants | ChatGPT Business, Claude Team, Microsoft 365 Copilot, Google Workspace with Gemini | account, identity, policy, training, support |
| `FIND` | Research and company knowledge | Perplexity Enterprise and approved assistant/knowledge configurations | sources, permissions, retention, evidence, evaluation |
| `MAKE` | Images, meetings, documents, and content | Midjourney, Canva Business, Fathom, Notion Business | named accounts, records policy, brand/use guidance |
| `BUILD` | Coding, models, and APIs | GitHub Copilot, OpenAI API, Anthropic API, OpenRouter, Azure, AWS, Google Cloud | keys, budgets, evaluations, model and change control |
| `MOVE` | Integration and automation | Zapier, Make, n8n | credentials, testing, exceptions, monitoring, rollback |
| `HOLD` | Application data and semantic search | Supabase, Pinecone | access, region, backup, retention, capacity |
| `WATCH` | Tracing and evaluation | Langfuse, LangSmith | telemetry, tests, alerts, incidents, cost review |

**Product disclaimer**

> Product names are candidate examples, not a promise of availability, resale authorization, suitability, or fixed price. Every quote confirms current terms, prerequisites, ownership, support, and commercial route.

**Actions:** `COMPOSE A PRODUCT MIX` · `SEE THE CATALOGUE METHOD`

**Layout**

- Heading and copy occupy 4 columns; category register occupies 8.
- Candidate names are text in the register, not a logo cloud.
- Do not publish per-seat pricing in the first website release.

### HOME / 05 — Managed comparison

**Folio:** `05 / ACCESS VERSUS OPERATION`

**Heading**

> ACCESS IS NOT THE SERVICE.

**Support**

> Buying the product answers “what can we use?” Managed operations answer “who owns it, how does it fit, what can it access, who supports it, what changed, and should we keep paying for it?”

**Annotated comparison**

| Product access | Managed AI operations |
|---|---|
| Product selected | Fit, overlap, prerequisite, and commercial route recorded |
| Seat assigned | Named user, role, owner, recovery, and offboarding managed |
| Training link sent | Role-specific onboarding, use guidance, support, and adoption review |
| Connector enabled | Data boundary, permission, test, exception, and failure path documented |
| Vendor says “secure” | Relevant controls and limitations reviewed for the actual use case |
| Usage dashboard exists | Budget, licence, quality, incident, and value signals reviewed |
| Renewal notice arrives | Need, overlap, price, ownership, and exit assessed before renewal |

**Layout:** `AnnotatedComparison`, with the decisive row on renewal/exit.

### HOME / 06 — Knowledge differentiator

**Folio:** `06 / THE COMPANY MEMORY`

**Heading**

> YOUR AI CAN ONLY RELY ON WHAT THE COMPANY ACTUALLY OWNS.

**Copy**

> Company information is scattered, duplicated, stale, overexposed, under-owned, and carried in people’s heads. Connecting a model does not repair any of that.

> We identify approved sources, name owners, test access, evaluate real questions, expose contradictions, and record what the system should not answer. That makes knowledge operations part of the AI service—not a separate filing project nobody maintains.

**Proof sequence**

`SOURCE / APPROVED` → `OWNER / NAMED` → `PERMISSION / TESTED` → `ANSWER / SUPPORTED` → `GAP / OPEN` → `CHANGE / LOGGED`

**Pull quote**

> “I don’t know” is a feature when the alternative is confident use of the wrong source.

**Action:** `SEE HOW KNOWLEDGE IS OPERATED`

**Layout**

- Ink full-width band.
- 7-column proof sequence, 5-column serif countervoice.
- This is the main bridge from broad AI MSP to the existing knowledge-reliability method.

### HOME / 07 — Method

**Folio:** `07 / FROM STACK TO SERVICE`

**Heading**

> MAP IT. DEPLOY IT. OPERATE IT.

**Work order**

1. `MAP` — products, accounts, people, company information, integrations, spend, problems, and desired outcomes.
2. `DESIGN` — choose the smallest viable product mix; identify overlap, prerequisites, owners, controls, support, and commercial route.
3. `APPROVE` — agree purpose, scope, data, responsibilities, costs, permitted use, tests, and stop conditions.
4. `DEPLOY` — establish customer-owned accounts, configure roles and settings, connect approved systems, test, document, and train.
5. `STABILIZE` — support a bounded cohort, resolve access and quality problems, confirm cost signals, and complete acceptance.
6. `OPERATE` — manage users, support, monitoring, controls, incidents, vendor changes, spend, renewals, and monthly improvement.
7. `RENEW OR EXIT` — reconcile value and licences, re-price, replace, export, transfer, or remove cleanly.

**Method note**

> A valid review can conclude: deploy, repair first, use a simpler product, keep the work human, or stop. Selling another tool is not the required outcome.

**Action:** `READ THE OPERATING METHOD`

**Layout:** vertical `WorkOrder`; show the feedback loop from operate to map/design.

### HOME / 08 — Trust and compliance readiness

**Folio:** `08 / TRUST IS OPERATED`

**Heading**

> COMPLIANCE IS NOT A STICKER.

**Copy**

> Dirtyworks.ai helps clients identify relevant obligations, configure practical controls, maintain operating evidence, monitor the managed scope, and bring in privacy, security, legal, or industry specialists when the work requires them.

> We do not certify legal or regulatory compliance. We do not replace the customer’s accountable officers, counsel, security provider, or professional judgment.

**Public control extract**

| Control | Mechanism | Responsibility |
|---|---|---|
| Customer ownership | Tenant, data, billing recovery, and exportable records remain customer-controlled by default | Customer + Dirtyworks.ai |
| Approved use | Intended users, information, decisions, and exclusions are written before deployment | Customer approves; Dirtyworks.ai records/operates |
| Access | Named accounts, MFA where available, least privilege, role/permission tests, revocable administration | Shared responsibility |
| Data and vendors | Location, retention, training use, subprocessors, and deletion are reviewed proportionally | Shared responsibility |
| Human decisions | Consequential employment, financial, legal, engineering, safety, and regulatory decisions remain accountable to people | Customer |
| Monitoring and incidents | Supported alerts, reporting, containment, notification, and written follow-up are defined | Dirtyworks.ai within scope |
| Portability | Current inventory, configuration, records, customer artefacts, and access removal form the exit package | Shared responsibility |

**Action:** `READ THE TRUST MODEL`

**Layout:** 4-column heading/limitations; 8-column `ControlRegister`.

### HOME / 09 — Fit

**Folio:** `09 / INITIAL FIT`

**Heading**

> START WHERE THE WORK IS VALUABLE AND THE BOUNDARY IS CLEAR.

**Fit field 1 — Professional services**

> Manage workforce AI, research, internal methods, templates, software procedures, engagement administration, onboarding, and low-risk workflow assistance.

Initial exclusions: unsupervised professional judgment, employee decisions, and client-record use without a specific approved scope.

**Fit field 2 — Energy services**

> Manage workforce AI, commercial and project information, client requirements, internal systems, project administration, closeout, and bounded workflow assistance.

Initial exclusions: safety, engineering, field-control, and regulatory decisions without specialist governance and a separately approved operating model.

**Fit field 3 — Traditional MSPs**

> Add product selection, AI administration, enablement, knowledge operations, governance, and managed AI workflows to an existing client relationship.

Partner fit requires an explicit responsibility seam for identity, security, service desk, customer access, data roles, sales, support, margin, and liability.

**Layout:** three editorial spreads; on desktop, two direct-client fields followed by one full-width MSP field.

### HOME / 10 — MSP lane

**Folio:** `10 / FOR MSPs`

**Heading**

> KEEP THE ACCOUNT. ADD THE AI PRACTICE.

**Copy**

> Dirtyworks.ai gives traditional MSPs a managed AI operations capability without requiring them to build every catalogue, review, training, knowledge, evaluation, governance, and operating method from scratch.

> Referral, co-managed, and white-label structures are available when the client relationship, tenant access, product billing, service desk, data responsibilities, support, brand, margin, and liability are written down.

**Responsibility seam**

- `MSP / ACCOUNTABLE` — agreed infrastructure, identity, security, service desk, and client relationship.
- `DIRTYWORKS.AI / ACCOUNTABLE` — agreed AI product, enablement, knowledge, evaluation, integration, and recurring operating scope.
- `CUSTOMER / ACCOUNTABLE` — business purpose, policy, access approval, source truth, employee use, and consequential decisions.

**Action:** `DESIGN A PARTNER PILOT`

**Layout:** ink or bone full-width split work order; one offset on the Dirtyworks.ai row.

### HOME / 11 — Manifesto

**Display**

> NO THEATRE.  
> NO MYSTERY.  
> WORK THAT WORKS.

**Copy**

> AI gets the spotlight. The work behind it does not.

> Product decisions. Account ownership. User access. Training. Company information. Integrations. Tests. Support. Policy. Monitoring. Incidents. Cost. Change. Exit.

> That is the dirty work. That is the service.

**Layout:** ink band, large declaration left, Instrument Serif final line right; acid may mark only `WORKS`.

### HOME / 12 — Conversion

**Folio:** `12 / MAP THE CURRENT STATE`

**Heading**

> SHOW US WHAT IS ALREADY IN THE STACK.

**Support**

> Bring one recent event: an account nobody owned, a person who could not get access, a tool nobody supports, an integration that failed, a cost nobody expected, or an answer nobody could verify. We will start there.

**Primary action:** `MAP YOUR AI STACK`  
**Secondary action:** `DESIGN AN MSP PILOT`

**Safety note**

> Do not send customer records, credentials, private documents, employee information, or other sensitive data through the website form.

**Layout:** `CTABand` leading to `/start`; do not embed the full form on the homepage.

## 6. Services page

### Page metadata

**Title:** `AI managed services | Dirtyworks.ai`  
**Description:** `Product selection, AI account administration, user onboarding, training, support, integrations, governance, monitoring, knowledge operations, and cost control for Alberta businesses.`

### SERVICES / 01 — Hero

**Display**

> THE TOOL IS ONE LINE ITEM.  
> THIS IS THE SERVICE.

**Support**

> Dirtyworks.ai operates a defined AI portfolio across its full lifecycle—from product choice and user access through training, integration, governance, monitoring, cost review, renewal, and exit.

**Action:** `MAP THE MANAGED SCOPE`

### SERVICES / 02 — Scope register

Use the eight capability rows from Home / 03, expanded into the following fields:

| Service | Included in a scoped engagement | Boundary to state |
|---|---|---|
| Portfolio planning and vendor management | requirements, comparison, prerequisites, overlap, purchasing path, inventory, renewal decision | no claim that every product can be resold or supported |
| Account and user administration | tenant/account setup, named admins, roles, licences, joiner/mover/leaver, recovery, offboarding | customer approves access; general identity administration may remain with MSP/IT |
| Training, adoption, and support | role-based onboarding, acceptable-use guidance, office hours/materials, supported-use triage, adoption blockers | not unlimited training or general IT support |
| Knowledge and data reliability | source selection, ownership, freshness, permissions, evaluation, gaps, company knowledge workflows | customer owns source truth and consequential decisions |
| Integration and automation | approved connectors, low-code/custom integration, tests, exceptions, human approval, monitoring, rollback | each production action requires separate risk and operating scope |
| Governance and compliance readiness | use-case register, policy implementation, risk/decision record, data/vendor review, control evidence, specialist coordination | no legal advice, certification, or guaranteed compliance |
| Monitoring, incident, and change operations | supported health/quality/cost signals, triage, containment, notification, vendor-change review, regression work | third-party uptime and events outside the managed scope are excluded |
| Licence, usage, and cost control | spend inventory, budgets, alerts, reconciliation, overlap review, renewal/exit | savings are measured, not promised in advance |

**Layout:** alternating `OwnerRow` plus short “included / boundary” columns. This page can be dense; use quiet spacing between every two rows.

### SERVICES / 03 — Engagement path

**Heading**

> START WITH THE UNCERTAINTY. END WITH A MANAGED SCOPE.

| Stage | Public description | Commercial treatment |
|---|---|---|
| `REVIEW` | Map the current stack, recent failure events, users, information, integrations, costs, owners, risks, and next decision. | Paid fixed scope when analysis or architecture is required |
| `DEPLOY` | Configure the selected customer-owned products, access, controls, integrations, tests, documentation, and training. | Fixed project or milestone scope |
| `OPERATE` | Manage the defined portfolio, users, support, monitoring, controls, incidents, spend, vendor changes, and reporting. | Monthly managed service |
| `EXTEND` | Add knowledge domains, integrations, assisted workflows, or controlled automation when evidence supports the change. | Scoped change/project plus recurring operating impact |
| `RENEW / EXIT` | Reconcile use and value, change plans, replace products, export records, transfer ownership, or remove access. | Included cadence or scoped transition |

Do not publish package prices until the sponsor approves the broader offer names and live sales evidence supports the rate card.

### SERVICES / 04 — Responsibility boundary

**Heading**

> MANAGED DOES NOT MEAN UNBOUNDED.

**Dirtyworks.ai operates:** the contracted AI portfolio, configuration, users/admin process, knowledge/integration scope, tests, enablement, monitoring, support, change, records, and reporting.

**The customer owns:** business policy, data/source truth, access approvals, employee use, legal/regulatory accountability, budget decisions, and final consequential judgment.

**The MSP/IT provider may own:** tenant-wide identity, endpoints, network, backup, cybersecurity, service desk, and infrastructure. Every account receives a written seam.

### SERVICES / 05 — CTA

**Heading:** `WHAT SHOULD SOMEBODY OWN BY MONDAY MORNING?`  
**Action:** `MAP THE MANAGED SCOPE`

## 7. Catalogue page

### Page metadata

**Title:** `Managed AI product catalogue | Dirtyworks.ai`  
**Description:** `Compose a governed mix of AI, automation, data, and monitoring products, then attach deployment, administration, support, controls, monitoring, and cost management.`

### CATALOGUE / 01 — Hero

**Display**

> CHOOSE THE TOOLS.  
> KEEP ONE OPERATING MODEL.

**Support**

> The catalogue helps a client select a practical product mix without turning every vendor into a separate operating problem. Products are organized by the job they perform, then assessed for fit, ownership, commercial path, controls, deployment work, and recurring support.

**Action:** `COMPOSE A PRODUCT MIX`

### CATALOGUE / 02 — What the catalogue is

**Heading:** `A GOVERNED SHORTLIST. NOT AN OPEN APP STORE.`

Show five approval questions as `ProofLabel`/register rows:

1. `JOB / DEFINED` — What company job does the product perform?
2. `OWNER / NAMED` — Who owns tenant, billing recovery, data, renewal, and exit?
3. `PATH / VERIFIED` — Customer-direct, authorized resale, cloud marketplace, or managed deployment?
4. `CONTROL / ASSESSED` — What information, people, systems, and decisions can it affect?
5. `SERVICE / SCOPED` — What deployment, administration, support, monitoring, and change work is required?

### CATALOGUE / 03 — Product menu

Use the seven category rows from Home / 04. On this page each row may expand to show:

- current candidate products;
- suitable client jobs;
- typical prerequisites;
- default operating tier: Register, Manage, or Operate;
- current catalogue state: Candidate, Conditional, Standard, Suspended, or Retired;
- purchase path and price verification date.

Do not show a buy button. The action is `ADD TO DRAFT PORTFOLIO` or `ASK ABOUT THIS CATEGORY` until the client configurator becomes a real application.

### CATALOGUE / 04 — Commercial route

**Heading**

> WHO SENDS THE SOFTWARE INVOICE DOES NOT DEFINE THE SERVICE.

| Route | Public explanation |
|---|---|
| Customer-direct | The client contracts with the vendor. Dirtyworks.ai deploys and administers the approved account. |
| Authorized resale | Dirtyworks.ai or an authorized channel supplies the applicable product under current contractual rights. |
| Customer cloud/marketplace | The product runs in the client’s cloud subscription; Dirtyworks.ai manages the agreed architecture and operation. |
| Customer-owned managed deployment | Approved software is deployed into client-controlled infrastructure under applicable licence terms. |

**Boundary copy**

> Partner-program membership, a public price page, or technical access does not establish resale authority. The quote confirms the seller of record, current terms, ownership, support, cancellation, and renewal.

### CATALOGUE / 05 — What a quote contains

Show an `ILLUSTRATIVE` product-composer output:

- selected product/plan;
- licence quantity or monthly usage budget;
- managed users;
- vendor charge estimate and who pays it;
- one-time deployment/onboarding work;
- monthly Dirtyworks.ai management;
- prerequisites and minimums;
- approval/verification state;
- assumptions, exclusions, and validity date.

Do not show the current internal fee hypotheses or live vendor prices on the public page.

### CATALOGUE / 06 — CTA

**Heading:** `BRING THE PRODUCTS YOU ALREADY HAVE. ADD ONLY WHAT THE WORK REQUIRES.`  
**Action:** `COMPOSE A PRODUCT MIX`

## 8. Method page

### Page metadata

**Title:** `Managed AI operating method | Dirtyworks.ai`  
**Description:** `How Dirtyworks.ai maps, designs, approves, deploys, stabilizes, operates, improves, renews, and offboards a company AI portfolio.`

### METHOD / 01 — Hero

**Display**

> GOOD AI OPERATIONS BEGIN BEFORE THE LOGIN.

**Support**

> Product choice matters. So do account ownership, source quality, access, training, integrations, support, tests, cost controls, incidents, and exit. We make those decisions visible before production and keep them current afterward.

### METHOD / 02 — Lifecycle work order

Use the seven steps from Home / 07. Expand each step with:

- inputs;
- work performed;
- customer decision/approval;
- output record;
- release or stop gate.

### METHOD / 03 — Valid review outcomes

**Heading:** `SELLING ANOTHER TOOL IS NOT THE REQUIRED OUTCOME.`

`DEPLOY` · `CONSOLIDATE` · `REPAIR FIRST` · `USE A SIMPLER TOOL` · `KEEP IT HUMAN` · `STOP`

**Copy**

> A useful review removes uncertainty. Sometimes that supports deployment. Sometimes it exposes duplicate tools, weak sources, missing ownership, unacceptable risk, or work that does not need AI.

### METHOD / 04 — Monthly operating record

Show a public illustrative extract with:

- managed products and owners;
- users added/removed;
- support and adoption issues;
- integration/service condition;
- evaluated failures and open knowledge gaps;
- access/control changes;
- incidents and corrective actions;
- licence/usage spend against budget;
- vendor changes and renewal decisions;
- next improvement and owner.

Every field must be marked `ILLUSTRATIVE` until real approved customer material exists.

### METHOD / 05 — CTA

**Heading:** `START WITH THE LAST THING THAT FAILED, COST TOO MUCH, OR HAD NO OWNER.`  
**Action:** `START WITH A SCOPED REVIEW`

## 9. Trust page

### Page metadata

**Title:** `AI governance, controls, and operating boundaries | Dirtyworks.ai`  
**Description:** `Customer ownership, access, data/vendor review, human accountability, monitoring, incidents, portability, and honest limits for managed AI operations.`

### TRUST / 01 — Hero

**Display**

> TRUST IS A RECORD OF WORK.

**Support**

> No vendor logo, policy document, or confidence score makes an AI service trustworthy by itself. Trust is built through named ownership, tested access, visible evidence, monitored operation, honest failure, and a clean way out.

### TRUST / 02 — Limitations first

**Heading:** `WHAT WE DO NOT PROMISE.`

- perfect answers;
- complete security;
- universal regulatory compliance;
- uninterrupted third-party services;
- unrestricted support or development;
- autonomous consequential decisions;
- savings before a baseline and measurement method exist;
- support for every AI product or use case.

**Pull quote:** `“I don’t know” is a feature.`

### TRUST / 03 — Public control register

Expand Home / 08 with:

- purpose and accountable owner;
- product/tenant/data ownership;
- approved users and use;
- access and identity;
- data location, retention, training use, and subprocessors;
- source and permission integrity;
- evaluation and failure paths;
- human review;
- usage/cost controls;
- monitoring and incidents;
- vendor/change review;
- export, transfer, deletion, and access revocation.

Each control needs: mechanism, evidence/record, Dirtyworks.ai role, customer/MSP role, and state.

### TRUST / 04 — Compliance-readiness copy

**Heading:** `WE OPERATE CONTROLS. WE DO NOT SELL A COMPLIANCE STICKER.`

> Dirtyworks.ai helps translate the approved use case into practical configuration, access, records, monitoring, review, and escalation work. When legal, privacy, security, employment, engineering, safety, or industry-specific judgment is required, the accountable customer owner and qualified specialists remain part of the process.

### TRUST / 05 — Incident voice

Show an illustrative time-stamped sequence:

```text
10:14 MT / SIGNAL RECEIVED
Materially incorrect answer reported in a supported question class.

10:22 MT / SCOPE CONTAINED
Affected connector disabled. Designated customer contact notified.

11:05 MT / EVIDENCE PRESERVED
Relevant configuration, source, access, and event records retained for review.

NEXT / OWNER NAMED
Root cause, customer impact, corrective action, and release decision recorded.
```

Label it `ILLUSTRATIVE INCIDENT VOICE`, not a historical incident.

### TRUST / 06 — Exit

**Heading:** `DEPENDENCE SHOULD COME FROM VALUE. NOT CAPTIVITY.`

> At offboarding, Dirtyworks.ai removes its access and provides the current inventory, agreed configurations, runbooks, operating records, evaluation material, customer artefacts, vendor actions, and residual-risk list in portable form.

### TRUST / 07 — CTA

**Heading:** `WRITE THE RESPONSIBILITY SEAM BEFORE PRODUCTION.`  
**Action:** `REVIEW THE OPERATING BOUNDARY`

## 10. For MSPs page

### Page metadata

**Title:** `Managed AI operations for MSP partners | Dirtyworks.ai`  
**Description:** `Referral, co-managed, and white-label AI operations for MSPs serving professional-services and energy-services SMBs.`

### MSP / 01 — Hero

**Display**

> KEEP THE ACCOUNT.  
> ADD THE AI PRACTICE.

**Support**

> Dirtyworks.ai supplies the product-catalogue, review, enablement, knowledge, integration, governance, evaluation, and operating method behind a managed AI service. The partner model can be referral, co-managed, or white-label when the responsibilities and economics work.

**Action:** `DESIGN A PARTNER PILOT`

### MSP / 02 — What the practice adds

- governed AI product selection and commercial-route review;
- client AI account and user administration;
- role-based onboarding, training, and supported-use triage;
- company knowledge/source and evaluation operations;
- application integration and controlled automation;
- AI use-case, control, and compliance-readiness records;
- monitoring, incidents, vendor change, spend, and renewal review;
- reusable runbooks, responsibility schedules, and offboarding.

### MSP / 03 — Three models

| Model | Customer relationship | Dirtyworks.ai visibility | Working seam |
|---|---|---|---|
| Referral | MSP introduces; Dirtyworks.ai contracts/delivers | Visible | commercial handoff and coordination |
| Co-managed | MSP and Dirtyworks.ai share delivery under named scopes | Visible/co-branded | explicit RACI, escalation, service desk, access, and margin |
| White-label | MSP leads brand/contract; Dirtyworks.ai performs agreed subcontracted work | Limited as commercially/legal appropriate | subcontract, data role, access disclosure, support, liability, and customer transparency |

Do not publish discounts or wholesale percentages before live partner validation.

### MSP / 04 — Responsibility seam

Use a three-party `OwnerRow` register for MSP / Dirtyworks.ai / Customer covering:

- sales and qualification;
- contract and seller of record;
- product billing and renewal;
- identity, endpoint, network, cloud, and cybersecurity;
- AI account/product configuration;
- source truth and access approval;
- training and service desk;
- evaluation, monitoring, incident, and change;
- privacy/security/legal specialist work;
- reporting, value review, and offboarding.

### MSP / 05 — One-customer pilot

**Heading:** `PROVE THE SEAM WITH ONE CUSTOMER.`

1. Partner discovery and qualification.
2. Select one low/medium-risk client problem and current product environment.
3. Agree customer ownership, responsibilities, sales/contract model, support, and economics.
4. Complete a paid review.
5. Deploy a bounded managed scope.
6. Run a 90-day operating and partner review.
7. Repeat, revise, or stop.

### MSP / 06 — CTA

**Heading:** `BRING ONE CLIENT. WRITE DOWN WHO OWNS WHAT.`  
**Action:** `DESIGN A PARTNER PILOT`

## 11. About page

### Page metadata

**Title:** `About Dirtyworks.ai | Operator-led managed AI services`  
**Description:** `Dirtyworks.ai is an Alberta managed AI operations company built by an experienced CTO and company operator.`

### ABOUT / 01 — Hero

**Display**

> BUILT BY AN OPERATOR.  
> FOR THE WORK AFTER THE DEMO.

### ABOUT / 02 — Provisional founder copy

> Dirtyworks.ai was founded by an experienced CTO and company operator who has spent a career working across technology, people, risk, budgets, vendors, and the less visible work required to keep systems useful after launch.

> The company exists because smaller businesses increasingly depend on AI but cannot always justify building a complete internal AI operations function. They need more than a product recommendation. They need somebody accountable for deployment, administration, training, integration, controls, support, monitoring, cost, and change.

> Dirtyworks.ai is being built as that operating partner—directly for Alberta businesses and alongside traditional MSPs.

**Sponsor inputs required before publication**

- founder name and approved title;
- concise employment/company history;
- specific operating achievements that can be verified;
- relevant professional credentials or memberships;
- approved founder photograph;
- legal company name and formation status;
- why Calgary/Alberta is the chosen market in the founder’s own words.

Do not inflate the biography into “visionary,” “serial entrepreneur,” or “AI pioneer.” Relevant operating evidence is stronger.

### ABOUT / 03 — Operating beliefs

1. A licence is not an operating model.
2. Customer ownership is the default.
3. Experienced employees are not bottlenecks to remove.
4. Unsupported answers should fail visibly.
5. Compliance claims require evidence and accountable specialists.
6. Automation follows understanding.
7. Exit is part of deployment.

### ABOUT / 04 — CTA

**Heading:** `BRING US THE OPERATING PROBLEM. NOT THE AI PITCH.`  
**Action:** `MAP YOUR AI STACK`

## 12. Notes page

### Page metadata

**Title:** `Notes on managed AI operations | Dirtyworks.ai`  
**Description:** `Practical notes on AI products, user administration, knowledge, integrations, governance, monitoring, cost, MSP delivery, and accountable automation.`

Use an editorial index, not blog cards. Each item shows thesis, evidence type, date, and reading time.

### Initial article queue

1. A licence is not an AI operating model.
2. Who owns the employee’s first day with AI?
3. Your AI catalogue needs an exit column.
4. Customer-direct software can still be a managed service.
5. Compliance is not a setting in the admin console.
6. Permission is part of the answer.
7. “Ask Sarah” is your most expensive undocumented system.
8. Before you automate the repeated question, find out why it repeats.
9. A managed AI service needs a failure path.
10. What an MSP owns—and what an AI operator should.
11. The cheapest AI seat is expensive when nobody uses it.
12. Model choice changes. Operating responsibility does not.

Do not fabricate article dates or reading times before the content exists. A launch Notes page with three complete articles is better than twelve empty links.

## 13. Start / diagnostic page

### Page metadata

**Title:** `Map your AI stack | Dirtyworks.ai`  
**Description:** `Tell Dirtyworks.ai what AI products, users, integrations, costs, or operating gaps need an owner—without sending sensitive company information.`

### START / 01 — Hero

**Display**

> SHOW US WHAT IS ALREADY IN THE STACK.

**Support**

> One recent event is enough: missing access, an unmanaged account, abandoned licences, an integration failure, unexpected spend, unclear policy, an unsupported team, or an answer nobody could verify.

### START / 02 — Diagnostic form

**Required fields**

- Name
- Company
- Role
- Work email
- What was somebody trying to do?
- What happened?
- Which product or system was involved?
- Who owns it today, if anyone?

**Optional fields**

- Approximate company size
- Current AI products or product categories
- Approximate number of people using them
- Existing Microsoft, Google, AWS, Azure, or other environment
- Need: product selection / user administration / training / support / integration / governance / monitoring / cost control / knowledge / MSP partnership
- Existing MSP relationship
- Preferred way/time to respond

**Consent/safety copy**

> Do not include passwords, API keys, customer or employee records, private documents, health or financial information, or other sensitive data. By submitting, you agree that Dirtyworks.ai may use the information to respond to this inquiry under the website privacy notice.

**Submit label:** `LOG THE OPERATING GAP`

**Confirmation state**

`RECEIVED / LOGGED`

> We will review the event and respond using the contact details provided. Sending this form does not create a service relationship or authorize access to company systems.

## 14. Cross-page copy system

### One-sentence explanations by audience

**Owner / COO**

> One accountable operating partner for the AI products, people, company information, controls, and costs that otherwise fall between departments and vendors.

**IT / security**

> A documented managed scope for AI products, access, data, integrations, tests, support, monitoring, incidents, change, and exit—inside customer-owned systems by default.

**Employee / knowledge holder**

> Approved tools, clear guidance, useful support, and a way to make company answers easier to find without treating experienced staff as a system to replace.

**MSP**

> Add an AI operations practice to the client relationship with a governed catalogue, delivery method, responsibility seam, and recurring operating model.

### Short service description

> Dirtyworks.ai selects, deploys, administers, trains, integrates, governs, monitors, and controls costs across a defined company AI portfolio.

### Extended service description

> Dirtyworks.ai is an AI managed service provider for Alberta businesses. We help select and source approved products, establish customer-owned accounts, manage users, train and support teams, connect applications and company knowledge, operate practical controls, monitor services and incidents, and keep licence and usage costs visible. Traditional MSPs can use the same capability through referral, co-managed, or white-label structures.

### Trust line

> Customer-owned by default. Human accountability stays human.

### Product line

> Choose the tools. Keep one operating model.

### MSP line

> Keep the account. Add the AI practice.

## 15. SEO and social copy

### Homepage

**Title:** `Dirtyworks.ai | Managed AI operations for Alberta businesses`  
**Meta description:** `An AI MSP for product selection, account and user management, training, integrations, knowledge, governance, monitoring, support, and cost control.`

### Social preview

**Headline:** `AI is already at work. Is anyone operating it?`  
**Description:** `Dirtyworks.ai manages the tools, people, company information, controls, and costs behind business AI.`

Use a type-led social image built from the design system. Do not use robots, brains, glowing networks, or an unsourced metric.

## 16. Responsive content behaviour

- Preserve headline meaning before preserving extreme scale. Do not crop a word needed to understand the offer on mobile.
- Registers become stacked records with the label above the value; do not create horizontal scrolling for core content.
- Comparisons stack row by row as `Product access` followed by `Managed AI operations`; preserve their pairing.
- Work-order steps remain numbered and sequential.
- Product categories become accordion/editorial rows. The default state shows job and operating emphasis; candidate products can expand.
- CTA labels remain specific. They may wrap to two lines but should not be shortened to `START` or `MORE`.
- Forms use one column, persistent labels, visible errors, and 44px minimum targets.
- Mobile footer preserves legal/contact information even if editorial links collapse.

## 17. Content and claim states

Use visible production annotations during design; remove internal annotations only when the state is resolved.

| State | Treatment | Current examples |
|---|---|---|
| `APPROVED METHOD CLAIM` | Publishable after final copy review | customer ownership default; scoped deployment/admin/training/monitoring method |
| `WORKING OFFER NAME` | Sponsor decision required | broader paid review, managed deployment, and recurring AI operations names |
| `VERIFY AT QUOTE` | Publish boundary, not a specific promise | vendors, prices, plan minimums, resale rights, availability |
| `ILLUSTRATIVE` | Keep label visible | hero portfolio, problem events, monthly record, incident sequence |
| `EVIDENCE REQUIRED` | Do not publish as fact | savings, accuracy, adoption improvements, response performance, customer outcomes |
| `LEGAL REVIEW` | Publish only after review | privacy, terms, compliance wording, form consent, contracts/service levels |

## 18. Design and coding handoff checklist

### Ready now

- page hierarchy and routes;
- homepage narrative and draft copy;
- full service capability register;
- catalogue taxonomy and commercial-route explanation;
- method, trust, and MSP page structures;
- CTA system and form fields;
- component mapping to the supplied design system;
- responsive content behaviour;
- claim-state rules.

### Required before public launch

- sponsor approval of the broader public offer names;
- approved legal entity name, email, telephone if used, and business address treatment;
- final founder name, biography, credentials/evidence, and photograph;
- privacy notice, website terms, accessibility statement, and form data path;
- confirmation of supported product shortlist and any authorized reseller/partner statements;
- final support boundaries and service-availability wording;
- at least one real or visibly illustrative operating example;
- three complete Notes articles if Notes launches;
- analytics/cookie decision and consent implementation if required;
- accessibility, performance, security-header, form-abuse, and mobile QA;
- review that no fabricated logos, testimonials, certifications, results, or vendor relationships appear.

### Explicitly out of scope for this handoff

- visual redesign of the supplied design system;
- Figma or production code;
- working client product configurator;
- live vendor pricing or checkout;
- CRM/form integration;
- legal advice or compliance certification;
- photography creation;
- customer case-study fabrication.

## 19. Open sponsor choices

These choices affect public emphasis but do not prevent design exploration:

1. **Lead category wording:** `AI MSP`, `managed AI operations`, or both. This handoff uses both: plain category first, acronym in explanation.
2. **Primary action:** `MAP YOUR AI STACK` versus `SHOW US WHAT NEEDS AN OWNER`. The first is clearer; the second is more distinctive.
3. **Public catalogue depth:** seven category rows only, or expandable candidate products. Do not expose prices in either version.
4. **Commercial offer names:** retain Knowledge Reliability Review/Launch/Operations as the first wedge, or rename the umbrella to AI Operations Review/Deployment/Operations while preserving knowledge-specific modules.
5. **Launch site size:** full multi-page site, or Home + Trust + For MSPs + Start first. Both use the same content system.

### Two viable launch scopes

| Scope | Includes | Strength | Constraint |
|---|---|---|---|
| Focused launch | Home, Trust, For MSPs, Start, legal/footer | Faster and enough for early conversations | Services/catalogue/method detail remains on homepage |
| Full launch | All pages in this document | Stronger buyer self-education and design range | More content, QA, legal review, and maintenance before evidence exists |

The current recommendation is the **focused launch** for private/early validation, with Services, Catalogue, and Method designed as section anchors that can become pages without changing the narrative. The sponsor may choose the full launch if the site is primarily a design/business-in-a-box asset rather than an immediate public release.
