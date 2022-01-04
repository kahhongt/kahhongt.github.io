---
title: "Systematic Trading using FTX API"
date: 2021-12-03
excerpt: "Trend-Following Strategy applied to ETH/USDT"
collection: portfolio
---

### Background
In this project, we explore the feasibility of backtesting a simple trend-following strategy using 2 exponentially-weighted moving averages. Moving averages are commonly used to generate systematic buy-sell-hold signals in traditional markets. When the fast exponential moving average > slow exponential moving average, this indicates upward price momentum, and the reverse would indicate downward price momentum.

Here, we attempt to implement a backtest using **ETH Spot**, using data from **28 March 2020 to 1 November 2021**.

### Setup
1. ETH Hourly OHLCV data is collected using the [FTX API](https://docs.ftx.com/#overview)
2. Create slow and fast exponential moving averages using different half-lives
3. Generate positions based on difference between the fast and slow exponential moving averages
4. Backtest over sample period and check PnL metrics
5. Generate half-life parameter field to identify regions of positive sharpe
6. Verify results using out-of-sample data

### Implementation
Since we are using hourly OHLCV bars, the shortest trade interval must be > 1 hour. We backtest our strategy with the following initial parameters:
1. Fast Half-life: 1 Hour
2. Slow Half-life: 5 Hours

We obtain the cumulative returns shown in Figure 1.

<p align = "left"><em>Figure 1: Cumulative Returns from Strategy vs Asset</em></p>
<p align="left"><img src="/images/Trend-following Cumulative Returns.png"/></p>

Figure 1 clearly shows an underperformance with the initial half-life parameters. To gain a general understanding of performance, we iterate across a wide range of half-life parameters for fast and slow exponential moving averages - to generate a sharpe field. A green label indicates positive sharpe, while a red label indicates negative sharpe. We can then visually identify regions in the parameter space indicating a positive sharpe.

<p align = "left"><em>Figure 2: Sharpe Field with varying fast and slow exponential half-lives</em></p>
<p align="left"><img src="/images/Trend-following Sharpe Field.png" height="450" width="600" /></p>

We can then identify the half-life pair that generates the highest sharpe ratios, and have found that the best combinations tend to involve a fast half-life of ~1, and a slow half-life from 40 to 48.

<p align = "left"><em>Figure 3: Results Summary - Top 5 Sharpe </em></p>
<p align="left"><img src="/images/Trend-following Results Table.png" height="150" width="210" /></p>

### Limitations

Nonetheless, any performance metrics calculated using the above backtest methodology would have been an overestimate due to the presence of slippage, transaction cost, and other execution-related inefficiencies.

### Contact
I hope you have enjoyed reading the above piece of analysis. I would be happy to receive your thoughts/comments at [kahhong.tai@gmail.com](kahhong.tai@gmail.com).
