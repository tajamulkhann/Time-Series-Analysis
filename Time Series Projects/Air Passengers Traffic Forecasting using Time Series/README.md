# ✈️ Air Passengers Traffic Forecasting using Time Series Analysis

A time-series project focused on forecasting monthly air passenger traffic using historical data, seasonal decomposition, and advanced forecasting models.

---

## 📌 Project Overview

This project covers the full forecasting pipeline: acquiring monthly passenger data, conducting EDA to identify trend and seasonality, creating lag/rolling features, applying time-series forecasting models, and evaluating prediction accuracy. The goal is to forecast future passenger volumes and generate actionable insights for transport/aviation planning.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** pandas, numpy, matplotlib, seaborn, statsmodels, Prophet, scikit-learn
* **Environment:** Jupyter Notebook / Google Colab

---

## 🔄 Workflow Summary

### 1. Data Collection

Monthly air passenger traffic dataset spanning several years (includes features such as date, total passengers) used to model and forecast future demand. ([Medium][1])

### 2. Exploratory Data Analysis (EDA)

* Surfaced trends in passenger traffic over time
* Decomposed series into trend, seasonal and residual components
* Checked stationarity (ADF/KPSS tests) and applied transformations as needed ([Kaggle][2])
* Identified cyclical patterns and anomalies

### 3. Feature Engineering

* Created lag features (e.g., previous 12 months) and rolling statistics (e.g., 3-month, 12-month moving averages)
* Encoded time-based features: year, month, seasonality buckets
* Differenced or logged the series to handle non-stationarity
* Defined train/test splits respecting temporal ordering

### 4. Modeling

Forecasting algorithms implemented include:

* **ARIMA / SARIMA** (handles seasonal and non-seasonal components)
* **Prophet** (handles trend/holiday effects)
* **(Optional) Hybrid approaches** combining classical and machine-learning models for improved performance ([MDPI][3])

### 5. Evaluation

Key forecasting metrics used:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Percentage Error (MAPE)
* Visualisation of forecast vs actuals and residual diagnostics

**Result:** The best model achieved strong forecast accuracy, capturing both trend and seasonality, enabling reliable future passenger volume projections.

### 6. Prediction & Insights

* Forecasted future monthly passenger volumes (e.g., next 12 months)
* Derived business insights: peak travel months, growth trends, planning implications for capacity and resources
* Provided actionable recommendations: staffing, inventory, route planning based on forecasted demand

---

## 📁 Project Structure

```
Air-Passengers-Traffic-Forecasting/
│── data/
│── notebooks/
│── src/
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Clear upward trend and consistent seasonality (higher volumes in certain months)
* Lag features and rolling statistics improved forecast accuracy significantly
* Forecasting model outputs support strategic planning for airlines, airports and regulators
* External events (holidays, economic changes) may affect accuracy and require model adaptation

---

## 🚀 Future Improvements

* Expand to multivariate forecasting by incorporating exogenous variables (fuel price, GDP, holidays, weather)
* Apply deep-learning techniques (e.g., LSTM/Transformer) for long-horizon forecasts or non-linear patterns
* Deploy model via a web dashboard (Streamlit/Flask) for interactive exploration by stakeholders
* Implement adaptive retraining and monitoring for model drift as passenger behaviour evolves
* Explore hierarchical forecasting (by region/airport/route) for finer-grained insights

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
