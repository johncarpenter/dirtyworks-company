# Dirtyworks.ai financial model guide

**Version:** 0.1  
**Date:** 2026-08-25  
**Workbook:** `documents/business-plan/dirtyworks-ai-financial-model.xlsx`  
**Status:** Formula-driven planning baseline; assumptions are unvalidated unless labeled otherwise

## Decision purpose

The workbook answers five questions:

1. What customer funnel must exist to produce the 18- and 36-month recurring-revenue outcomes?
2. Which offer and channel structures can support the required normalized gross margin?
3. When does a half-time founder run out of delivery capacity?
4. How much cash is required under downside, base, and upside assumptions?
5. Which assumptions must be validated before the next tranche of capital or operating complexity is justified?

It is an operating model, not a valuation. A discounted cash flow, terminal value, or investment return would imply a precision the company does not yet have.

## Workbook map

| Sheet | Role |
|---|---|
| `Cover` | Version, conventions, navigation, and model status |
| `Dashboard` | Side-by-side downside, base, and upside outputs plus MRR and cash charts |
| `Assumptions` | Active-case selector used by unit and channel economics |
| `Scenarios` | Editable downside, base, and upside hypotheses |
| `Monthly Model` | Three complete 36-month customer, revenue, capacity, margin, operating-expense, and cash schedules |
| `Unit Economics` | Offer-level direct and channel normalized margin tests |
| `Channel Economics` | Direct, referral, co-managed, and white-label responsibility/economic comparison |
| `Checks` | Mix, customer roll-forward, revenue, capacity, and cash reconciliation |
| `Sources` | Internal source documents, external context, status, and limitations |

## How to use it

1. Open `Scenarios` and edit blue cells only.
2. Keep each column internally coherent; do not change a single optimistic input without reviewing the related sales, churn, capacity, cost, and collection assumptions.
3. Use `Dashboard` to compare all cases.
4. Change `Assumptions!B4` to select the case used by `Unit Economics` and `Channel Economics`.
5. Confirm `Checks` remains `PASS`.
6. Treat a failed business threshold as a decision signal even when the mechanical checks pass.

Blue cells are editable assumptions. Green cells are cross-sheet references. Black cells are calculations. Yellow highlights identify active/base inputs or figures requiring attention.

## Core mechanics

### Customer funnel

```text
paid review in month n
× review-to-launch conversion
= launch in month n+1

launch in month n
× launch-to-managed conversion
= new managed account in month n+1

active accounts
= new managed accounts
− monthly churn
```

Fractional contracts are planning averages. They prevent a small number of lumpy deals from making a monthly model unreadable; the operating plan must still schedule real contracts discretely.

### Revenue

Revenue is built from:

- paid reviews;
- launches;
- active recurring accounts by Core, Operate, and Scale package;
- expansion-project incidence;
- partner enablement projects.

The model applies a weighted channel factor:

```text
effective revenue factor
= 1 − (channel share × channel discount)
```

This is appropriate for scenario planning, but not for pricing a real partner agreement. Use `Channel Economics` to test a named responsibility structure.

### Capacity

Delivery demand is calculated from offer volume and hours per offer. Capacity fills in this order:

1. founder delivery capacity;
2. planned core contractor capacity after its start month;
3. flex subcontracting.

Flex subcontracting prevents the model from recognizing revenue with no delivery plan. It also exposes the margin consequence and the scale of the next hire.

### Founder economics

The model keeps two views:

- **Cash view:** founder cash compensation affects cash operating expense and runway.
- **Normalized view:** all founder time carries a loaded economic cost; delivery time is cost of service and non-delivery time is operating expense.

Do not add founder cash compensation to normalized founder cost. The normalized view replaces the cash compensation view to avoid double counting.

### Cash

Cash receipts combine same-month collection with the prior month's remaining receivable. Cash disbursements include cash cost of service and cash operating expense. Sponsor capital arrives only in the scenario-defined tranche months.

The model excludes GST, income tax, debt, depreciation, capitalized development, pass-through customer licences, and refunds. Add those schedules when real operations make them material.

## Current scenario outputs

| Metric | Downside | Base | Upside |
|---|---:|---:|---:|
| Month 18 managed accounts | 0.8 | 4.5 | 10.3 |
| Month 18 MRR | $1.8K | $18.9K | $56.5K |
| Month 18 normalized gross margin | 7.8% | 58.4% | 76.4% |
| Month 36 managed accounts | 2.2 | 13.3 | 30.7 |
| Month 36 MRR | $4.8K | $55.3K | $167.7K |
| 36-month cumulative revenue | $157.8K | $1.15M | $3.23M |
| Planned sponsor capital | $5.0K | $42.5K | $50.0K |
| Additional cash required above plan | $5.6K | $2.2K | $2.0K |
| Peak flex contractor hours/month | 0.0 | 82.4 | 208.2 |
| Month 36 normalized operating profit/(loss) | ($5.5K) | $33.3K | $144.3K |

The cases are not probability-weighted. The upside is a capacity stress case as much as a sales case.

## Findings the model exposes

### 1. The original 18-month funnel was not internally consistent

The strategy recorded five paid reviews, three launches, and five managed-service customers. A progressive review → launch → managed funnel cannot produce more managed customers than launches without another acquisition path.

The base model therefore uses a coherent acquisition ramp, 60% review-to-launch conversion, and 75% launch-to-managed conversion. It produces approximately 4.5 active managed accounts by month 18. The strategy should later choose whether to:

- increase paid-review volume;
- improve conversion through qualification;
- add a direct-to-managed path for already-qualified partner accounts;
- lower the month-18 managed-account target.

No choice is made by the model.

### 2. The base case narrowly misses the current MRR target

Month-18 base MRR is approximately $18.9K versus the strategy range of $20K–$30K. The gap can be closed through several mechanisms:

- stronger Operate/Scale mix;
- higher price;
- more paid reviews;
- higher conversion;
- lower churn;
- additional domains or separately priced recurring scope.

Each mechanism changes delivery and market risk. The model leaves them separately editable.

### 3. Three reference offers miss their normalized direct-margin target

At base assumptions:

| Offer | Direct normalized GM | Target | Mechanism to test |
|---|---:|---:|---|
| Review | 57.5% | 60% | Reduce eight delivery hours, adjust scope, or change price |
| Launch | 44.9% | 50% after second | Reuse launch assets, reduce 40 hours, or increase price |
| Core | 56.5% | 60% | Hold delivery near six hours, reduce direct cost, or change scope/price |
| Operate | 60.8% | 60% | Preserve scope discipline |
| Scale | 62.2% | 60% | Scope each account; do not treat the proxy as a quote |

The first-launch threshold remains 40% when rework creates reusable assets. That is a deliberate learning allowance, not a permanent margin standard.

### 4. White-label economics depend on work actually removed

A 25% partner discount applied without labour reduction makes most base offers unattractive. `Channel Economics` separately tests revenue retained and delivery-cost factor.

The reference white-label model assumes Dirtyworks.ai retains 75% of customer price and reduces normalized delivery cost by 10%. Under those assumptions:

- Review: 49.6% normalized GM;
- Launch: 34.3%;
- Core: 48.3%;
- Operate: 53.5%.

The result supports multiple real options:

- keep Review and Launch closer to direct price while discounting mature recurring work;
- require a paid partner-enablement fee;
- use referral or co-managed delivery until the partner proves sales and tier-1 deflection;
- reduce partner discount;
- standardize the launch before offering wholesale economics.

### 5. The planned capital envelope needs a timing choice

The base case includes $42.5K of planned sponsor capital and still reaches a minimum cash balance of approximately negative $2.2K. Options include:

- add roughly $2.2K–$5K of explicit working-capital headroom;
- improve collection timing;
- defer one-time readiness or repeatability spend;
- delay founder cash compensation;
- slow acquisition and contractor timing.

The total remains within the sponsor's $5K–$50K range if the base plan is adjusted carefully.

### 6. Capacity becomes the scale constraint

The base case begins core contractor capacity in month 15 at 80 hours per month, yet eventually requires approximately 82 additional flex hours in the peak month. The upside case requires more than 200 flex hours.

The decision is not simply “hire.” Real options are:

- hire a delivery lead when contracted recurring margin covers the role;
- maintain a bench of qualified flex contractors;
- cap concurrent launches;
- narrow package scope;
- automate repeated internal delivery work after it is measured;
- slow sales deliberately to protect quality.

## Scenario interpretation

### Downside

Tests weak conversion, 3% monthly churn, 40% channel mix, a 30% channel discount, slower acquisition, higher delivery hours, and no later capital tranches. It demonstrates that cash gross profit can look acceptable while normalized profitability remains poor because founder labour is not free.

### Base

Tests a plausible founder-led operating plan: a coherent funnel to roughly five managed accounts by month 18, stronger Operate mix, staged contractors, 1.5% monthly churn, and evidence-gated capital.

### Upside

Tests stronger conversion, price, mix, retention, and partner activity. It should be read as a delivery-system stress test. The cash outcome is attractive only if the company adds capacity without losing quality or margin.

## Updating with evidence

Replace assumptions as operating data arrives:

| Evidence event | Update |
|---|---|
| Paid review sold | Review volume, price, collection, and acquisition cost |
| Review completed | Review hours, direct cost, and feasibility rate |
| Launch signed | Conversion, price, milestone collection, and launch timing |
| Launch accepted | Launch hours, rework, direct cost, and release quality |
| Day-30/60/90 managed operation | Package hours, support burden, direct cost, normalized GM, use, and customer outcome |
| Partner pilot | Revenue retained, sales/account/support work removed, collections, and escalation burden |
| First renewal or loss | Churn, sales cycle, reasons, and expansion incidence |

Do not average away critical permission, privacy, security, or customer-outcome failures.

## Known limitations

- No operating data exists yet.
- Target-account population and obtainable market are not quantified.
- Sales arrive discretely, while the model uses monthly planning averages.
- Taxes and indirect-tax timing are excluded.
- Accounts receivable uses a simplified one-month collection pattern.
- No refund, bad-debt event, debt, or financing cost schedule exists.
- Scale-package price and delivery are proxies until scoped.
- Expansion revenue is incidence-based, not cohort-specific.
- Contractor availability and qualification are assumed.
- The model does not value the company.

These limitations do not block current customer and partner validation. They should be addressed when real transactions make them decision-relevant.

