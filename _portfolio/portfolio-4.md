---
title: "Statistical Arbitrage for Highly-Correlated Crypto Assets [WIP]"
date: 2023-01-02
excerpt: "From Simple Price Ratio Analysis to Gaussian Process Application"
collection: portfolio
---

### Background
According to Investopedia, Statistical Arbitrage regers to trading strategies that utilise mean-reversion to invest in diverse portfolios, over both short and medium time horizons. A statistical arbitrage portfolio would typically be intended to be market neutral, due to the presence of both long and short positions in highly-correlated assets. While statistical arbitrage is typically used on trading pairs, the concept may also be applied to groups of correlated securities. For greater simplicity and interpretability we will be limiting analyses only to a pair of cryptocurrencies.

### Identifying Pairs for Mean-Reversion
There are a few core criteria for selecting appropriate trading pairs:
1. High Correlation
2. High Cointegration
3. Stationarity of Price Spread/Ratio

High degree of correlation and cointegration is required to ensure that the two assets move in tandem over both short-term and long-term time horizons, thereby allowing the overall portfolio to be approximately market neutral and thus not directionally exposed. In checking for cointegration, we inspect the p-values generated via the Engle-Granger Two-Step Cointegration Test, and identify pairs with a sufficiently low p-values, indicating a high-degree of cointegration.

<p align = "left"><em>Figure 1: Correlation Matrix</em></p>
<p align="left"><img src="https://user-images.githubusercontent.com/33640882/222986972-104568c5-9976-4b73-ba3b-7d44424781a1.png"/></p>

<p align = "left"><em>Figure 2: Cointegration p-values</em></p>
<p align="left"><img src="https://user-images.githubusercontent.com/33640882/222987009-a90ee378-69e9-4191-ae8b-65a2ce39b79d.png"/></p>

From the above we see a number of candidates: BTCUSDT/ETHUSDT, LTCUSDT/ETHUSDT, and NEOUSDT/LTCUSDT. The characteristic of stationarity would be most critical towards implementing any mean-reversion trading strategy, as the statistical properties of the time series - variance. autocorrelation and mean, can be assumed to remain unchanged over time. After stationarity of the price ratio has been determined using the Augmented Dickey-Fuller test, we explore implementation using a training set of the BTC/ETH trading pair.

### Implementation
We split data for BTCUSDT/ETHUSDT from August 2017 to December 2022 into training and testing sets, and parameter selection was evaluated on the training set. Considering the BTCUSDT/ETHUSDT ratio, a short BTC position and long ETH position will be placed when the ratio exceeds a certain threshold X, while a long BTC position and short ETH position will be plaved when the ratio exceeds a certain threshold -X. When a position has been placed, it will be held until the ratio reverts to another threshold Y and -Y respectively. The thresholds were constructed using exponential moving averages and standard deviation, with an arbitrarily determined half-life parameter. We generate some portfolio statistics below in Figure 3, and some useful plots in Figure 4. In determining the thresholds, we set the confidence interval as 95%, and halflife as 40 days.

<p align = "left"><em>Figure 3: Training Set Performance Statistics</em></p>
<p align="left"><img src="https://user-images.githubusercontent.com/33640882/222988890-e8e28202-09e3-419e-b11e-1727bd026f2d.png"/></p>

<p align = "left"><em>Figure 4: Training Set Performance Plots</em></p>
<p align="left"><img src="https://user-images.githubusercontent.com/33640882/222989179-e073387f-69a4-4dfe-b622-3187df5afc19.png"/></p>







### Limitations


### Contact
I hope you have enjoyed reading the above piece of analysis. I would be happy to receive your thoughts/comments at [kahhong.tai@gmail.com](kahhong.tai@gmail.com).
