# SummerFund




Goal - >2% p.w. return
Predict the probability of moving up/down for various products
Predict the size of the moves, e.g. the probability of a 1% move is 80%
Healthy winning ratio and risk/reward, e.g. >50% winning ratio with 2/1 reward risk.
How many trades needed to make 2% p.w. ? How much leverage is required?

Trading strategy and rules
Strategies may differ across various asset classes, .e.g equity, bond, commodity, FX.
Need to be market neutral overall? i.e. long/short offsetting (negatively correlated) asset classes (or this can be dealt with a correlation limit?)
Capture both mean reversion and trend
Use fair value gap to determine initial long/short direction and size
Position size = risk budget * value gap per vol * confidence
Confidence = backtested winning ratio of trading signals. Static or dynamic?
Half life for vol and correlation ?
Use short term indicators for daily trading (or intra-day). 
Max out budget if market value is 20%? 30%? away from fair value. The bigger the gap the higher the confidence.
Model prediction time frame: next day, week, month, year. What’s the appropriate weights? The longer the term, the higher the risk, so less %?
Daily rebalancing
Trade 1, based on fair value gap moves, which determine the direction and size
Trade 2, use indicators to predict the move for the next day, e.g. probability of moving up/down, by how much. Essentially predict the FV gap for tomorrow. 
Trade 1&2 may net off each other, or double up.
Regular rebalance 2 times a day, London & NY. Plus event driven rebalance, e.g. mkt moves more than 1% during Asian hours. (this is related to trading materiality)
Fair value is based on:
Fundamentals, 50%? Or dynamic? Based on backtrsting, but shouldn’t renew often.
Long term trend (1 year?), expected equity premium or a long term average number?
Refresh quarterly (fixed date?)
Equities
100 * (1+R)^n
R = Risk free plus equity risk premium 
Risk free rate = 10y Govt bond
Equity_vol - Bond_vol (can use UST ETF to work out bond vol)
Bottom up DCFs, or P/E?
Top down multiples
Bonds
Norminal yield should equal to GDP long term growth rate? But there will be differences between EM and DM given different growth potential 
Inflation expectation, so real yield at least 0%
GDP v.s. Unemployment rate, expected high or low yield environment
Monetary policy, in a hiking cycle?
Spread to AAA corporate bond
Flight to safety , asset allocations considerations 
Confidence on fundamental impact on fair value if trading short term. Some indicators will have a bigger impact if they surprise market expectations. (Machine learning on data release and market reactions?)
FX
Interest rate differential, 2yr? (This should have inflation priced in)
Balance of payment (capture trade and capital flows)
Risk premium and market volatility 
Commodities
Supply/production v.s. demand
Sizing
Initial size
C * B * V

C = confidence about VP gap (should start from 10-30% if not confident) , determined by winning ratio from backtesting 
B = risk budget, allocation based on expected risk/reward, and also actual performance (ML opportunity?)
V = value gap per vol

Rebalance size, driven by chang of V, and predicted change of V from technical indicators 
Signals/indicators
Technical: Each individual indicator has buy, sell, and hold rating each day
Trend
Momentum
Volume
Volatility
Factors
Combination, and patterns for various products/asset classes, e.g. equity v.s. commodity
Fundamental/macro indicators
Economic data
Money supply, e.g. M2 growth and velocity of money
Forward looking interest rate
Earnings data
Leverage level in household and other sectors
Geopolitical risks, propaganda measures, narrative trends and where and when it started 
Risk premium for various asset classes
Alternative data, e.g. social media, news trends (web scriping)


Trading products
Eligibility
Must have mean-reversion nature
Liquid, and low cost to trade, e.g transaction, holding, carry cost.
No single stocks, as no need to have idiosyncratic risk
Weekly vol is greater than the trading materiality, e.g 1%
Less structural shifts risk 
Products

Equities
Bonds
Commodities
FX vs USD


S&P500
UST 10y
Gold
AUD






Silver
EUR






Corn
JPY






Rice
GBP






Oil?
CHF





How to allocate a budget? 25% each category? Based on profitability from backtesting results? Or dynamically adding more allocation to better performance asset classes?


Risk and budget management - this is the IP!
Never all-in!
Risk budget per product. Vol based rather than % of notional. 
Dynamic risk budget, so more budget for performing strategies, but should still be a cap. Cap is reviewed regularly but not too frequently, to capture view on long term structural shifts.
Materiality to trade, 1% move? More for budget reason than science, e.g. trading cost and noise 
Limits
Capital usage
Correlation
Risk/reward
Tail risk, stress test (e.g. 95% VaR)
Liquidity risk, means?

Backtesting
Which indicators (or combination of) are useful for which products
Each day, each technical indicator would have buy/sell/hold signals. What’s the probability of accurate prediction for the following day? For a 1 (2 or 3) year running period. 
If combining 2 or more indicators, would the prediction accuracy improve?
Adding fundamental indicators (need to define their buy/sell signal)
How to avoid over fitting 
Historical fair value gap
What’s the optimal “all-in” FV gap, e.g. 20 or 30%
Backtest trading materiality level, 1 or 2 %
Trade sizing
Test budget allocation for each product category and individual trade


Limits
Test opportunity cost from various limits

On-going maintenance and development 
Signal library, predictability time series 
Data daily refresh
Performance tracking
Machine learning?
Auto trading? Maybe 10% the program?
