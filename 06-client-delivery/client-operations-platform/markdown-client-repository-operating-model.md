# Markdown client repository operating model

**Version:** 0.1  
**Date:** 2026-08-26  
**Owner:** Service operations  
**Status:** Sponsor-directed working architecture; validate with a synthetic client before production  
**Related:** [client repository template pack](../../90-templates/client-operations-repository/README.md), [first-customer onboarding checklist](../onboarding/first-customer-onboarding-checklist.md), [agent-operated service platform blueprint](../../11-technology-and-data/architecture/agent-operated-service-platform-blueprint.md)

## Decision

Dirtyworks.ai will use **one private Git-backed Markdown repository per end customer** as the initial source for private operating knowledge. An internal interface may read and propose changes to these repositories. `personal-wiki` is the candidate compiler/review mechanism and `kgmd` is the candidate rebuildable search/knowledge-graph layer.

Freshdesk remains the customer-facing request and communication authority. 1Password remains the secrets authority. Vendor, identity, contract and finance systems remain authoritative for the facts they create. Markdown connects, explains and reconciles these sources; it does not replace them.

Hudu is no longer required for launch. It remains a migration or integration option if collaboration, audit, portal, permission or maintenance needs exceed the file-based model.

## Why this can work

The architecture fits three existing strengths:

1. Dirtyworks.ai already operates its company documentation as readable source files.
2. `personal-wiki` already provides Git-backed workspaces, configurable page types, source lineage, deterministic validation and human-reviewed proposals.
3. `kgmd` already builds an incremental SQLite knowledge graph and MCP read surface from a Markdown corpus.

The mechanism is:

```text
Approved source/evidence files
              │
              ▼
    personal-wiki ingestion
      and proposed pages
              │
        human review/accept
              │
              ▼
  Published Markdown on main  ◄── operator-authored records
              │
        ┌─────┴─────────┐
        ▼               ▼
 internal interface   kgmd graph/MCP
        │               │
        └──────┬────────┘
               ▼
       sourced read/request agent

Writes: proposal or work request → approval → native action → verification → Markdown update
```

The published Markdown branch is authoritative for Dirtyworks.ai's private procedure and reconciled operating view. Search indexes, rendered pages, databases, graph entities and agent memories are derived and disposable.

## Repository and tenant boundary

### Required boundary

- One repository per end customer, including MSP-sourced/white-label customers.
- One knowledge-graph database and one interface workspace per client repository.
- No cross-client corpus, embedding index, graph database, prompt context or agent session by default.
- The company documentation repository contains shared standards and sanitized templates, not customer production records.
- A separate MSP coordination repository may contain partner-level procedures and responsibility seams, but not copies of every end-customer record.

This boundary compensates for Git's weak folder-level authorization and reduces accidental cross-customer retrieval. It does not by itself create authorization: repository, device, identity, model-provider and backup access must also be controlled.

### Repository identifiers

Use a non-sensitive stable repository name and customer ID. Do not place confidential project names, personal information or contract details in the repository URL.

Example:

```text
dw-client-c0007
```

The internal account record maps `c0007` to the legal customer. The global portfolio index should hold only the minimum metadata needed to locate a repository: customer ID, repository locator, service owner, lifecycle and next review.

## Authority model

| Operational fact | Authority | Markdown record |
|---|---|---|
| Customer request, response, priority and ticket state | Freshdesk | Link the ticket; retain only durable operating learning |
| Password, secret, recovery material and token | 1Password | Store item reference, purpose, scope, owner and review date—never the value |
| Signed legal language | Contract repository | Store agreement ID/link and operational obligations; never replace the signed text with a summary |
| Current user, role, tenant setting and native activity | Vendor/identity system | Store observed snapshot, source, verifier, date and reconciliation result |
| Issued invoice and payment | Vendor plus accounting/AP | Store normalized period/amount/variance and evidence link |
| Dirtyworks.ai procedure, responsibility, review and reconciled view | Published Markdown | Full operational record with evidence and relationships |
| Search result, graph entity or agent answer | Derived interface/kgmd | Must cite the Markdown page and disclose freshness; verify native state before action |

An interface must never silently copy a derived graph value back into Markdown as fact. It creates a proposal or work item containing the source, intended change and verification requirement.

## Workspace layers

The proposed repository follows the current `personal-wiki` contract rather than inventing a second compiler:

| Layer | Purpose | Tracking policy |
|---|---|---|
| `config/` | Workspace schema, provider, prompt and connection policy | Tracked; reviewed like code |
| `raw/` | Imported originals accepted into the evidence system | Tracked only when approved for the repository retention policy |
| `wiki/` | Flat published Markdown pages | Tracked; authoritative operating source |
| `changes/` and proposal refs | Human review and publication workflow | Follow personal-wiki's tracked/ref contract |
| `state/` tracked artifacts | Source registry, lineage and reproducible publication artifacts | Follow personal-wiki's contract |
| `.kgmd/graph.db` and embeddings | Rebuildable derived client graph containing client information | Untracked, access-controlled and deletable |
| `templates/` | Human/source templates used to create authored pages | Tracked but excluded from kgmd/published page ingestion |

The `wiki/` namespace remains flat because `personal-wiki` currently enforces `wiki/<page-id>.md`. The interface groups pages by type; directory location does not encode the record type.

## Published page contract

Use the current `personal-wiki` frontmatter fields without expansion in the first experiment:

```yaml
---
id: requirement-admin-mfa
title: Administrative accounts require MFA
type: requirement
status: accepted
summary: Every supported product administrator must use a named account with MFA where available.
source_ids: [src-0004]
owner: access-security-owner
created_at: 2026-08-26
updated_at: 2026-08-26
review_by: 2026-11-26
tags: [class-confidential, control-access]
---
```

### Field rules

| Field | Rule |
|---|---|
| `id` | Stable, lowercase, hyphenated; never reuse after retirement |
| `title` | Human-readable statement or record name |
| `type` | Declared in `config/schema.yaml`; determines required sections and lifecycle |
| `status` | One of the type's allowed states; status changes require `updated_at` |
| `summary` | Current conclusion in 500 characters or fewer; no unsupported claim |
| `source_ids` | Imported evidence IDs used by the page; unique and relevant |
| `owner` | Accountable role or named operator; not merely the last editor |
| `created_at` | First publication date; immutable |
| `updated_at` | Last material operating change, not formatting-only touch |
| `review_by` | Required for active operational pages; no silent evergreen records |
| `tags` | Small controlled facets; not a substitute for page type or relationships |

### Classification tags

Every operational page uses exactly one:

- `class-internal` — Dirtyworks.ai method with no customer-confidential facts;
- `class-confidential` — ordinary customer operating information;
- `class-restricted` — sensitive security, privacy, financial or incident context requiring narrower handling.

The repository is the primary tenant boundary. Tags help handling and display but must never be the sole authorization control.

## Page types

The template schema defines these types:

| Type | Purpose | Typical authorship |
|---|---|---|
| `account` | Customer charter, contacts, scope boundary and system identifiers | Authored |
| `requirement` | Accepted atomic contractual, security, vendor, service or customer dependency | Authored after human promotion/entry |
| `finding` | Source-backed candidate requirement, risk, product, decision or gap awaiting disposition | Synthesized proposal |
| `service` | Contracted managed-service unit, responsibilities, targets and lifecycle | Authored |
| `product` | Product/tenant, administration, cost/renewal and exit facts | Authored |
| `access` | Privileged or material access authorization/reference/review | Authored |
| `process` | Runbook with authority, verification, exception and rollback | Authored |
| `training` | Audience, material version, delivery/completion and follow-up | Authored |
| `cost` | Periodic licence/usage/invoice reconciliation and action | Authored |
| `risk` | Risk, consequence, control, owner, acceptance and expiry | Authored or proposed |
| `decision` | Durable choice, reason, alternatives and consequences | Authored or proposed |
| `change` | Requested/approved implementation with verification and rollback | Authored |
| `incident` | Private operating summary linked to Freshdesk/incident authority | Authored |
| `review` | Onboarding, monthly, quarterly, renewal or offboarding review | Authored |
| `person` / `organization` | Stable relationship entities used by other pages | Authored |
| `source` | Imported evidence with immutable lineage | Synthesized by personal-wiki |

Do not add a page type for every vendor or minor workflow. Page types represent stable governance/lifecycle differences. Products and variations belong in page content, relationships and controlled tags.

## Relationship protocol

Links make the Markdown navigable and give both a deterministic parser and `kgmd` clearer graph evidence. Use a required `## Relationships` section where the schema calls for it.

```markdown
## Relationships

- `applies-to` -> [[service-page-id|Managed workforce AI]]
- `operated-on` -> [[product-page-id|ChatGPT workspace]]
- `approved-by` -> [[person-page-id|Alex Morgan]]
- `implemented-by` -> [[process-page-id|Administrative MFA setup]]
```

Initial predicate vocabulary:

| Predicate | Meaning |
|---|---|
| `owned-by` | Accountable operating owner |
| `approved-by` | Person/role with decision authority |
| `applies-to` | Requirement/risk/decision governs another record |
| `depends-on` | Record cannot operate or complete without another |
| `operated-on` | Process/change acts on a product/service |
| `implemented-by` | Requirement/control is fulfilled through a process/change |
| `implements` | Process/change fulfills a requirement/control |
| `supported-by` | Service/product uses another product, source or organization |
| `escalates-to` | Issue/process routes to a person, organization or service |
| `replaces` | New record supersedes an older record |
| `produced-by` | Review/evidence/result came from a process/change |
| `related-to` | Meaningful relationship not covered by a stronger predicate |

Relationship direction is always subject page → linked object. Use `related-to` sparingly. Do not infer authorization from a graph edge.

## Source ingestion and requirement extraction

### Drop-zone mechanism

The internal interface may provide an approved drop zone. Files are not immediately operational truth:

1. identify client repository and uploader;
2. malware/type/size screen;
3. classify information and confirm provider/retention eligibility;
4. register and parse exactly once through personal-wiki;
5. propose atomic cited findings identifying candidate requirements, risks, products, decisions and relationships;
6. validate citations, contradictions and unsupported sections;
7. human reviews the source-backed diff;
8. accept/reject the finding proposal without changing operational state;
9. explicitly promote accepted findings into operator-authored requirement, risk, product, decision or other current-state pages;
10. rebuild search and the client-local knowledge graph;
11. create implementation/change work separately where required.

Extraction is discovery, not execution. A newly extracted contractual finding does not change a tenant, promise a service level, approve access or become an accepted operational requirement.

### Git-retention constraint

`personal-wiki` preserves imported originals and lineage in Git. Git history is intentionally difficult to erase selectively. Therefore Dirtyworks.ai must not indiscriminately ingest:

- credentials, recovery codes or tokens;
- bulk customer content or employee records;
- highly sensitive incident evidence;
- unredacted financial/account data when a reference is sufficient;
- documents whose required deletion/retention terms conflict with durable Git history;
- any file that the approved model provider is not permitted to process.

For these records, store a minimal external-source reference or an approved redacted extract. Before production, choose and document whether customer source originals are (a) approved/redacted Git evidence, (b) retained outside Git and referenced, or (c) stored in Git with a tested expiry/history-removal procedure.

## Personal-wiki role

Use `personal-wiki` for:

- workspace initialization and Git-backed publication;
- parsing and immutable source lineage;
- configurable page-type and lifecycle validation;
- source-backed synthesis into proposals;
- deterministic health checks;
- human acceptance/rejection and reviewable diffs;
- readable navigation/search artifacts.

The proposed [schema](../../90-templates/client-operations-repository/config/schema.yaml) fits the current version-2 schema and fixed frontmatter model. The main adaptation is a new recipe and operational page types; a frontmatter-model change is not required for the first experiment.

Current personal-wiki validates required sections for synthesized pages but deliberately does not enforce section completeness on authored pages. The client-repository generator/interface must therefore add a deterministic operational lint that checks authored pages for the schema's required sections, owner, `review_by`, exactly one classification tag and valid controlled relationship syntax. The schema repeats required authored headings in `suggested_sections` so `wiki page new` produces the complete scaffold rather than an empty human page.

Operator-authored current-state pages and machine-synthesized finding/source pages must both pass the published page contract appropriate to their authorship. `personal-wiki` currently prohibits generation from targeting authored page types; the internal interface must preserve that boundary. LLM-generated changes never publish directly, and a finding becomes operational state only through an explicit human promotion step.

## kgmd role

Use one `kgmd` corpus per client repository, restricted to published `wiki/` pages.

Use it for:

- semantic search across operating pages;
- entity lookup and relationship navigation;
- finding nearby requirements, products, processes, owners and risks;
- MCP read queries for the internal agent;
- discovering missing or inconsistent relationships for human review.

Do not use it as authority for:

- current tenant configuration;
- ticket or approval state;
- invoice or payment facts;
- authorization to act;
- exact contract language;
- automatic Markdown mutation.

`kgmd` extracts relations with an LLM, resolves duplicates probabilistically and induces its schema. The graph can be incomplete or wrong. Every operational answer must return the supporting page path/ID and its `updated_at`/`review_by`; high-impact answers must also verify the authoritative source.

The local embedding default does not make the whole build local: current `kgmd` entity/relation extraction uses an LLM provider. Provider selection, client authorization, data-use terms and permitted classifications must be evaluated per client. `.kgmd/graph.db` is untracked but contains derived customer information and must receive the same endpoint/access/deletion protection as the repository.

### Required kgmd adapter before production

The current kgmd implementation is a useful base but should not be pointed unmodified at a production client workspace. The repository wrapper/adaptation must:

1. index published `wiki/*.md` pages while excluding personal-wiki reserved/generated `index.md` and `log.md` pages;
2. parse frontmatter rather than treating YAML as ordinary prose;
3. attach page ID, type, status, owner, `updated_at`, `review_by`, classification and path to indexed chunks/results;
4. parse controlled `Relationships` bullets into deterministic directed edges with page provenance;
5. reserve LLM relation extraction for implicit relationships and visibly distinguish inferred from declared edges;
6. return evidence page/chunk and freshness for every entity/relationship answer;
7. preserve deletion/incremental rebuild behavior when a published page is removed or replaced;
8. reject an attempted corpus path outside the resolved client repository and run one MCP process/session per authorized client boundary;
9. exclude raw sources, templates, proposals, logs, secrets and interface session state;
10. support an approved-provider or no-LLM mode appropriate to the page classification.

Until this adapter passes the synthetic test, kgmd is an experimental retrieval aid. Direct Markdown search remains the reliable fallback.

## Internal interface contract

### Read operations

The interface may:

- browse and filter pages by type, status, owner, tag and review date;
- search Markdown and the derived graph;
- show relationships and source lineage;
- identify missing fields, broken links, overdue reviews and inconsistent status;
- answer questions with page/source citations and freshness;
- show Freshdesk/vendor/contract/finance links subject to the user's authorization.

### Write operations

The interface must not directly rewrite published pages or privileged vendor state. It may:

1. create an authored draft or proposal;
2. show exact changed pages and evidence;
3. collect required approval;
4. publish through the personal-wiki/Git review mechanism;
5. for native actions, create an approved work card;
6. execute only through a typed authorized connector or human procedure;
7. read after write and capture verification;
8. propose the resulting Markdown update.

No unattended action may grant privileged access, delete data, accept legal terms, make a crisis communication, approve spend, change a consequential policy or cross a customer repository boundary.

## Freshdesk workflow

Freshdesk remains the human/customer work queue:

```text
Customer request in Freshdesk
        ↓
Link applicable Markdown requirement/process/product
        ↓
Approval and execution according to runbook
        ↓
Native verification
        ↓
Customer response in Freshdesk
        ↓
Proposal for durable Markdown update if operating knowledge changed
```

Do not ingest every ticket into the wiki. Promote only durable knowledge: recurring cause, approved change, incident summary, new requirement, runbook correction or customer decision.

## Security and continuity baseline

- Private repository and separately authorized remote per client.
- Named accounts, MFA and least privilege for Git, interface, model provider and local workspace.
- Managed encrypted devices; no shared local OS account.
- 1Password references only; secret scanning before commits and pushes.
- Protected published branch and review for machine-generated/material changes.
- Encrypted backup or remote mirror plus tested recovery from a fresh clone.
- No repository contents in logs, analytics, crash reports or debug captures by default.
- Repository-level client offboarding: revoke access, export, apply retention/deletion decision, remove local clones and derived graph/cache.
- Separate model-provider and data-handling decision for `class-restricted` pages.
- Record all agent/tool writes, proposal IDs, approver and verification result.

Git provides change history, not a complete read-access audit. A client requiring read-event audit, granular document-level permissions or legal-hold/retention features may require a different repository host, encrypted document system or Hudu-class platform.

## Synthetic acceptance test

Create one fictional customer repository and prove:

- [ ] workspace initializes from the proposed recipe and validates the schema;
- [ ] two source files produce cited finding proposals for candidate requirements/products/risks;
- [ ] unsupported or contradictory requirements remain visible rather than silently resolved;
- [ ] human accepts one finding proposal, rejects another and promotes the accepted finding into an authored operational page;
- [ ] authored service, access, process, cost and review pages pass validation;
- [ ] the operational authored-page lint rejects a missing required section, owner, review date, classification tag and malformed relationship;
- [ ] controlled relationship bullets create usable links and discoverable graph relations;
- [ ] kgmd indexes only the selected client's published wiki pages;
- [ ] kgmd excludes reserved pages/frontmatter noise and distinguishes deterministic declared edges from inferred edges;
- [ ] agent answers ten operating questions with page IDs and freshness;
- [ ] an overdue `review_by`, broken relationship and missing owner surface as findings;
- [ ] a Freshdesk-style request links to a process and results in a verified change proposal;
- [ ] a secret fixture is rejected and does not enter Git, logs, prompts or graph state;
- [ ] a second client repository cannot be searched or referenced from the first session;
- [ ] monthly cost reconciliation and variance review are completed from synthetic evidence;
- [ ] offboarding exports readable Markdown, revokes access and deletes derived graph/cache;
- [ ] fresh-clone recovery reconstructs the published wiki and rebuildable interface/graph.

## Adoption and migration triggers

Continue Markdown-first while it remains reliable and economic. Consider Hudu or another controlled documentation platform when any of these is observed:

- more than two operators need frequent concurrent updates;
- repository administration or repeated merge/review conflict exceeds the recorded threshold;
- a partner requires access that cannot be safely represented at repository level;
- read-access audit or granular document permission is contractually required;
- review/renewal work is repeatedly missed despite automated health queues;
- customer document self-service is required beyond Freshdesk articles;
- retention/legal-hold requirements conflict with Git history;
- interface and maintenance work exceeds an available platform's total cost;
- the internal interface becomes an accidental custom PSA rather than a narrow Markdown control surface.

## Measured experiment

For the synthetic client and first three production clients, record:

- setup and onboarding hours;
- pages and source files by type/classification;
- proposal acceptance/rejection/correction rates;
- time to answer ten common operating questions;
- stale/broken/missing-record findings;
- Markdown maintenance and merge-conflict time;
- kgmd false merge, missing relationship and unsupported-answer cases;
- monthly cost-close time and corrections;
- access/admin time per repository;
- recovery and offboarding test result;
- whether a platform would have eliminated measured work rather than merely changed its location.

## Open production decisions

1. Approved Git host, region, backup and repository-access model.
2. Customer-original retention model: redacted Git evidence, external reference or full tracked source with expiry/history-removal procedure.
3. LLM provider and permitted data classifications for personal-wiki and kgmd extraction.
4. Whether operator-authored pages use direct reviewed commits or the same proposal mechanism as generated pages.
5. Global portfolio metadata permitted outside individual client repositories.
6. MSP access model: Dirtyworks-owned repository, partner-owned repository or controlled mirror/handoff.

None prevents schema/template development or a synthetic test. They are production gates before customer information is ingested.
