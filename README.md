# Adaptive beta for hedging equity portfolios

Estimating the market beta of S&P 500 stocks (against SPY) for hedging, and comparing sliding-window beta, Follow the Leader and Random Forest, scored by beta error. BSc thesis, Budapest University of Technology and Economics (BME), 2020

## What's inside

- [`thesis/`](thesis) - the full thesis (docx)
- [`notebooks/Follow_the_leader.ipynb`](notebooks/Follow_the_leader.ipynb) - beta error per sliding window, best window per day, Follow the Leader v1 and v2
- [`notebooks/Random_forest.ipynb`](notebooks/Random_forest.ipynb) - Random Forest models trained on different features of the instruments (returns, high, low, volume)

## Approach

- Data: daily prices of S&P 500 stocks and SPY, 2000-2020, from Yahoo Finance
- Baseline: beta over fixed sliding windows (5 to 60 days), plus the best window for each day
- Follow the Leader: two variants that favour the window with the best track record
- Random Forest: several models compared against the baselines

## Result

Random Forest does best at the start of the test period, then converges to Follow the Leader. More features and tuning should help, details in the conclusion of the thesis

## Notes

- The notebooks are the original working versions, saved with their outputs
- Re-running needs the input CSVs (Yahoo Finance data, not included) and a `Results/` folder
- Not investment advice
