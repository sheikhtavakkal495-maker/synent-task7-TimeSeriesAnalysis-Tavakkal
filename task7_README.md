# synent-task7-timeseriesanalysis-yourname

## Problem Statement

Stock prices change daily and it can be hard to tell if a price movement is part of a long-term trend or just short-term noise. The goal was to analyze historical stock price data to identify trends, check for seasonality, and optionally forecast future prices.

## Dataset Details

- Dataset: Historical Stock Price Dataset
- Source: Kaggle / Yahoo Finance
- Contains daily open, high, low, close prices and volume for a stock over several years.
- Format: CSV
- Stock used: Apple (AAPL) from 2015 to 2023

## Approach

I set the date column as the index and focused on the closing price. A 30-day and 90-day rolling average was plotted over the raw price to show the overall direction. I then used seasonal decompose from statsmodels to break the series into trend, seasonal, and residual parts. Daily returns were also calculated and plotted to visualize volatility. As an optional step I tried an ARIMA model to forecast the next 30 days of closing prices.

## Results

- The stock shows a clear upward trend from 2015 to early 2022 followed by a correction
- There is mild seasonality that loosely aligns with quarterly earnings periods
- The highest volatility period was early 2020 during the market crash
- The ARIMA model gave a reasonable forecast with confidence intervals that widened over time as expected
