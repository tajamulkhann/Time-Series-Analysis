# 📊 Walmart Sales Projection using Time Series Analysis

A time-series project focused on forecasting sales for Walmart using historical data, trend/seasonality decomposition, and forecasting algorithms.

---

## 📌 Project Overview

This project maps out a full workflow: acquiring historical weekly sales data for Walmart stores, conducting trend and seasonality analysis, creating key features (lags, rolling stats), applying time-series forecasting models (ARIMA/SARIMA, Prophet, etc.), and evaluating the forecasting performance. The objective is to project future sales and translate those forecasts into business-actionable planning insights for inventory and operations.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** pandas, numpy, matplotlib, seaborn, statsmodels, Prophet, scikit-learn
* **Environment:** Jupyter Notebook / Google Colab

---

## 🔄 Workflow Summary

### 1. Data Collection

Historical dataset containing features such as weekly sales total per store, date, holiday flag, and possibly macro variables (fuel price, CPI, unemployment) across multiple Walmart stores. ([Kaggle][1])

### 2. Exploratory Data Analysis (EDA)

* Visualised sales trends over time and by store/team
* Decomposed time series into trend, seasonal, and residual components
* Checked stationarity of series (ADF/KPSS tests) and applied transformations if required ([Medium][2])
* Investigated correlation with macro external factors and holiday periods

### 3. Feature Engineering

* Created lag features (weekly, monthly) and rolling window statistics (e.g., 4-week, 12-week moving average)
* Encoded holiday periods, season buckets, store-/department-level effects
* Differenced or logged series to achieve stationarity
* Split the dataset into training and testing windows

### 4. Modeling

Forecasting algorithms typically deployed:

* **ARIMA / SARIMA** for baseline time series forecasting with seasonality
* **FB Prophet** for rapid deployment with trend + seasonal + holiday effects
* **(Optional) Hybrid ML/TS models** combining supervised machine learning with lagged features and exogenous variables ([Our Blogs][3])

### 5. Evaluation

Common forecasting metrics include:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Percentage Error (MAPE)
* Residual plots and forecast vs actual visualisations

**Result:** The forecasting models showed strong performance in capturing overall trend and seasonality, enabling sales projections that support operational planning. For example, time-series studies on Walmart data found Gaussian Process models achieved notably low RMSE in forecast evaluation. ([ResearchGate][4])

### 6. Prediction & Business Insights

* Produced future sales forecasts (e.g., next 52 weeks) for Walmart stores
* Highlighted key drivers influencing sales fluctuations (seasonality, holidays, external factors)
* Translated forecasts into operational recommendations: inventory allocation, promotion planning, staffing/resource adjustments

---

## 📁 Project Structure

```
Walmart-Sales-Projection/
│── data/
│── notebooks/
│── src/
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Seasonal peaks and holiday periods significantly affect sales volumes
* Lagged features and rolling averages strongly improve forecasting accuracy over naïve models
* Macro variables and external holiday flags add predictive signal when included
* Forecasting results can directly guide business decisions such as inventory safety-stock levels and promo timing

---

## 🚀 Future Improvements

* Extend to store × department hierarchical time-series for finer-grained projection (e.g., using multivariate or hierarchical forecasting)
* Deploy deep-learning models (LSTM/Transformer) for longer-horizon or complex seasonal patterns
* Build an interactive dashboard (e.g., Streamlit) to display forecasts and scenario simulations for business stakeholders
* Incorporate real-time data (e.g., promotions, weather, local events) as exogenous inputs to improve forecast responsiveness
* Continuously evaluate model drift and retrain model periodically as retail patterns evolve

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
