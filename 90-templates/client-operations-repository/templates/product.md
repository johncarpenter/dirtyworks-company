---
id: product-<vendor-or-product>-<tenant-purpose>
title: <Product and tenant purpose>
type: product
status: planned
summary: <Product, customer-owned tenant and managed purpose.>
source_ids: []
owner: <product-owner>
created_at: <YYYY-MM-DD>
updated_at: <YYYY-MM-DD>
review_by: <YYYY-MM-DD>
tags: [class-confidential, product-ai-saas]
---

# <Product and tenant purpose>

## Product Record

- **Vendor / seller of record:** <organizations>
- **Plan/SKU:** <plan>
- **Tenant/account ID:** <non-secret identifier>
- **Customer owner / Dirtyworks.ai owner:** <links>
- **Purchased / assigned / active definitions:** <definitions and current source dates>
- **Authoritative admin/support sources:** <links>

## Administration

Record identity, roles, MFA, delegated administration, configuration baseline, audit/export and vendor escalation.

## Cost and Renewal

Record billing owner, price basis, currency/tax, period, invoice source, renewal, notice and cancellation. Link the current cost page.

## Exit

Record suspension, export, user/access revocation, cancellation and deletion/retention path.

## Relationships

- `supported-by` -> [[org-<vendor>|<Vendor>]]
- `applies-to` -> [[service-<name>|<Service>]]
- `operated-on` -> [[process-<name>|<Administration process>]]

## Data and Security

Record approved use, data categories, model-training/data-use setting, location, retention and material subprocessors.

## Configuration Baseline

State native source, observed date, verifier and approved exceptions.

## Support

Link Freshdesk workflow, vendor status/support route and escalation boundary.

## Evidence

Link vendor/contract/admin/invoice authorities with observed dates; do not paste secrets.

