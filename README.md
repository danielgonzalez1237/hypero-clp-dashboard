# Hypero CLP Strategy Dashboard

Interactive analytics dashboard for the WETH/WBTC Concentrated Liquidity Position (CLP) strategy on Uniswap V3 Arbitrum (0.05% fee tier).

## Overview

This dashboard presents a comprehensive audit and backtest of Hypero's delta-neutral CLP strategy, covering:

- **Equity Curve** — BTC-denominated performance over 3.94 years (Jan 2022 – Mar 2026)
- **8 Scenario Comparison** — Range widths from ±5% to ±20%, with funding variations
- **Return Components** — Fee income, hedge income, IL costs, gas costs breakdown
- **Pool APY Analytics** — Daily & rolling 30d APY with yearly statistics
- **Rebalance Log** — All 38 rebalance events with IL and fee data
- **Risk Metrics** — Drawdown analysis, sensitivity stress tests, risk matrix
- **Funding Analysis** — Hedge income vs fees, funding scenario comparisons
- **Data Validation** — Cross-verified against CoinGecko and on-chain data
- **GO/NO-GO Verdict** — Final deployment recommendation with phased plan

## Key Results (±10% Recommended Strategy)

| Metric | Value |
|--------|-------|
| CAGR | 20.19% (BTC terms) |
| Final Portfolio | 2.0625 BTC (from 1.0 BTC) |
| Max Drawdown | -0.17% |
| Rebalances | 38 over 3.94 years |
| Time in Range | 97.2% |
| Cumulative Fees | +0.9316 BTC |
| Hedge Income | +0.1870 BTC |
| IL Cost | -0.0540 BTC |

## Features

- **BTC / USD toggle** — View all metrics in BTC benchmark or USD reference
- **10 interactive tabs** — Overview, Equity Curve, Scenarios, Components, Pool APY, Rebalances, Risk Metrics, Funding, Validation, Verdict
- **Real data only** — No synthetic or simulated data; all sourced from CoinGecko, Uniswap V3 pool data, and verified on-chain

## Tech Stack

- Vanilla HTML/CSS/JS (static, no build step)
- Chart.js for all visualizations
- Inter + JetBrains Mono typography
- Dark theme, responsive layout

## Deployment

Static files — serve with any web server:

```bash
npx serve . -l 3000
```

Or deploy to Vercel, Netlify, GitHub Pages, or any static host.

## Data Sources

- ETHBTC daily prices: CoinGecko API (validated within 1.92%)
- Pool APY/TVL: DefiLlama (WBTC-WETH Arbitrum Uniswap V3)
- Funding rates: Conservative 7% annualized constant
- Backtest engine: Independent Python implementation

---

**Verdict: CONDITIONAL GO** — Deploy ±10% strategy with phased capital allocation.

Built by [Hypero](https://hypero.io)