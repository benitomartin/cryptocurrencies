# **CRYPTOCURRENCIES TIME SERIES** :chart_with_upwards_trend:

This repository contains some notebooks with an analysis of 10 cryptocurrencies and a comparison of several models' predictions for ETH and BTC. The following models were compared:
- ARIMA
- XGBoost
- LSTM
- Prophet
- Gradient Boosting. 


## Cryptocurrencies Comparison

In the first stage, a comparison of 10 cryptocurrencies was carried out. For that, data from `yfinance` from January 2019 to June 2023 were downloaded and the following features were extracted:

- **Date**: Date of the trade
- **Open**: The price at which the stock began
- **High**: Highest price during that trading day
- **Low**: Lowest price during that trading day
- **Close**: The price at which the stock ended
- **Adj Close**: The closing price after adjustments for splits, right offerings, and dividends, to make prices comparable over time
- **Volume**: Total stocks traded that day

Adj Close offers an accurate comparison between cryptocurrencies and the values were plotted in several subplots.

<p align="center">
<img align="center" src="./EDA_notebooks/images/10_currencies.png"> 

</p>

However, in order to get a better insight the returns were calculated as it represents the money made or lost on an investment over some period of time and additionally, the cumulative return to express the total change in the price of a cryptocurrency over time.

<p align="center">
<img align="center" src="./EDA_notebooks/images/cum_returns.png"> 

</p>

It can be also appreciated that some cryptocurrencies are more correlated to each other than others. We can see that BCH, ETH, EOS, and LTC are highly correlated. That means for example that when BCH goes up, ETH also goes up, and when Bitcoin falls, ETH also falls. On the other hand, BSV is less correlated to BNB and XRP.

</p>

<p align="center">
<img align="center" src="./EDA_notebooks/images/heatmap.png"> 

</p>

Moving average (rolling average) was used to smooth out "noise", which are random short-term fluctuations in price, to identify long-term trends or cycles. For example, a 7-day moving average reflects short-term trends in the stock market, whereas a 100-day rolling average indicates major trends in the stock market. Here the **arithmetic** mean was calculated.

We can observe from the chart that in May of 2021, the price crosses below the 50-day MA, which indicates a **downward trend**, and in August 2021, the price crosses above the MA, which shows an **upward trend**.

</p>

<p align="center">
<img align="center"src="./EDA_notebooks/images/ma20_100.png"> 

</p>

We can also observe that around May of 2021, the 20-day MA crosses below the 100-day MA. It indicates that the trend is shifting **downwards**, and it’s a **sell signal**. Towards August 2021, the 20-day MA crosses above the 100-day MA. It shows that the trend is shifting **upwards**, and it’s a **buy signal**.

</p>

<p align="center">
<img align="center"  src="./EDA_notebooks/images/ma50.png"> 

</p>


## Cryptocurrencies Comparison

