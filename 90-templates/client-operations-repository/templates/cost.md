---
id: cost-<product-or-portfolio>-<period>
title: <Product or portfolio cost reconciliation for period>
type: cost
status: current
summary: <Period, total/variance status and primary action without false precision.>
source_ids: []
owner: <finance-or-service-owner>
created_at: <YYYY-MM-DD>
updated_at: <YYYY-MM-DD>
review_by: <YYYY-MM-DD>
tags: [class-restricted, control-cost]
---

# <Cost reconciliation title>

## Cost Record

- **Cut-off / currency / tax basis:** <values>
- **Products included:** <links>
- **Contracted / purchased / assigned / active / billed:** <separate values and definitions>
- **Vendor cost / Dirtyworks.ai fee:** <separate values>
- **Source freshness:** <dates>

## Reconciliation

For each material value, record authoritative source, collected/observed date, status as estimate/export/invoice/payment and reconciliation result.

## Variance and Action

Record budget/prior-period variance, cause, confidence, approved action, owner and due date. Do not treat a bank transaction or dashboard estimate as an invoice.

## Relationships

- `applies-to` -> [[product-<name>|<Product>]]
- `produced-by` -> [[process-page-id|Monthly cost close]]
- `approved-by` -> [[person-<name>|<Budget owner>]]

## Forecast

Record disclosed assumptions and known renewal/consumption effects.

## Optimization

Record proposed removal, reassignment, plan change or budget control; link approval/change if executed.

## Evidence

Link approved invoice/export/accounting evidence under the repository retention policy.
