# Daily Minimum Temperature Prediction

This repository focuses on predicting daily minimum temperatures using various time series forecasting models, including ARIMA, Prophet, and LSTM. The project includes data cleaning, exploratory data analysis, data visualization, and the implementation of different models.

## Getting Started

To run this project, follow the steps below:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/daily-min-temperature-prediction.git
   cd daily-min-temperature-prediction
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Code:**
   ```bash
   python main_script.py
   ```

## 1. Data Cleaning

Explore the dataset, check for missing values, and parse date into day, week, month, and season. Clean up column names and handle outliers.

```python
import numpy as np
import pandas as pd

# Load the dataset
df = pd.read_csv('daily_min_temp.csv')

# Data cleaning steps
# ... (code snippets)

# Additional features for time series analysis
df['season'] = df['month'].apply(get_season)
```

## 2. Data Visualization

Visualize the distribution of minimum temperatures, detect and remove outliers, and analyze average temperatures over time using seaborn and matplotlib.

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Data visualization snippets
# ... (code snippets)
```

## 3. ADF Test

Perform the Augmented Dickey-Fuller (ADF) test to check for stationarity in the time series.

```python
from statsmodels.tsa.stattools import adfuller

# ADF test snippets
# ... (code snippets)
```

## 4. ACF and PACF Plot

Explore autocorrelation and partial autocorrelation functions to determine ARIMA parameters.

```python
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf

# ACF and PACF plot snippets
# ... (code snippets)
```

## 5. Time Series Decomposition

Decompose and plot the components of the time series, including trend, season, and error.

```python
from statsmodels.tsa.seasonal import seasonal_decompose

# Time series decomposition snippets
# ... (code snippets)
```

## 6. Non-Seasonal ARIMA

Apply auto ARIMA model without seasonality.

```python
from pmdarima import auto_arima

# Non-seasonal ARIMA snippets
# ... (code snippets)
```

## 7. Seasonal ARIMA

Apply auto ARIMA model with seasonality and compare the results.

```python
# Seasonal ARIMA snippets
# ... (code snippets)
```

## 8. Prophet

Use the Prophet model for time series prediction and compare it with ARIMA models.

```python
from prophet import Prophet

# Prophet snippets
# ... (code snippets)
```

## 9. Cyclical Encoding

Cyclically encode days, weeks, months, and seasons for improved LSTM prediction.

```python
# Cyclical encoding snippets
# ... (code snippets)
```

## 10. LSTM

Implement LSTM (Long Short-Term Memory) neural network for time series prediction.

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import LSTM, Dense

# LSTM snippets
# ... (code snippets)
```

## Conclusion

For this dataset, LSTM proves to be the most effective model for predicting daily minimum temperatures. However, Prophet can be a suitable choice when computational resources are limited. Experiment with different models and parameters to optimize predictions for your specific use case.
