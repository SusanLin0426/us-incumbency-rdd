# Incumbency Advantage in U.S. Elections (RDD)

This repo examines whether incumbency raises the probability of winning the next election. We estimate a baseline **OLS** model and **Regression Discontinuity Designs (RDD)**—both linear and quadratic—around the **50% vote share** cutoff using U.S. state-level presidential results by cycle.

## Methods
- **Model 1 – OLS:** next-cycle win indicator on current-cycle win indicator.  
- **Model 2 – RDD (Linear):** sharp RDD at 50% vote-share cutoff with treatment dummy and interactions.  
- **Model 3 – RDD (Quadratic):** quadratic polynomials on each side of the cutoff to reduce functional-form bias.  
- **Diagnostics:** bandwidth choice, visual discontinuity plots, heteroskedasticity-robust SEs, placebo checks (optional).

## Variables (illustrative)
- `win_dem` — party wins current cycle (0/1)  
- `win_dem_t1` — party wins next cycle (0/1)  
- `demvoteshare` — Democratic vote share (0–1) this cycle  
- `D` — treatment dummy: 1 if `demvoteshare >= 0.5`, else 0
