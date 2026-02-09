# Time Series Sample Code

## Libraries I Usually Use
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

from statsmodels.tsa.stattools import adfuller, kpss
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.statespace.sarimax import SARIMAX
from statsmodels.stats.diagnostic import acorr_ljungbox
```

## 1️⃣ Problem Understanding
“Target = sales, horizon = next 12 weeks, daily granularity, focus on interpretability.”

## 2️⃣ Data Collection & Time Index
```python
df['date'] = pd.to_datetime(df['date'])
df = df.sort_values('date')
df = df.set_index('date')
df = df.asfreq('D')      # enforce daily frequency
df = df[~df.index.duplicated()]
```

## 3️⃣ EDA (Trend & Seasonality)
```python
df['sales'].plot(figsize=(10,4))
plt.show()

df['sales'].rolling(7).mean().plot(label='7-day MA')
plt.legend()
plt.show()
```
👉 “I visually check trend, seasonality, volatility.”

## 4️⃣ Missing Values
```python
df.isna().sum()
df['sales'] = df['sales'].ffill()      # or bfill / interpolate
```
👉 “Never random fill — time logic matters.”

## 5️⃣ Outlier Treatment
```python
rolling_med = df['sales'].rolling(7).median()
df['sales'] = np.where(
    abs(df['sales'] - rolling_med) > 3 * df['sales'].std(),
    rolling_med,
    df['sales']
)
```
👉 “I cap or smooth unless business-driven.”

## 6️⃣ Stationarity Tests
```python
adf_p = adfuller(df['sales'])[1]
kpss_p = kpss(df['sales'], regression='c')[1]

print(adf_p, kpss_p)
```
👉
ADF p < 0.05 → stationary
KPSS p > 0.05 → stationary

## 7️⃣ Differencing
```python
df['sales_diff'] = df['sales'].diff().dropna()
```
👉 “I re-test stationarity after differencing.”

## 8️⃣ ACF & PACF
```python
plot_acf(df['sales_diff'].dropna(), lags=30)
plot_pacf(df['sales_diff'].dropna(), lags=30)
plt.show()
```
👉
PACF → p
ACF → q
Seasonal spikes → P, Q

## 9️⃣ Train–Test Split (Time-based)
```python
train = df.iloc[:-30]
test  = df.iloc[-30:]
```

## 🔟 Model Building (SARIMA Example)
```python
model = SARIMAX(
    train['sales'],
    order=(1,1,1),
    seasonal_order=(1,1,1,7)
)
results = model.fit()
```

## 1️⃣1️⃣ Model Evaluation
```python
pred = results.forecast(steps=30)
rmse = np.sqrt(((pred - test['sales'])**2).mean())
print(rmse)
```

## 1️⃣2️⃣ Residual Diagnostics
```python
residuals = results.resid
plot_acf(residuals)
plt.show()
acorr_ljungbox(residuals, lags=[10], return_df=True)
```
👉 “Residuals should be white noise.”

## 1️⃣3️⃣ Forecasting
```python
forecast = results.get_forecast(steps=30)
forecast_ci = forecast.conf_int()
```

## 1️⃣4️⃣ Business Validation (talk)
“I sanity-check trends, spikes, and confirm with business stakeholders.”

## 1️⃣5️⃣ Deployment & Monitoring (talk)
“Automated retraining + monitor data drift and error drift.”

## 🎯 One-Line Interview Summary
“I follow a full pipeline: EDA → stationarity → SARIMA modeling → residual diagnostics → business validation, using statsmodels and pandas.”
