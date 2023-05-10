# Strategic Analysis of Equity Investment Performance: A Comparative Study of Passive and Active Strategies

![image](https://user-images.githubusercontent.com/114705723/235526593-e7961a19-00e7-4384-999b-b79ece18e80c.png)

This project takes a comprehensive dive into the realm of investment strategies, benchmarking their efficacy when applied to a carefully chosen range of U.S. equities and indices. The scope of the study includes the following tickers: 'AAPL' (Apple Inc.), 'MSFT' (Microsoft Corporation), 'AMZN' (Amazon.com, Inc.), 'GOOGL' (Alphabet Inc.), 'TSLA' (Tesla, Inc.), 'SPY' (SPDR S&P 500 ETF Trust), and 'QQQ' (Invesco QQQ Trust).

The methodology employed in this project is multi-pronged, encompassing the retrieval of historical stock data, the computation of an array of technical indicators, and the development of both passive and active investment strategies.

The efficacy of these strategies is scrutinized across multiple investment time frames. Their returns and associated risk profiles are subject to rigorous statistical analysis and are visually represented for a more intuitive understanding.

This project is an endeavor to illuminate the relative performance of different investment strategies and to foster a more profound understanding of strategic decision-making in equity investments. The ultimate goal is to provide valuable insights that can guide investors in making informed decisions about their investment approaches.

## Features 

- 1. **Data Retrieval**: Retrieves historical stock data and computes various technical indicators including Simple Moving Averages (SMA), Exponential Moving Averages (EMA), Bollinger Bands, Moving Average Convergence Divergence (MACD), Relative Strength Index (RSI), and Average True Range (ATR).
- 2. **Data Analysis**: Conducts statistical analysis on stock returns, volatility, and correlations. Also provides stock betas and computes returns and volatility over a customizable window.
- 3. **Data Visualization**:  Generates visual plots for stock price history, return distributions, and technical indicators, offering a clear visual understanding of stock performance and movements over time.
- 4. **Investment Strategy Analysis**: Compares the performance of passive and active investment strategies on the selected stocks, including strategies like Buy-and-Hold (passive) and technical indicator-based trading rules (active).

## Delving into Insights: A Brief Visual Showcase from My Exploratory Data Analysis Journey

![distribution](https://user-images.githubusercontent.com/114705723/236968375-38c66b04-5ec1-4dc9-9507-8f9a7021cd10.png)

![historical_price](https://user-images.githubusercontent.com/114705723/236968487-53fd7b4b-8f83-4317-8cdc-9afd9cb14290.png)

![rsi](https://user-images.githubusercontent.com/114705723/236968545-fdce6023-8ccd-4ccf-b9ed-bab5c2dbafb0.png)

![correlation](https://user-images.githubusercontent.com/114705723/236968584-45173819-54e9-47a9-bdde-9bedc2f7a858.png)

## Event Study Analysis for Economic Indicators

As a key facet of my comprehensive data analysis project, I've applied an innovative technique known as event study analysis. This approach is specifically applied to three economic indicators obtained from the Federal Reserve Economic Data (FRED): Gross Domestic Product (GDP), Unemployment Rate (UNRATE), and Consumer Price Index for All Urban Consumers (CPIAUCSL). This analysis allows me to delve into the effects of certain events on these indicators, offering a profound understanding of economic trends and fluctuations.

Data Procurement and Refinement: The journey of this analysis starts with procuring time-series data for our chosen economic indicators - GDP, UNRATE, and CPIAUCSL, over a predetermined date range. To make this process efficient and seamless, I harness the power of the FRED API for reliable data extraction.

Application of Event Study Analysis: After gathering the necessary data, I deploy the event study methodology on this historical dataset. The process requires identification of an 'event window' around a specific date, the 'event date', and a thorough examination of each economic indicator's behaviour within this window.

The event window encompasses a specific number of periods both prior to and following the event date. This structured approach permits an exhaustive investigation into the event's impact on each economic indicator, considering both the aftermath (post-event) and the anticipatory period (pre-event).

This analytical process is replicated across each event date, with daily returns calculated within each event window. The returns are then averaged across all event windows, producing a representative illustration of each economic indicator's typical response to the event.

The culmination of this rigorous event study provides a panoramic view of the performance of the GDP, UNRATE, and CPIAUCSL during significant economic events. This broadens our understanding of the reaction of these specific indicators and the overarching economic climate, proving invaluable for informed economic and financial decision-making.

![CPIAUCSL_event_study](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/dc2f7157-4c91-4ad8-a2fe-0dd229f31f36)

![UNRATE_event_study](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/93164d42-7534-4fe0-be79-c44dd71ede0f)

![GDP_event_study](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/7a77394a-7bf9-40ed-89bc-f997d0be9439)




## Usage!


*The project is organized into several functions that handle tasks such as data retrieval, computation of technical indicators, data cleaning, data saving, and plotting of data and indicators.

*The project starts with defining the tickers of interest and the date range for which historical data is needed. The data is then downloaded, cleaned, and processed to calculate returns, volatility, and other technical indicators. The results are stored in separate dataframes for each ticker and also combined into a single dataframe for further analysis.

*The project also includes several plotting functions that provide visualizations of the historical price data, return distributions, and technical indicators for each stock and index.

*Lastly, the project checks for missing values in the data and calculates summary statistics, providing an overview of the distribution of returns and relation for each stock.

## Data Saving
The processed data is saved into Excel files for future reference and further analysis. Both individual and combined dataframes are saved.

## Conclusion
This project serves as a comprehensive tool for analyzing and comparing different investment strategies on selected equities. It provides both analytical and visual insights into the performance of these stocks, enabling users to make informed decisions about their investment strategies. Additionally, it lays a solid groundwork for building more complex trading algorithms and models.

## Future Work
While the project currently provides a robust analysis of selected stocks using predefined strategies, there's always room for enhancement. Future work could involve integrating more advanced trading strategies, incorporating machine learning algorithms for stock price prediction, or expanding the scope of the project to include other asset classes such as commodities, bonds, or cryptocurrencies.

## Requirements

The project uses Python as its core programming language, along with several libraries to aid in data retrieval, analysis, and visualization. These include:
- datetime: for handling date and time data.
- yfinance: to retrieve historical market data from Yahoo Finance.
- pandas: for data manipulation and analysis.
- numpy: for numerical computations.
- matplotlib and seaborn: for data visualization.
- ta: for technical analysis and computation of technical indicators.
- fredapi: to access economic data from the Federal Reserve Bank of St. Louis.
- scipy: for scientific and technical computing.

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
