# Daily Minimum Temperature Prediction

This repository focuses on predicting daily minimum temperatures using various time series forecasting models, including ARIMA, Prophet, and LSTM. The project includes data cleaning, exploratory data analysis, data visualization, and the implementation of different models.


# Project Overview

## Temperature Time Series Analysis and Prediction

### Introduction
This project aims to analyze and predict minimum daily temperatures using a time series dataset spanning 10 years, from 1/1/1981 to 31/12/1990. The dataset, loaded from 'daily_min_temp.csv,' undergoes comprehensive data cleaning, visualization, and modeling using statistical and machine learning techniques.

### 1. Data Cleaning
- Exploration of data structure and overview.
- Identification and handling of missing values.
- Parsing date information into day, week, month, and season.
- Renaming columns for clarity.
- Creation of a 'season' column based on months.

### 2. Data Visualization
- Utilization of Seaborn and Matplotlib for visualizing temperature distribution and detecting outliers.
- Identification of outliers based on average temperatures over time.
- Removal of outliers where minimum temperature exceeds 20°C.
- Seasonal, monthly, weekly, daily, and yearly analysis of temperature variations.

### 3. Augmented Dickey-Fuller (ADF) Test
- Verification of time series stationarity.
- Rolling window analysis to assess mean and variance stability.
- ADF test results indicating stationarity.

### 4. Autocorrelation and Partial Autocorrelation Analysis
- Examination of autocorrelation and partial autocorrelation functions to determine ARIMA parameters (p and q).

### 5. Time Series Decomposition
- Decomposition of time series into trend, seasonality, and residuals.
- Assessment of autocorrelation of residuals.

### 6. Non-seasonal ARIMA Modeling
- Application of auto ARIMA model without seasonality.
- Evaluation of model performance and visualization of results.

### 7. Seasonal ARIMA Modeling
- Application of auto ARIMA model with seasonality.
- Comparative analysis with non-seasonal ARIMA.

### 8. Prophet Modeling
- Utilization of the Prophet model for time series prediction.
- Comparison of results with ARIMA models.

### 9. Cyclical Encoding
- Utilization of sine and cosine functions for cyclical encoding of days, weeks, months, and seasons.

### 10. Long Short-Term Memory (LSTM) Modeling
- Implementation of LSTM neural network for time series prediction.
- Training and evaluation of the model using 365 previous days to predict the next day.

### Conclusion
The project concludes by comparing the performance of different models. The LSTM model is identified as the most effective for this dataset, capturing the strong seasonal component in temperature variations. However, Prophet is acknowledged as a resource-efficient alternative in scenarios with limited computational resources.


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
