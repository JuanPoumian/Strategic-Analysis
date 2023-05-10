# Strategic Analysis of Equity Investment Performance: A Comparative Study of Passive and Active Strategies

![image](https://user-images.githubusercontent.com/114705723/235526593-e7961a19-00e7-4384-999b-b79ece18e80c.png)

This project takes a comprehensive dive into the realm of investment strategies, benchmarking their efficacy when applied to a carefully chosen range of U.S. equities and indices. The scope of the study includes the following tickers: 'AAPL' (Apple Inc.), 'MSFT' (Microsoft Corporation), 'AMZN' (Amazon.com, Inc.), 'GOOGL' (Alphabet Inc.), 'TSLA' (Tesla, Inc.), 'SPY' (SPDR S&P 500 ETF Trust), and 'QQQ' (Invesco QQQ Trust).

The methodology employed in this project is multi-pronged, encompassing the retrieval of historical stock data, the computation of an array of technical indicators, and the development of both passive and active investment strategies.

The efficacy of these strategies is scrutinized across multiple investment time frames. Their returns and associated risk profiles are subject to rigorous statistical analysis and are visually represented for a more intuitive understanding.

This project is an endeavor to illuminate the relative performance of different investment strategies and to foster a more profound understanding of strategic decision-making in equity investments. The ultimate goal is to provide valuable insights that can guide investors in making informed decisions about their investment approaches.

## Features 

- 1. **Data Retrieval**: Retrieves historical stock data and computes various technical indicators including Simple Moving Averages (SMA), Exponential Moving Averages (EMA), Bollinger Bands, Moving Average Convergence Divergence (MACD), Relative Strength Index (RSI), and Average True Range (ATR).
- 2. **Data Cleaning**: Ensures that the retrieved data is clean, accurate, and ready for analysis. This includes handling missing data and checking for data consistency.
- 3. **Data Analysis**: Conducts statistical analysis on stock returns, volatility, and correlations. Also provides stock betas and computes returns and volatility over a customizable window.
- 4. **Event Study Analysis for Economic Indicators**: This feature retrieves data for specified economic indicators, performs an event study around significant dates, calculates daily returns, and visualizes the average returns along with their variability. It effectively handles missing data for robust analysis.
- 5. **Data Visualization**:  Generates visual plots for stock price history, return distributions, and technical indicators, offering a clear visual understanding of stock performance and movements over time.
- 6. **Investment Strategy Analysis**: Compares the performance of passive and active investment strategies on the selected stocks, including strategies like Buy-and-Hold (passive) and technical indicator-based trading rules (active).

## Data Saving
The processed data is saved into Excel files for future reference and further analysis. Both individual and combined dataframes are saved.

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

## Delving into Insights: A Brief Visual Showcase from My Exploratory Data Analysis Journey

![distribution](https://user-images.githubusercontent.com/114705723/236968375-38c66b04-5ec1-4dc9-9507-8f9a7021cd10.png)

![historical_price](https://user-images.githubusercontent.com/114705723/236968487-53fd7b4b-8f83-4317-8cdc-9afd9cb14290.png)

![rsi](https://user-images.githubusercontent.com/114705723/236968545-fdce6023-8ccd-4ccf-b9ed-bab5c2dbafb0.png)

![volatility](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/0db30719-577c-4ea5-be9a-9d009a2866d8)

![bollinger_bands](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/2b54c6ac-022c-4ada-bde9-ea83cb48e796)

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

## Passive Strategy

**Result of My Analysis of Buy and Hold Returns for Selected Stocks**

The analysis for the 1-year period demonstrates a varying landscape of returns:

- Apple (AAPL) yielded a total return of 8.38% with an annualized return of 8.57%.
- Microsoft (MSFT) outperformed with a total return of 12.94% and an annualized return of 13.25%.
- Amazon (AMZN) and Google (GOOGL) experienced negative returns, with Amazon's total and annualized returns at -8.12% and -8.30% respectively, while Google's returns stood at -7.26% (total) and -7.42% (annualized).
- Tesla (TSLA) saw the most significant negative return, with a total return of -43.06% and an annualized return of -43.77%.
- The market indices SPY and QQQ returned positively, with SPY earning 2.83% (total) and 2.89% (annualized), while QQQ gained 5.11% (total) and 5.22% (annualized).

Buy and Hold Returns for the 3-Year Period:

Over the 3-year period, the returns showed a more positive trend:
- AAPL stood out with a total return of 130.25% and an impressive annualized return of 32.32%.
- MSFT also performed well, returning 73.10% in total and 20.23% on an annualized basis.
- AMZN underperformed with a negative total return of -10.30% and an annualized return of -3.59%.
- GOOGL and TSLA provided robust returns, with GOOGL returning 59.56% (total) and 16.99% (annualized), while TSLA skyrocketed with a total return of 214.94% and an annualized return of 46.99%.
- The market indices, SPY and QQQ, also returned positively, with SPY earning 53.18% (total) and 15.40% (annualized), while QQQ gained 49.85% (total) and 14.55% (annualized).

Buy and Hold Returns for the 5-Year Period:

In the 5-year period, the returns were predominantly positive:
- AAPL continued its strong performance with a total return of 284.51% and an annualized return of 31.07%.
- MSFT also showed strong returns, with a total return of 238.35% and an annualized return of 27.74%.
- AMZN provided a modest total return of 31.80% and an annualized return of 5.70%.
- GOOGL returned 102.63% in total and 15.24% on an annualized basis.
- TSLA was the clear standout, with a stunning total return of 714.03% and an annualized return of 52.38%.
- The market indices, SPY and QQQ, also returned positively, with SPY earning 69.69% (total) and 11.21% (annualized), while QQQ gained 100.82% (total) and 15.03% (annualized).

This in-depth analysis of buy and hold returns offers a comprehensive understanding of the performance of these stocks and market indices over various time periods. It provides a clear picture of the long-term profitability of these investments, with some companies such as Apple (AAPL) and Microsoft (MSFT) consistently performing well across all periods. On the other hand, companies like Tesla (TSLA) show higher volatility, with exceptional returns in the longer term despite short-term losses.

This analysis serves as a valuable tool for making informed investment decisions and understanding market trends. It also highlights the importance of considering the time horizon in investment strategies. While some stocks may underperform in the short term, they may yield significant returns over a longer period, underlining the potential advantages of a buy and hold strategy.

The investigation of these returns, along with the detailed examination of other market indicators, forms a core part of my data analysis project, aimed at providing a holistic understanding of the financial market landscape.

![1-Year_Buy_and_Hold_Returns](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/74310e13-93cd-4791-b84e-c1bd2cc7c778)

![3-Year_Buy_and_Hold_Returns](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/b197d50d-8641-4a3f-8f1c-880d45828715)

![5-Year_Buy_and_Hold_Returns](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/ba1b2cb6-e31d-4722-90d2-a8778f24c9f7)

## Active Strategies

**Trading Strategy Optimization Results: RSI and MACD-EMA**

This part of the document presents the results of an optimization study conducted on two trading strategies:
1. RSI (Relative Strength Index)
2. MACD-EMA (Moving Average Convergence Divergence - Exponential Moving Average)

The optimization was applied to the following stock tickers: AAPL, MSFT, AMZN, GOOGL, TSLA, SPY, and QQQ.

**Evaluation Metrics**:

The performance of each strategy was evaluated based on several metrics:

- Total Return
- Average Return
- Sharpe Ratio
- Maximum Drawdown

These metrics provide a comprehensive view of each strategy's performance, allowing us to balance returns against risk.

**Optimization Parameters**:

The best RSI parameters found were 80 for the overbought level and 35 for the oversold level. For the MACD-EMA strategy, the optimal parameters were a short EMA of 15 days and a long EMA of 100 days.

**Optimization Results**:

**Apple Inc. (AAPL)**: The MACD-EMA strategy outperformed the RSI strategy with a total return of 46.72%, compared to RSI's 24.50%. The Sharpe Ratio was higher for the MACD-EMA strategy (14.17 vs -23.28), indicating better risk-adjusted returns.

**Microsoft Corp. (MSFT)**: Similar to AAPL, the MACD-EMA strategy outperformed the RSI strategy, albeit with a lower total return of 0.39% compared to RSI's 1.84%. The Sharpe Ratio was higher for the MACD-EMA strategy, suggesting better risk-adjusted returns.

**Amazon.com Inc. (AMZN)**: The RSI strategy provided a higher total return of 20.38%, but the MACD-EMA strategy showed a higher Sharpe Ratio of 10.78, indicating better risk-adjusted returns.

**Alphabet Inc. (GOOGL)**: The RSI strategy delivered a higher total return of 16.58%, but the MACD-EMA strategy had a higher Sharpe Ratio of 13.10, suggesting better risk-adjusted returns.

**Tesla Inc. (TSLA)**: The MACD-EMA strategy outperformed the RSI strategy with a total return of 56.07% compared to RSI's 22.51%. The Sharpe Ratio was higher for the MACD-EMA strategy, indicating better risk-adjusted returns.

**SPDR S&P 500 ETF Trust (SPY)**: The RSI strategy provided a higher total return of 1.34%, but the MACD-EMA strategy showed a higher Sharpe Ratio of 13.66, suggesting better risk-adjusted returns.

**Invesco QQQ Trust (QQQ)**: The RSI strategy delivered a higher total return of 2.04%, but the MACD-EMA strategy had a higher Sharpe Ratio of 12.80, indicating better risk-adjusted returns.

These results demonstrate the importance of parameter optimization and strategy selection for different stocks. It's crucial to note that past performance does not guarantee future results. Therefore, these strategies should be tested on out-of-sample data before live trading.

Here's a glimpse of the charts I've generated, with Apple as an example:

![AAPL_MACD_EMA_strategy](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/ee392972-95b4-4d1b-bfb1-daf8211de3ec)

![AAPL_RSI_strategy_1](https://github.com/JuanPoumian/Stock-Analysis-and-Visualization/assets/114705723/cbe33d8c-68d5-4382-bda7-e6682b368784)

## Conclusion

A comparative review of passive and active investment strategies, as revealed by the data analysis of selected stocks, offers compelling insights into their respective performances.

The passive strategy of 'Buy and Hold' shows a diverse return landscape over a 1-year, 3-year, and 5-year period. Consistent performers like Apple and Microsoft demonstrate the long-term profitability of this approach despite market fluctuations. Simultaneously, the high volatility yet exceptional returns of Tesla remind us of the potential benefits of long-term investment, even in the face of short-term losses. This supports the classic wisdom of 'time in the market' over 'timing the market'.

On the other hand, active strategies such as RSI and MACD-EMA, optimized for individual stocks, also yield significant results. The key lies in balancing the returns against the risk, as reflected in the Sharpe Ratio. For instance, Apple and Tesla showed superior total returns with the MACD-EMA strategy, while stocks like Amazon and Alphabet performed better with the RSI strategy in terms of total returns. However, the MACD-EMA strategy often demonstrated better risk-adjusted returns, evident in a higher Sharpe Ratio across most stocks.

In essence, the choice between passive and active strategies is not a binary one. The comprehensive analysis suggests the need for a nuanced approach that considers the stock's performance history, market conditions, risk tolerance, and investment horizon. The active strategy's increased returns could compensate for its higher time and effort commitment. In contrast, a passive strategy might be more suitable for investors preferring a 'set-and-forget' approach, betting on the long-term growth of the market.

The detailed examination of these strategies reinforces the importance of data-driven decision-making in investment management. It underscores the value of robust data analysis tools that can provide a holistic understanding of the financial market landscape, allowing investors to navigate it more confidently and effectively.

## Future Work
Potential future enhancements include integrating sophisticated trading strategies, applying machine learning for stock forecasting, and broadening the asset classes covered to include commodities, bonds, or cryptocurrencies.
