# Managed AI product catalog and commercial model

**Version:** 0.1  
**Date:** 2026-08-25  
**Status:** Working commercial design; vendor pricing, partner status, and resale rights require quote-time verification

## Purpose

Dirtyworks.ai can give a client a practical menu of AI, knowledge, automation, and data products, then deploy and operate the selected mix. The catalogue is not an unconstrained app store. It is a governed shortlist that makes five things explicit before a product is sold or administered:

1. what business job the product performs;
2. who owns the tenant, contract, billing relationship, and data;
3. how Dirtyworks.ai is commercially allowed to participate;
4. what deployment and recurring operating work is required; and
5. what must be checked before a quote becomes an order.

The working default is **customer-owned tenant and billing, Dirtyworks-managed operation**. That permits Dirtyworks.ai to create recurring value even when no resale margin is available. Resale is an optional commercial rail, not the proposition.

## Why the model works—and where it breaks

A buyer does not primarily need another licence seller. They need a coherent product mix, fewer unmanaged accounts, dependable configuration, user lifecycle administration, spend control, policies, support, and a path to remove or replace tools. Those responsibilities can support a managed-services fee regardless of who invoices the software.

The model breaks if Dirtyworks.ai:

- implies reseller rights it has not secured;
- carries large licence or consumption exposure without deposits, credit controls, and contract protection;
- treats every product as deployable without privacy, security, identity, data-residency, and use-case review;
- creates vendor lock-in or owns the customer tenant by default;
- supports an unlimited long tail of tools without standard runbooks and minimum account economics; or
- bundles volatile usage into a fixed price without an allowance and overage mechanism.

## Client-facing menu architecture

The public menu should be organized by the work a client wants done, not by vendor logo.

| Menu | Client job | Example candidates | Typical operating work |
|---|---|---|---|
| **WORK** | General assistants for writing, analysis, and internal work | ChatGPT Business, Claude Team, Microsoft 365 Copilot, Google Workspace with Gemini | tenant setup, identity, roles, policy, enablement, adoption, support |
| **FIND** | Research and governed knowledge access | Perplexity Enterprise, ChatGPT, Claude, Microsoft Copilot, Google Gemini | source boundaries, retention settings, evaluation, permissions, reporting |
| **MAKE** | Images, presentations, meeting records, and content | Midjourney, Canva Business, Fathom, Notion Business | brand controls, user register, content policy, records handling, training |
| **BUILD** | Models, APIs, coding, and application development | OpenAI API, Anthropic API, OpenRouter, GitHub Copilot, Azure OpenAI, AWS Bedrock, Vertex AI | cloud/account architecture, keys, budgets, model policy, evaluations, change control |
| **MOVE** | Workflow and task automation | Zapier, Make, n8n | connection inventory, credential design, testing, monitoring, exceptions, rollback |
| **HOLD** | Application data and semantic search | Supabase, Pinecone | tenancy, access, backup, capacity, retention, cost monitoring |
| **WATCH** | Tracing, evaluation, and model operations | Langfuse, LangSmith | telemetry design, access, test sets, alerts, incident and cost review |

These are candidates, not automatic recommendations. A buyer may choose individual products, but Dirtyworks.ai retains the right to mark a selection **Ready**, **Assessment required**, **Custom architecture**, or **Not supported**.

## Commercial pathways

| Code | Path | Mechanism | Quote and contract treatment |
|---|---|---|---|
| `CUST-DIRECT` | Customer-direct / administer-only | Client contracts with and pays the vendor; Dirtyworks.ai receives delegated or named admin access | Show vendor cost as an estimate paid directly; invoice deployment and management separately |
| `AUTH-RESELL` | Authorized resale | Dirtyworks.ai or its distributor is contractually permitted to resell the specific SKU and geography | Use only after authorization, current price book, taxes, credit, renewal, support, and cancellation rules are documented |
| `CLOUD-MKT` | Customer cloud / marketplace | Product is purchased in the client’s Azure, AWS, Google Cloud, or other approved account | Client pays consumption; Dirtyworks.ai manages architecture, configuration, spend, and operation |
| `OSS-MANAGED` | Customer-owned managed deployment | Software is deployed into client-owned infrastructure under a licence that permits the intended use | Charge for design, infrastructure, deployment, updates, security, backup, and support; complete a licence review |
| `PARTNER` | Referral, services partner, or co-sell | Vendor may provide leads, enablement, or services collaboration | Do not infer resale or margin rights from partner membership |
| `VERIFY` | Commercial status unresolved | Public information is incomplete, volatile, or contract-specific | Do not issue a binding licence quote until resolved |

Microsoft’s [Cloud Solution Provider program](https://partner.microsoft.com/en-us/partnership/cloud-solution-provider) and Google’s [Workspace reseller program](https://support.google.com/channelservices/answer/9400042?hl=en) are real resale paths, but Dirtyworks.ai is not recorded as authorized in this repository. OpenAI’s [partner network](https://openai.com/business/partners/) and Anthropic’s [services partner track](https://www.anthropic.com/news/services-track-partner-hub) support partner delivery; membership or programme availability alone does not establish a right to resell licences.

## Initial candidate catalogue

The companion workbook contains the structured catalogue, current public price assumptions, URLs, and quote controls. This is the recommended starting breadth; a launch menu should initially support only the products used by real prospects.

| Category | Candidate products | Working commercial posture |
|---|---|---|
| Workforce AI | ChatGPT Business; Claude Team; Microsoft 365 Copilot Business and Copilot Chat; Google Workspace Business Standard; Perplexity Enterprise Pro | Customer-direct by default; Microsoft/Google may move to authorized resale later |
| Team and creative | GitHub Copilot Business; Notion Business; Canva Business; Midjourney Pro/Mega; Fathom | Customer-direct; administer where the product exposes suitable organization controls; verify Fathom price at quote |
| Model/API access | OpenAI API; Anthropic API; OpenRouter; Azure OpenAI; AWS Bedrock; Vertex AI | Customer cloud/vendor account with an explicit monthly consumption estimate and budget control |
| Automation | Zapier Team; Make Teams; n8n | Customer-direct or customer-owned deployment; workflows require connection, test, exception, and rollback records |
| Data and search | Supabase Pro; Pinecone Standard | Customer-direct; treat production data systems as critical managed platforms |
| Model operations | Langfuse Core or self-hosted; LangSmith Plus | Customer-direct or licence-reviewed self-hosting; usage charges remain separate |

### Current public-price anchors

The configurator uses public prices only as editable planning inputs. Examples captured on 2026-08-25 include:

- ChatGPT Business Standard at USD 20 per seat/month on annual billing; OpenAI states Business is for 2–200 users ([OpenAI pricing](https://openai.com/business/pricing/?LanguageId=1)).
- Claude Team at USD 25 per person/month on annual billing, with a five-member minimum ([Anthropic pricing](https://www.anthropic.com/pricing), [Team minimum](https://support.anthropic.com/en/articles/9267247-how-do-i-get-started-with-the-team-plan)).
- OpenRouter pay-as-you-go model charges plus a stated 5.5% credit-purchase fee; BYOK has separate terms ([OpenRouter pricing](https://openrouter.ai/pricing), [FAQ](https://openrouter.ai/docs/faq)).
- Midjourney monthly list prices of USD 10/30/60/120 for Basic/Standard/Pro/Mega, with a 20% annual discount; organizations over USD 1 million gross revenue must use Pro or Mega ([Midjourney plan comparison](https://docs.midjourney.com/hc/en-us/articles/27870484040333-Comparing-Midjourney-Plans)).
- Microsoft 365 Copilot Business Canadian public pricing includes promotional and commitment-specific amounts and requires a qualifying Microsoft 365 plan ([Microsoft Canada pricing](https://www.microsoft.com/en-ca/microsoft-365-copilot/pricing)).
- Google Workspace Canadian business plans include Gemini features; Business Standard is listed at CAD 18.40 per user/month on annual commitment at the captured date ([Google Workspace Canada](https://workspace.google.com/intl/en_ca/business/)).
- GitHub Copilot Business is listed at USD 19 per granted seat/month; GitHub currently flags a self-service organizational signup constraint that must be checked at order time ([GitHub plan documentation](https://docs.github.com/en/copilot/get-started/plans)).
- Perplexity Enterprise Pro is listed at USD 40 monthly or USD 400 annually per seat ([Perplexity onboarding guide](https://www.perplexity.ai/help-center/en/articles/12742827-perplexity-enterprise-onboarding-guide)).

Prices exclude tax, foreign exchange, consumption overages, prerequisites, and contract-specific terms unless the quote says otherwise. Promotional prices and public web pages can change without notice.

## Dirtyworks.ai management model

The first quoting tool exposes three adjustable operating tiers. They are pricing hypotheses, not a public rate card.

| Tier | Suitable for | Working one-time platform fee | Per-user onboarding | Working monthly platform fee | Per-user monthly admin | Operating scope |
|---|---|---:|---:|---:|---:|---|
| **Register** | Low-risk user tools with limited integration | $500 | $25 | $150 | $5 | owner/billing register, basic setup, licence changes, quarterly inventory |
| **Manage** | Workforce platforms connected to business information | $1,500 | $50 | $450 | $12 | lifecycle administration, core policy/configuration, spend controls, support triage, monthly review |
| **Operate** | APIs, automation, databases, or business-integrated platforms | $3,500 | $75 | $1,000 | $20 | architecture/runbook, monitoring, incidents, cost controls, change and recovery procedures |

All amounts are CAD before tax. The platform fee recognizes that three seats still require tenant, policy, support, and vendor-management work. The per-user fee recognizes lifecycle volume. Custom integrations, workflow changes, data cleanup, identity projects, privacy/security work, and usage charges remain separate.

### Three models to test with buyers

The workbook implements the transparent line-item model, but the company should preserve three real options:

1. **Transparent operating layer:** vendor costs estimated separately; Dirtyworks.ai charges per platform plus managed user. This is easiest to audit and works without resale rights.
2. **Portfolio bundle:** a monthly price covers a defined number of approved tools, users, reviews, and changes. This is easier to buy but requires stronger scope boundaries and measured delivery cost.
3. **Authorized resale plus management:** software and service may appear on one invoice. It can improve buying convenience, but introduces working-capital, tax, renewal, cancellation, and vendor-concentration risk. Any margin should improve economics, not replace the management fee without evidence.

The sponsor can choose which model to test first. The current workbook defaults to option 1 because it exposes the economics most clearly.

## Quote formula and presentation

For each selected item:

```text
Estimated vendor monthly cost (CAD)
  = quantity × public or overridden unit price × quote-time FX

Dirtyworks.ai one-time fee
  = platform setup + (quantity × per-user onboarding) + scoped services

Dirtyworks.ai monthly fee
  = platform management + (quantity × per-user administration)

Estimated first-month total
  = vendor estimate + one-time fee + monthly management
```

Usage products use an estimated monthly budget rather than seats. Annual-commitment prices are shown as monthly equivalents, while the quote must state whether the vendor invoices annually, monthly, or by consumption. Customer-direct vendor estimates are informational and should not be presented as Dirtyworks.ai receivables.

## Product approval and deployment lifecycle

1. **Discover:** record client job, users, data, integrations, risk, incumbent tools, and desired outcome.
2. **Compose:** select candidates in the configurator; identify overlap, prerequisites, commercial route, and estimated cost.
3. **Assess:** review vendor terms, privacy/security, identity, retention, data location, support model, exit, and licence/admin fit.
4. **Approve:** client accepts the product, costs, responsibilities, permitted use, and account owner; Dirtyworks.ai approves the support tier.
5. **Deploy:** create or claim the customer-owned tenant, configure identity/policy, assign licences, test, document, and train.
6. **Operate:** manage joiner/mover/leaver events, support, spend, changes, incidents, vendor notices, and value review.
7. **Renew or exit:** reconcile users and use, re-price, export customer artifacts, revoke Dirtyworks.ai access, and remove unused licences.

No shared user accounts should be used to reduce seat cost. Administrative access should be named, least-privilege, logged where available, and revocable.

## Economics and control rules

- Keep customer-direct vendor estimates out of Dirtyworks.ai revenue and gross margin.
- Treat resale billings and matching vendor cost as pass-through revenue/cost only when Dirtyworks.ai is the authorized seller of record.
- Require prepayment or credit controls before Dirtyworks.ai assumes non-cancellable licence or usage obligations.
- Give every usage product a monthly estimate, warning threshold, approver, and hard limit where the platform permits it.
- Set a minimum monthly managed-platform fee; do not rely on small per-seat charges alone.
- Consolidate overlapping tools during the quarterly portfolio review. More products are not automatically more value.
- Add a candidate to the standard catalogue only after pricing, licence/resale status, admin capabilities, security/privacy evidence, support route, deployment runbook, and exit procedure are recorded.
- Remove or suspend a product when vendor terms, control gaps, support burden, or customer evidence makes it uneconomic or unsafe.

## Validation plan

| Hypothesis | Test | Evidence threshold |
|---|---|---|
| Buyers value a curated menu | Use the catalogue in 10 discovery calls | At least 5 buyers ask to compare or compose a mix |
| Transparent management is buyable without resale | Issue 5 quotes with vendor cost separated | At least 2 accept the structure without demanding one invoice |
| Platform plus user pricing reflects effort | Time all deployment/admin work | 60% normalized recurring gross margin after stabilization |
| A narrow standard catalogue is supportable | Support first 3 client portfolios | At least 80% of products use a repeatable runbook and remain within support allowance |
| Resale improves—not distorts—economics | Obtain one distributor/vendor proposal | Net margin and cash exposure outperform customer-direct administration after all obligations |

## Decisions still owned by the sponsor

- Whether the public experience emphasizes a simple recommended stack or a larger build-your-own menu.
- Whether the first sales experiment uses line-item management or a portfolio bundle.
- Whether to pursue Microsoft/Google indirect-reseller authorization during validation or wait for confirmed demand.
- Whether Dirtyworks.ai will ever carry usage credit, or require all variable consumption to remain in customer accounts.
- Which products become the first supported runbooks after the initial prospect conversations.

None of these blocks using the candidate catalogue and configurator for discovery. They do block promising a fixed public rate card or representing Dirtyworks.ai as an authorized reseller.

