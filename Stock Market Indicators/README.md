# Lead–Lag Analysis: Google Search Trends vs MTN Stock Price Overview

This analysis tests whether Google Search Trends act as a leading, lagging, or coincident indicator for MTN Ltd's (MTN.JO) stock price.
Using time-series alignment and cross-correlation, we assess whether changes in search interest influence short-term stock movements.

## Objectives
* Determine if search trends lead or lag stock price movements.
* Compare normalised time-series for pattern alignment.
* Quantify relationships using the cross-correlation function (CCF).
* Assess predictive relationships using statistical lead-lag tests and machine learning models.

## Data
* MTN Daily Prices — Yahoo Finance (via `yfinance` library)
* Google Trends — keyword search interest (via `pytrends` library)

## Processing
* Normalisation (MinMaxScaler, StandardScaler)
* Date Alignment
* Missing Value Handling

## Analysis
* Time-series visualisation and stationarity testing (ADF test)
* Cross-correlation at various lags (CCF)
* Granger Causality tests
* Vector Autoregression (VAR) modeling
* Machine Learning models (e.g., KNN, RF and XGBoost) for prediction

## Tools
* Python (pandas, numpy, matplotlib, seaborn, scikit-learn, statsmodels, pytrends, yfinance)

## Key Visualisations
### Visualisation 1
Caption: MTN.JO Share Price with Moving Averages
<img src="images/download (1).png" width="700">

### Visualisation 2
Caption: Performing STL decomposition for MTN.JO Share Price
<img src="images/download (2).png" width="700">

### Visualisation 3

Caption: Normalised MTN.JO

<img src="images/download (3).png" width="700">

### Visualisation 4
Caption: Performing STL decomposition for: mtn stock price: (South Africa)
<img src="images/download (4).png" width="700">

### Visualisation 5
Caption: Correlation Heatmap with Google Search Keywords
<img src="images/download (5).png" width="700">

### Visualisation 6
Caption: Cross-Correlation: mtn stock price (google trend search keyword)  vs Stock Price
<img src="images/download (6).png" width="700">

### Visualisation 7
Caption: ML Model Forecasts vs Actual Stock Price Movements
<img src="images/download (7).png" width="700">

## Key Findings
* Google Search Trends (particularly certain keywords) showed a leading relationship with MTN stock price movements, with p-values from Granger Causality tests indicating predictive power at various lags.

* ADF stationarity tests confirmed that both the stock price and Google Trends series, or their differenced forms, were stationary, a prerequisite for time-series analysis.

* Not all keywords showed strong predictive signals; the relationship varied by search term and lag duration.

* Machine learning models were employed to assess predictive relationships, leveraging lagged features of both stock prices and search trends.

* The analysis suggests exploratory predictive value of search trends, demonstrating their potential as indicators rather than standalone forecasting tools.

