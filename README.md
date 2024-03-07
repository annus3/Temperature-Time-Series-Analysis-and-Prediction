# Project Overview

## Temperature Time Series Analysis and Prediction


### Introduction
This project aims to analyze and predict minimum daily temperatures using various time series forecasting models, including ARIMA, Prophet, and LSTM, as well as a dataset spanning 10 years from 1/1/1981 to 31/12/1990. The dataset, loaded from 'daily_min_temp.csv,' undergoes comprehensive data cleaning, visualization, and modeling using statistical and machine learning techniques.


## Getting Started

To run this project, follow the steps below:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/annus3/Time-Series-Analysis-on-Daily-Minumum-Temperature
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
- The dataset is loaded, and initial exploratory data analysis is performed.
- Identification and handling of missing values.
- Parsing date information into day, week, month, and season.
- Basic statistics of the dataset are presented.
- Renaming columns for clarity.
- A function (get_season) is defined to map months to seasons.
- Additional columns for 'season' and other time-related features are created.

### 2. Data Visualization
- Seaborn and Matplotlib are used for visualizing temperature distribution and detecting outliers.
- Boxplot is employed to identify outliers based on average temperatures 'min_temp' across different time intervals (season, month, week, day, year).
- Removal of outliers where minimum temperature exceeds 20°C.
- Seasonal, monthly, weekly, daily, and yearly analysis of temperature variations.

### 3. Augmented Dickey-Fuller (ADF) Test
- ADF test is performed to check for stationarity in the time series.
- Time series data is plotted over time, and rolling mean/variance are calculated and visualized.

### 4. Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) Plot
- Examination of autocorrelation and partial autocorrelation functions/plots are generated to determine parameters (p ,d, and q) for ARIMA model.

### 5. Time Series Decomposition
- The time series is decomposed into trend, season, and error components using the seasonal decomposition of time series (STL) method.
- Autocorrelation of residuals is visualized.

### 6. Non-seasonal ARIMA Modeling
- Auto ARIMA is applied without seasonality to the training data.
- Model diagnostics are plotted.
- Root Mean Squared Error (RMSE) is calculated and used to evaluate the model on training and test sets.

### 7. Seasonal ARIMA Modeling
- Application of auto ARIMA model with seasonality.
- Comparative analysis with non-seasonal ARIMA.
- Model diagnostics, RMSE, and model summary are displayed.
- Model performance is evaluated on the test set.

### 8. Prophet Modeling
- Prophet, a forecasting tool, is used to predict 'min_temp' for time series prediction.
- The dataset is reformatted for Prophet, and the model is trained.
- Predictions are made on the test set, and RMSE is calculated.
- Comparison of results with ARIMA models.

### 9. Cyclical Encoding
- Days, weeks, months, and seasons are cyclically encoded using sine and cosine functions.

### 10. Long Short-Term Memory (LSTM) Modeling
- Long Short-Term Memory (LSTM) neural network is implemented for time series prediction.
- LSTM model architecture is defined and trained on the training set.
- Training and evaluation of the model is done based on 365 previous days to predict the next day.
- Data is prepared in sequences.
- Predictions are made for both the training and test sets, and RMSE is calculated.

## Conclusion
The project concludes by comparing the performance of different models. The code provides a thorough exploration of time series analysis, including data preprocessing, visualization, statistical testing, and modeling with various techniques. The LSTM model is identified as the best-performing model for this dataset, capturing the strong seasonal component in temperature variations. However, Prophet is considered a good alternative, especially in resource-limited scenarios.

