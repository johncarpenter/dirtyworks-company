# Functional company repository reorganization

**Date:** 2026-08-27  
**Status:** Completed  
**Source:** `/Users/john/Documents/Workspace/DirtyWorks.ai/documents/`  
**Destination:** `/Users/john/Documents/Workspace/DirtyWorks.ai/dirtyworks-company/`

## Outcome

Moved all 390 meaningful company-documentation files into the functional company repository, including 93 Markdown files and their supporting workbooks, design-system files, campaign assets and client-operations template resources. macOS `.DS_Store` metadata was not migrated.

## Placement decisions

- Company authority, scorecards, readiness and work planning moved to `01-governance/`.
- Strategy, research, segmentation, channels, business model and roadmaps moved to `02-strategy-and-research/`.
- Offers, pricing, product catalogue, configurator and deferred application concepts moved to `03-offers-and-products/`.
- Brand governance, marketing content, campaigns, creative assets and the complete design system moved to `04-marketing-and-brand/`.
- GTM, discovery, qualification, account research and MSP discovery tools moved to `05-sales-and-partnerships/`.
- Reusable service delivery, customer gates, onboarding, quality and client-operations platform design moved to `06-client-delivery/`.
- Financial models, workbooks and experiment capital planning moved to `08-finance/`.
- Contracting framework and business-draft agreements moved to `09-legal-risk-and-compliance/`.
- Agent/service architecture and SaaS cost-platform evaluation moved to `11-technology-and-data/`.
- The client-operations repository template pack moved to `90-templates/`.

## Integrity work

- Rewrote 165 local Markdown links according to the source-to-destination map.
- Preserved the existing company documentation index under `01-governance/company/`.
- Preserved the design-system production index as `04-marketing-and-brand/design-system/production-guide.md`; the functional repository guidance remains its `README.md`.
- Did not move application-local documentation from application repositories or the internal Codex skill under `tools/`.

## Known policy follow-up

Several migrated operating documents still describe one private repository per client. The newly selected shared-client-repository model changes access, isolation, ingestion, retention and offboarding assumptions. That content requires a separate substantive architecture decision and document revision; this migration changed placement and links, not business meaning.
