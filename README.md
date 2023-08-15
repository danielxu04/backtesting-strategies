# Backtesting
A resource for backtesting various trading strategies to enhance performance/profitability of trading bots. Backtesting is a crucial step in the development and optimization of algorithmic trading strategies, allowing traders to assess their historical performance under different market conditions. It is of critical importance in assessing the merit of a trading strategy/system. <br /><br />

When backtesting, one must realize the importance of slippage and trading/brokerage cost when assessing the performance, as they are aspects that affect profitability of the strategy. <br /><br />

## 1. Monthly Portfolio Rebalancing
This strategy involves choosing a universe of stocks (large, mid, small, insdustry specific, etc.) and to use this as the source of your portfolio for backtesting. This version of Portfolio Rebalancing will construct and maintain a portfolio by picking stocks based on its monthly returns, with a large cap universe. <br /><br />

Every month, the portfolio will be rebalanced by removing the worst $x$ stocks, and replaced with the best $x$ stocks from our universe. You will find the Python file for backtesting in this repository, where comparisons are made between the strategy with that of a simple buy of the corresponding index.

## 2. Intraday Resistance Breakout
A resistance breakout materializes when a stock effectively traverses a predefined resistance threshold, ascertained through analysis of the price chart. This maneuver primarily entails the curation of stocks with heightened trading volume and substantial market activity, often referred to as pre-market movers, with the aim of optimizing potential yield.<br /><br />

In this example, we implement a 20-period rolling assessment of maximum and minimum price points. Within this framework, strategic positions will be initiated or liquidated contingent upon surpassing the established the resistance or dipping beneath the support. Furthermore, the delineation of our stop-loss directive is based on the previous day's closing price +/- the magnitude of the 20-period Average True Range (ATR), effectively serving as the dynamic threshold for our rolling stop-loss.
