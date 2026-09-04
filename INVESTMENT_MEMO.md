# Investment Memo: Borssele 1 & 2 Offshore Wind Farm

**Question: Should an investor have invested in Borssele 1 & 2 in 2016?**

*Perspective: September 2016, at the time of the tender award. A retrospective postscript follows using outcomes through 2026.*

---

## Executive Summary

Based on information available in 2016, Borssele 1 & 2 offered a marginally positive, low-risk business case: an unlevered NPV of approximately **EUR 64 million** on a c. EUR 1.5 billion investment, an IRR of **4.9%** against a WACC of 4.3%, and a 15-year government-backed revenue floor that removed most downside price risk. A Monte Carlo simulation shows the base case sits close to the break-even point of the distribution, with a **c. 49% probability of a negative NPV**, concentrated almost entirely in the ten operational years following subsidy expiry. On balance, the project was investable in 2016 for an investor with a long-dated, infrastructure-style risk appetite — but only marginally so, and the winning bid only clears its cost of capital under construction costs below contemporary market estimates. Realised outcomes since 2021 have substantially exceeded the 2016 expectation, driven by wholesale prices well above the subsidy threshold.

## Investment Thesis

Borssele 1 & 2 (752 MW, 94 × Siemens Gamesa 8MW turbines, 23km off the Zeeland coast) was awarded to Ørsted (then DONG Energy) in July 2016 following a competitive tender: the winning bid of **EUR 72.70/MWh** was the lowest of 38 submissions, roughly 40% below the pre-tender cost ceiling.

Three features support the investment case:

1. **Revenue protection without a return cap.** The Dutch SDE+ subsidy tops up revenue to the EUR 72.70/MWh tender amount whenever the market price falls between a floor of EUR 29/MWh and the tender amount, for the first 15 operational years. Above EUR 72.70/MWh, the project earns the full market price with no clawback — asymmetric protection that favours the operator.
2. **Competitive price discovery.** A 38-bid competitive tender is strong evidence the award price reflected efficient market pricing rather than a subsidy giveaway.
3. **Structural demand backdrop.** Dutch and EU decarbonisation policy commitments underpin long-run demand for offshore generation capacity, supporting the value of the asset beyond the subsidy period.

## Risks

- **Merchant price exposure after year 15.** From operational year 16 onward the project sells entirely at the prevailing market price, with no floor. This is the single largest driver of downside in the simulation (see below).
- **Downside below the subsidy floor.** If the market price falls below EUR 29/MWh even within the subsidy period, the operator absorbs the shortfall — the floor protects the subsidy calculation, not the operator's realised price.
- **Construction cost overrun.** At CREG's 2016 cost estimate (EUR 1,891m, c. 27% above the EIB's later EUR 1,491m figure), the base case NPV turns **negative (-EUR 291m)**. The bid is only rational under costs below this conservative outside estimate.
- **Regulatory/tax assumptions.** WACC and tax treatment are based on 2016-era assumptions that may not hold over a 25-year horizon.

## Base Case

Deterministic cash flow model, constant EUR 30/MWh market price assumption (CREG, 2016), WACC 4.3%:

| Metric | Value |
|---|---|
| NPV | EUR 63.6m |
| IRR | 4.91% |
| Payback (discounted) | 15 years |
| LCOE | EUR 53.82/MWh |

The base case NPV is positive but thin relative to a c. EUR 1.5bn outlay — consistent with a competitively tendered, subsidy-backed infrastructure asset rather than a high-margin opportunity.

## Monte Carlo Analysis

20,000 simulations, varying market price (lognormal, mean EUR 30/MWh, std EUR 7.3/MWh, calibrated to 2015–2019 realised NL price volatility), capacity factor (normal, mean 50%, std 3pp), and CAPEX (normal, mean EUR 1,491m, std EUR 150m):

| Metric | Value |
|---|---|
| Mean NPV | -EUR 0.4m |
| Median NPV | EUR 8.1m |
| 5th percentile | -EUR 422m |
| 95th percentile | EUR 392m |
| P(NPV < 0) | 48.6% |

The distribution is close to symmetric around zero — this is a coin-flip investment at the point of decision, not a clearly value-accretive one. Decomposition shows the downside is concentrated in the unprotected post-subsidy years (16–25): a below-average price draw compounds over ten unhedged years, while the subsidy period cushions the same draw to close to the tender amount. The upside is comparably wide because prices above EUR 72.70/MWh flow through to the operator uncapped.

## Recommendation

**Marginal approve, with risk awareness.** An investor with a long-duration, infrastructure-matched cost of capital and tolerance for a near coin-flip distribution around a thin positive expected value could reasonably have approved this investment in 2016, on the basis that:

- the subsidy structure caps the probability-weighted downside during the first 15 years,
- the competitive tender process provides confidence the price reflects efficient market discovery, and
- the exposure to unprotected merchant risk in years 16–25 is a known, quantifiable, and hedgeable feature (e.g. via PPAs closer to year 15) rather than an open-ended risk.

An investor unwilling to accept a c. 49% probability of a negative NPV, or unable to underwrite construction costs below the CREG estimate, should have declined.

---

## Postscript: What Actually Happened (2021–2026)

Realised NL wholesale prices from 2021 exceeded the tender amount in most years — most sharply in 2022 (average EUR 241/MWh amid the European energy crisis) — meaning the project earned the full market price rather than the subsidised amount for most of its operating life to date.

| Metric | Ex-ante (2016) | Ex-post (realised + tail assumption) |
|---|---|---|
| NPV | EUR 64m | EUR 1,324m |
| IRR | 4.9% | 14.0% |

**Market validation.** In April 2021, Norges Bank Investment Management paid EUR 1,375m for a 50% equity stake, implying a total equity value of c. EUR 2,750m. Discounting the model's post-2021 cash flows to the same date and netting initial project debt implies a model equity value of c. EUR 1,893m — c. EUR 857m below the price paid, consistent with infrastructure investors accepting a lower required return than the WACC applied here, or pricing in a more constructive long-term power price view at the time.

The 2016 decision was correct on the information available at the time; the realised outcome substantially exceeded even the upper end of what a 2016 analyst would reasonably have modelled, illustrating how a marginal base case combined with asymmetric subsidy protection can produce strong realised returns when the underlying commodity price moves favourably.

---

*Methodology, full assumptions with sources, and the underlying model are documented in the accompanying README and Jupyter notebook.*
