# Stock Analysis and Visualization
![png-transparent-stock-market-design-elements-dynamic-arrows-charts-sketch-thumbnail](https://user-images.githubusercontent.com/114705723/235526321-876ef0b1-80bc-453d-b504-e052ef88036b.png)


This project focuses on analyzing and visualizing historical stock data for a selection of companies and indices, providing insights into various stock market indicators and measures.

## Features

- Retrieve historical stock data for selected tickers (e.g., AAPL, MSFT, AMZN, GOOGL, SPY, QQQ, TSLA)
- Compute various technical indicators, such as Moving Averages, Bollinger Bands, MACD, RSI, and more
- Conduct statistical analysis on stock returns, volatility, and correlations
- Generate plots for stock price history, return distributions, and technical indicators
- Perform event studies on economic indicators

## Libraries Used
Programming language: Python
- yfinance
- pandas
- numpy
- matplotlib
- seaborn
- ta
- fredapi

## Column Descriptions

- **Date**: Date of the stock observations (YYYY-MM-DD)
- **Open**: Opening price of the stock on the trading day
- **High**: Highest price reached by the stock during the trading day
- **Low**: Lowest price reached by the stock during the trading day
- **Close**: Closing price of the stock at the end of the trading day
- **Adj Close**: Adjusted closing price that takes into account dividends and stock splits
- **Volume**: Total volume of shares traded during the trading day
- **ATR**: Average True Range, a measure of volatility based on price ranges over a period of time
- **Returns**: Daily return of the stock, calculated as the percentage change in closing price
- **Volatility**: Stock volatility, measured as the standard deviation of returns over a period of time
- **SMA_50**: 50-day simple moving average of the closing price
- **EMA_50**: 50-day exponential moving average of the closing price
- **Upper**: Upper Bollinger Band, calculated as the sum of the simple moving average and twice the standard deviation of closing prices
- **Middle**: Middle Bollinger Band, equal to the 50-day simple moving average
- **Lower**: Lower Bollinger Band, calculated as the difference between the simple moving average and twice the standard deviation of closing prices
- **RSI**: Relative Strength Index, a technical momentum indicator that measures the magnitude of recent price changes to evaluate overbought or oversold conditions
- **MACD**: Moving Average Convergence Divergence, a technical indicator that measures the relationship between two exponential moving averages
- **MACD Signal**: MACD signal line, calculated as the 9-day exponential moving average of the MACD
- **Beta**: Stock beta coefficient, a measure of the stock's volatility relative to the overall market
- **Ticker**: Stock's ticker symbol

## How to Use

1. Set the desired tickers, start date, and end date for the historical data in the tickers, start_date, and end_date variables.
2. Run the script to collect historical data, calculate technical indicators, and perform statistical analysis.
3. Visualize the data using the provided plotting functions to gain insights into stock performance and market trends.
