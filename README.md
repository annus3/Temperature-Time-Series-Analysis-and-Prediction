# Project Overview

## Temperature Time Series Analysis and Prediction


### Introduction
This project aims to analyze and predict minimum daily temperatures using various time series forecasting models, including ARIMA, Prophet, and LSTM, as well as a dataset spanning 10 years from 1/1/1981 to 31/12/1990. The dataset, loaded from 'daily_min_temp.csv,' undergoes comprehensive data cleaning, visualization, and modeling using statistical and machine learning techniques.


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
   python temp_TimeSeries_script.ipynb
   ```

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

