# **CRYPTOCURRENCIES TIME SERIES** :chart_with_upwards_trend:

This repository contains some notebooks with analysis of 10 cryptocurrencies and a comparison of several models' predictions for ETH and BTC: ARIMA, XGBoost, LSTM, Prophet, and Gradient Boosting. 


## Cryptocurrencies Comparison

In the first stage, a comparison of 10 cryptocurrencies was carried out. For that, data from `yfinance` from January 2019 to June 2023 were downloaded and the following features were extracted:

- **Date**: Date of the trade
- **Open**: The price at which the stock began
- **High**: Highest price during that trading day
- **Low**: Lowest price during that trading day
- **Close**: The price at which the stock ended
- **Adj Close**: The closing price after adjustments for splits, right offerings, and dividends, to make prices comparable over time
- **Volume**: Total stocks traded that day

Adj Close offers an accurate comparison between cryptocurrencies and the values were plotted. 

<p align="center">
<img align="center" src="./EDA_notebooks/images/10_currencies.png"> 

</p>

<p align="center">
<img align="center" src="./EDA_notebooks/images/cum_returns.png"> 

</p>


</p>

<p align="center">
<img align="center" src="./EDA_notebooks/images/heatmap.png"> 

</p>


</p>

<p align="center">
<img align="center"src="./EDA_notebooks/images/ma20_100.png"> 

</p>


</p>

<p align="center">
<img align="center"  src="./EDA_notebooks/images/ma50.png"> 

</p>
