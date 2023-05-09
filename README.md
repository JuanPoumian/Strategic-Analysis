# Strategic Analysis of Equity Investment Performance: A Comparative Study of Passive and Active Strategies

![image](https://user-images.githubusercontent.com/114705723/235526593-e7961a19-00e7-4384-999b-b79ece18e80c.png)

The objective of this project is to analyze and compare the performance of various investment strategies applied to a selection of U.S. equities and indices. The project involves retrieving historical stock data for selected tickers, calculating a range of technical indicators, and developing both passive (Buy-and-Hold) and active (technical indicator-based) investment strategies. The performance of these strategies will be assessed over multiple investment horizons, and their returns and associated risk will be statistically analyzed and visually represented. This comprehensive study aims to provide insights into the efficacy of different investment strategies in the context of the selected stocks, fostering a deeper understanding of strategic decision-making in equity investments.

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
- idea = # Define the purpose of each library
"""
datetime: provides classes for working with dates and times.
yfinance: allows downloading stock data from Yahoo Finance.
pandas: provides data structures and tools for data manipulation and analysis.
numpy: provides arrays and numerical operations for data analysis.
ta: provides technical indicators for financial analysis.
scipy.optimize: provides optimization algorithms for numerical optimization.
matplotlib: provides plotting functionality.
seaborn: provides higher-level interface for visualizing data.
"""

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
