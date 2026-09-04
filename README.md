# Borssele 1 & 2 — DCF & Monte Carlo Analysis

A DCF valuation and Monte Carlo simulation of the Borssele 1 & 2 offshore wind farm (752 MW, Netherlands), built from the perspective of the 2016 tender decision, with a reflection using realised outcomes through 2026.

**➜ [Read the investment memo](INVESTMENT_MEMO.md)** for the full analysis and recommendation: *Should an investor have invested in Borssele 1 & 2 in 2016?*

## Contents

| File | Description |
|---|---|
| `INVESTMENT_MEMO.md` | Investment thesis, risks, base case, Monte Carlo results, and recommendation |
| `Borssele_DCF_Model.ipynb` | Full model: deterministic DCF, sensitivity analysis, Monte Carlo, ex-post analysis, benchmarking |
| `Borssele_Model_EN.xlsx` | Companion Excel model, used to validate the Python implementation |
| `data/NL_wholesale_electricity_prices.csv` | NL wholesale day-ahead electricity prices (ENTSO-E), 2015–2026 |

## Methodology

The model follows the Dutch SDE+ subsidy mechanism specific to this tender: for the first 15 operational years, revenue is topped up to the tender amount (EUR 72.70/MWh) whenever the market price falls between a floor (EUR 29/MWh) and the tender amount; above the tender amount the project earns the full market price; below the floor, the operator retains the downside. After year 15, revenue is market price only.

Two perspectives are modelled:
- **Ex-ante**: a fixed EUR 30/MWh price assumption, matching the 2016 CREG cost-benefit analysis of the tender.
- **Ex-post**: realised NL day-ahead prices (2021–mid 2026), with a documented assumption for years beyond available data.

The Python model is validated against an independently built Excel model; both produce identical NPV, IRR, and LCOE outputs for the base case.

## Key sources

CREG (2016) tender cost-benefit analysis · Ørsted project disclosures · European Investment Bank (2020) financing summary · Netherlands Court of Audit, *Kosten windenergie op zee* (2018) · RVO SDE+ scheme documentation · ENTSO-E Transparency Platform · Norges Bank Investment Management (2021) transaction announcement

Full parameter-level sourcing is documented in the Assumptions sheet of the Excel model and the first section of the notebook.

## Running the notebook

```
pip install numpy numpy-financial pandas matplotlib
```

Place `NL_wholesale_electricity_prices.csv` in a `data/` folder alongside the notebook, then run all cells in order.

## Limitations

- Turbine degradation is set to 0% (wind degradation is small and disputed in the literature; the parameter is exposed for sensitivity testing).
- The Monte Carlo draws one long-run price per simulation rather than a year-by-year path, modelling uncertainty about the average price level rather than short-term volatility.
- Actual (as opposed to assumed) capacity factor has not been cross-checked against metered production data.
- The post-2026 price assumption (EUR 80/MWh) is a documented judgement, not a third-party forecast.
