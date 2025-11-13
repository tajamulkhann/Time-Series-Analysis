# 🪙 Gold Price Forecasting using Time Series Analysis

A time series project focused on forecasting gold prices using historical data, decomposition into trend/seasonality components, feature engineering, and advanced forecasting algorithms.

---

## 📌 Project Overview

This project provides a full forecasting pipeline: obtaining price history for gold, performing EDA to detect patterns and cycles, engineering lag/rolling features, training time-series models (ARIMA, Prophet, etc.), and evaluating predictions. The goal is to forecast future gold prices and provide insights for investors or market analysts.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** pandas, numpy, matplotlib, seaborn, statsmodels, Prophet, scikit-learn
* **Environment:** Jupyter Notebook / Google Colab

---

## 🔄 Workflow Summary

### 1. Data Collection

Dataset comprising historical gold prices (daily/weekly/monthly), possibly including features like date, open/high/low/close, volume, and external macroeconomic indicators.

### 2. Exploratory Data Analysis (EDA)

* Visualization of gold price trends over time
* Decomposition into trend, seasonal and residual components
* Stationarity tests (ADF/KPSS) and transformations applied if necessary
* Examination of patterns during economic events and cycles

### 3. Feature Engineering

* Creation of lag features (e.g., previous day/week price), rolling window statistics (moving average, volatility)
* Encoding calendar-time features: year, month, quarter, holiday flags
* Addition of exogenous variables (e.g., currency index, inflation, interest rates) if available
* Log-transform or differencing for stationarity
* Time-based train/test split (no random shuffle)

### 4. Modeling

Forecasting algorithms implemented include:

* **ARIMA / SARIMA** for capturing trend and seasonality
* **Prophet** for flexible modelling of trends and holiday/season effects
* **(Optional) Hybrid ML/TS models** combining classical time-series with machine learning features

### 5. Evaluation

Key metrics employed:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Percentage Error (MAPE)
* Forecast vs actual plots and residual diagnostics

**Result:** The forecasting models achieved strong accuracy and captured key market trends in gold prices, supporting future price projections and investment decisions.

### 6. Prediction & Insights

* Forecasted gold prices for upcoming periods (e.g., next 12 months)
* Identified key drivers of price fluctuations (seasonality, macroeconomic indexes, historical lag returns)
* Provided strategic insights for investors: timing buy/sell decisions, risk/return outlook

---

## 📁 Project Structure

```
Gold-Price-Forecasting/
│── data/
│── notebooks/
│── src/
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Strong seasonal and cyclical patterns influence gold prices
* Lag and rolling features significantly boosted forecasting performance
* Incorporating exogenous macroeconomic variables improved accuracy where available
* Forecasting framework supports financial decision-making with actionable outputs

---

## 🚀 Future Improvements

* Expand to multi-variate forecasting including external factors like inflation rate, USD index, oil prices
* Apply deep-learning sequence models (LSTM, Transformer) for longer-horizon or complex pattern modelling
* Deploy model via a dashboard or API for real-time forecasting and scenario simulation
* Incorporate live data feed to update forecasts and adapt to changing market dynamics
* Monitor and address model drift due to major economic events or structural market shifts

---

## 🧑‍💻 Author

**[Tajamul Khan](https://www.linkedin.com/in/tajamulkhann/) – Data Scientist & AI Engineer**

## Let's Connect <img src="https://github.com/JayantGoel001/JayantGoel001/blob/master/GIF/Handshake.gif" height="30px" style="max-width:100%;">

<div align="center">

<a href="https://www.linkedin.com/in/tajamulkhann/">
<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white">
</a>
<a href="https://www.instagram.com/tajamul.datascientist/" target="_blank">
<img src="https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=instagram&logoColor=white">
</a>
<a href="https://topmate.io/tajamulkhan" target="_blank">
<img src="https://img.shields.io/badge/Topmate-FF0000?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMDAgMTAwIj48Y2lyY2xlIGN4PSI1MCIgY3k9IjUwIiByPSI0MCIgZmlsbD0id2hpdGUiLz48L3N2Zz4=&logoColor=white">
</a>
<a href="https://www.whatsapp.com/channel/0029VaYs05jJkK7JKCesw42f">
<img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white">
</a>
<a href="https://t.me/tajamul_khan">
<img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white">
</a>
<a href="https://substack.com/@tajamulkhan">
<img src="https://img.shields.io/badge/Substack-%23006f5c.svg?style=for-the-badge&logo=substack&logoColor=FF6719">
</a>
<a href="https://www.kaggle.com/tajamulkhan">
<img src="https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white">
</a>
<a href="https://github.com/tajamulkhann">
<img src="https://img.shields.io/badge/Github-12100E?style=for-the-badge&logo=github&logoColor=white">
</a>
<a href="https://medium.com/@tajamulkhan">
<img src="https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white">
</a>
<a href="https://www.youtube.com">
<img src="https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white">
</a>
</div>
