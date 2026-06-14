# Crypto Portfolio Risk Dashboard

This project builds a portfolio risk dashboard for a multi-asset crypto portfolio using Python.

The dashboard analyses historical daily price data for BTC, ETH, SOL, BNB, XRP, ADA and LINK. It evaluates portfolio-level and asset-level risk using returns, volatility, drawdowns, correlations, Value at Risk, Expected Shortfall, risk contribution, stress testing and allocation scenario comparison.

The aim of the project is to understand not only which assets performed best historically, but which assets contributed most to portfolio risk.

## Project Objective

The main objective of this project is to answer the following question:

**How risky is a multi-asset crypto portfolio, and which assets are driving that risk?**

The dashboard is designed to move beyond simple return analysis by focusing on portfolio construction, downside risk and risk concentration.

## Assets Analysed

The dashboard analyses the following crypto assets:

* BTC
* ETH
* SOL
* BNB
* XRP
* ADA
* LINK

Daily price data is downloaded using `yfinance`.

## Sample Portfolio

The sample portfolio uses the following allocation:

* BTC: 40%
* ETH: 25%
* SOL: 15%
* BNB: 10%
* XRP: 4%
* ADA: 3%
* LINK: 3%

This allocation is not a recommendation. It is used only as a sample portfolio for historical risk analysis.

## What The Dashboard Measures

The notebook calculates:

* Portfolio value over time
* Daily portfolio returns
* Total return
* Annualised return
* Annualised volatility
* Sharpe ratio
* Best and worst daily return
* Maximum drawdown
* Value at Risk
* Expected Shortfall
* Asset-level risk metrics
* Daily return correlation matrix
* Rolling 30-day annualised volatility
* Risk contribution by asset
* Stress test scenarios
* Allocation scenario comparison

## Main Findings

The sample crypto portfolio produced very strong historical returns over the sample period, but those returns came with substantial volatility and deep drawdowns.

The portfolio experienced a maximum drawdown of almost 80%, showing that even a profitable long-term crypto allocation would have required the investor to tolerate severe temporary losses.

The asset-level analysis showed that SOL, XRP, LINK and ADA displayed particularly high standalone volatility and severe historical drawdowns.

The risk contribution analysis showed that portfolio weights do not fully explain portfolio risk. BTC represented the largest allocation, but contributed less risk than its weight alone would suggest. SOL had a smaller allocation, but contributed disproportionately to total portfolio risk because of its higher volatility.

The correlation matrix showed that all selected crypto assets were positively correlated. This means that diversification benefits were limited, especially during broad crypto market sell-offs.

The stress testing section confirmed that isolated asset-specific shocks were less damaging than broad market sell-offs where BTC, ETH and altcoins all fall together.

The allocation comparison showed that a high-beta altcoin tilt produced the strongest historical return, but also had the highest volatility and deepest drawdown. A BTC/ETH core allocation was more defensive, but sacrificed upside.

## Tools Used

* Python
* pandas
* NumPy
* matplotlib
* yfinance
* Google Colab

## Key Limitations

This dashboard is a simplified historical risk analysis and has several limitations.

The analysis uses historical daily price data from `yfinance`, so results may vary depending on data quality, asset availability and future price updates.

The sample begins when all selected assets have available price data, meaning earlier BTC and ETH history is excluded.

The dashboard assumes fixed portfolio weights and does not model rebalancing, taxes, trading fees, slippage or liquidity constraints.

The stress tests are hypothetical scenarios rather than forecasts. They are useful for understanding possible downside exposure, but they do not predict future market behaviour.

The Sharpe ratio is included as a simple risk-adjusted return measure, but it has limitations when applied to crypto assets because crypto returns can be highly volatile, skewed and exposed to extreme tail events.

## Possible Improvements

Future versions of this project could include:

* Portfolio rebalancing rules
* Rolling correlation analysis
* Rolling risk contribution
* Downside beta
* Monte Carlo simulations
* Stablecoin or cash allocations
* Transaction costs and slippage
* Live data integration
* Interactive dashboard functionality using Streamlit or Plotly Dash

## Disclaimer

This project is for educational and research purposes only. It is not financial advice, investment advice or a recommendation to buy or sell any crypto asset.

Cryptoassets are highly volatile and can result in substantial losses. The results shown in this project are based on historical data and simplified assumptions. They should not be relied upon for live trading or investment decisions.
