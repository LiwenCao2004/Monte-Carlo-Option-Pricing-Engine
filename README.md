# Monte Carlo Option Pricing Engine

A flexible Monte Carlo option pricing engine for equity derivatives under a Geometric Brownian Motion (GBM) model, in the risk-neutral measure with zero dividends.

## Supported option styles

- European call / put options
- Asian options (arithmetic or geometric average)
- Barrier knock-in options (up-and-in, down-and-in)
- Barrier knock-out options (up-and-out, down-and-out)
- American-style options (priced via Least-Squares Monte Carlo / Longstaff-Schwartz)

## What's inside

- GBM path simulation with configurable step size
- Closed-form Black-Scholes pricing used to validate the European Monte Carlo estimates
- Longstaff-Schwartz least-squares regression for American-style early exercise
- Antithetic variates for variance reduction
- Numerical Greeks (Delta, Gamma, Vega, Theta, Rho) via central finite differences
- Sensitivity analysis across volatility, maturity, strike, and barrier level

## Setup

```bash
pip install -r requirements.txt
```

## Run

Open `Monte_Carlo.ipynb` and run all cells. All inputs are set manually at the top of the notebook (spot price, strike, expiry, rate, volatility, number of simulations) — no external dataset or API key is required.
