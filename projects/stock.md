---
layout: default
title: Stock Price Analysis and Prediction
github_url: https://github.com/will51mps0n/stock_price_analysis

---

[← Back to Home](../index.html)

# Stock Price Analysis and Prediction
[View Code on GitHub](https://github.com/will51mps0n/stock_analysis)

---

## Overview

This project presents a comprehensive approach to **Stock Price Analysis and Prediction**, encompassing:

1. **Data Retrieval:**  
   - Fetching historical stock data using the Financial Modeling Prep (FMP) API.
   
2. **Technical Indicator Computation:**  
   - Calculating various technical indicators to analyze stock trends and volatility.
   
3. **Machine Learning Models:**  
   - Implementing models such as Linear Regression, Random Forest, and Long Short-Term Memory (LSTM) networks for stock price prediction.

---

## Features

### Data Retrieval:
- **Financial Modeling Prep (FMP) API Integration:**
  - Utilizes FMP's free API to obtain real-time and historical stock data, supporting over 25,000 stocks across multiple exchanges. :contentReference[oaicite:0]{index=0}

### Technical Indicator Computation:
- **Moving Averages:**
  - Calculates Simple Moving Averages (SMA) and Exponential Moving Averages (EMA) over specified windows to identify price trends.
  
- **Relative Strength Index (RSI):**
  - Computes RSI to assess the magnitude of recent price changes and evaluate overbought or oversold conditions. :contentReference[oaicite:1]{index=1}

- **Moving Average Convergence Divergence (MACD):**
  - Measures the relationship between two EMAs to identify bullish or bearish momentum. :contentReference[oaicite:2]{index=2}

- **Bollinger Bands:**
  - Calculates Bollinger Bands to analyze price volatility and potential overbought or oversold signals. :contentReference[oaicite:3]{index=3}

- **Volatility Metrics:**
  - Determines historical volatility and Average True Range (ATR) to gauge market fluctuations.

- **On-Balance Volume (OBV):**
  - Computes OBV to relate price changes to trading volume, aiding in trend confirmation.

### Machine Learning Models:
- **Linear Regression:**
  - Implements linear regression to model the relationship between lagged closing prices and predict future prices.

- **Random Forest Regressor:**
  - Utilizes ensemble learning to enhance prediction accuracy and manage overfitting.

- **Long Short-Term Memory (LSTM) Networks:**
  - Applies LSTM networks to capture temporal dependencies in sequential stock price data for improved forecasting.

---

## How It Works

1. **Data Retrieval:**
   - The `stock_history` function fetches historical stock data for a specified ticker, year, and month using the FMP API. :contentReference[oaicite:4]{index=4}

2. **Technical Indicator Computation:**
   - Functions like `calculate_moving_averages`, `calculate_rsi`, and `calculate_macd` compute respective technical indicators using the `ta` library.

3. **Machine Learning Modeling:**
   - The `prepare_data` function structures the data with lag features for regression models.
   - The `train_predict_lr_rf` function trains and evaluates Linear Regression and Random Forest models.
   - The `prepare_lstm_data` and `train_predict_lstm` functions handle data preparation and training for LSTM networks.

4. **Prediction and Evaluation:**
   - Models are evaluated using metrics such as Root Mean Squared Error (RMSE) to assess prediction accuracy.

---

## Technologies
- Python
- pandas
- NumPy
- requests
- BeautifulSoup
- ta (Technical Analysis Library)
- scikit-learn
- TensorFlow/Keras
- matplotlib

---

[← Back to Home](../index.html)
