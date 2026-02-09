# Libraries I Usually Use
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

from statsmodels.tsa.stattools import adfuller, kpss
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.statespace.sarimax import SARIMAX
from statsmodels.stats.diagnostic import acorr_ljungbox
```

## 1️⃣ Problem Understanding (talk, not code)
“Target = sales, horizon = next 12 weeks, daily granularity, focus on interpretability.”

## 2️⃣ Data Collection & Time Index
```python
df['date'] = pd.to_datetime(df['date'])
df = df.sort_values('date')
df = df.set_index('date')
df = df.asfreq('D')      # enforce daily frequency
df = df[~df.index.duplicated()]
```