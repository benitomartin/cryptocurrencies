# **CRYPTOCURRENCIES TIME SERIES** :chart_with_upwards_trend:

This repository hosts a collection of notebooks featuring an in-depth analysis of ten cryptocurrencies, along with a comparative study of predictions made by various models specifically for BTC. The following models were meticulously evaluated:

- ARIMA
- XGBoost
- LSTM
- Prophet
- Gradient Boosting

## Cryptocurrencies Comparison

In the first stage, a comparison of 10 cryptocurrencies was carried out. For that, data from `yfinance` from January 2019 to June 2023 were downloaded and the following features were extracted:

- **Date**: Trade date
- **Open**: Opening stock price
- **High**: Peak price during the trading day
- **Low**: Lowest price during the trading day
- **Close**: Closing stock price
- **Adj Close**: Adjusted closing price, accounting for splits, offerings, and dividends for accurate historical comparison
- **Volume**: Total trade volume for the day

The utilization of Adj Close allows for meaningful comparisons between cryptocurrencies, and these values are thoughtfully visualized through multiple subplots.

<p align="center">
<img align="center" src="./EDA_notebooks/images/10_currencies.png"> 

</p>

In the pursuit of enhanced insights, **returns** were computed, providing a measure of profitability over a specific period. Furthermore, cumulative returns were calculated to express the overall price change of a cryptocurrency over time.

<p align="center">
<img align="center" src="./EDA_notebooks/images/cum_returns.png"> 

</p>

Notably, a pattern emerges revealing varying **degrees of correlation** between different cryptocurrencies. BCH, ETH, EOS, and LTC exhibit a strong positive correlation, implying that when one of these cryptocurrencies experiences an increase, the others tend to follow suit. Conversely, BSV displays a weaker correlation with BNB and XRP.

</p>

<p align="center">
<img align="center" src="./EDA_notebooks/images/heatmap.png"> 

</p>

The application of a **moving average**, also known as a rolling average, helped in smoothing out short-term price fluctuations to identify longer-term trends or cycles. For instance, a 7-day moving average captures short-term trends, while a 100-day rolling average highlights more substantial trends. The use of arithmetic mean was adopted in this context.

From the plotted chart, it is discernible that in May of 2021, the price dipped below the 50-day moving average, signifying a **downward trend**. Conversely, in August 2021, the price surged above the moving average, indicating an **upward trend**.

</p>

<p align="center">
<img align="center"src="./EDA_notebooks/images/ma20_100.png"> 

</p>

Further observations reveal that around May of 2021, the 20-day moving average crossed below the 100-day moving average, signaling a shift towards a downward trend and serving as a **sell signal**. Conversely, by August 2021, the 20-day moving average crossed above the 100-day moving average, marking an upward trend and presenting a **buy signal**.

</p>

<p align="center">
<img align="center"  src="./EDA_notebooks/images/ma50.png"> 

</p>


## BTC Analysis

The subsequent stage of analysis focused on an in-depth exploratory data analysis (EDA) of BTC. This time frame involved data sourced from Binance, spanning from January 2020 to May 2023. The data attributes from Binance include:

- **open_time**: Opening time of the specified period
- **open**: Opening price of the trading instrument for the given period
- **high**: Highest price attained by the trading instrument during the specified period
- **low****: Lowest price reached by the trading instrument during the specified period
- **close**: Closing price of the trading instrument for the given period
- **volume**: Total trading volume, representing the quantity of the trading instrument, during the specified period
- **close_time**: Closing time of the specific period
- **quote_volume**: Total volume in terms of the quote asset, which determines the trading instrument's value
- **count**: Number of trades occurring during the specified period
- **taker_buy_volume**: Volume of the quote asset bought by market takers during the period
- **taker_buy_quote_volume**: Volume of the base asset bought by market takers during the period
