# Prediction of Financial statements of American oil and gas companies

## Task
The task is to build a forecast for Revenue and Operating Income for each company.

### Technologies and methods
* Python with econometrics + AutoML(PyCaret)

### Baseline model
For the baseline model I'd like to take ARIMA. But we have to understand the stationarity of our time series. Hence, let's implement Augmented Dickey-Fuller test. Furthermore, we have to find p and q. I'd like to apply this test to COP.xlsx time series and find p and q, and such p and q I'd like to use in my baseline model (it's just my own assumption, further we will select parameteres individually for each company).

### Metric 
As we know, scale dependent metrics are not suitable for comparing different time series. Percentage Error Metrics solve this problem. They are scale independent and used to compare forecast performance between different time series. In our analysis we'll use MAPE. Why? Because the mean absolute percentage error (MAPE) is one of the most popular used error metrics in time series forecasting. It is calculated by taking the average (mean) of the absolute difference between actuals and predicted values divided by the actuals. MAPE’s advantages are it’s scale-independency and easy interpretability.

### Additional data (macro)
For macrodata features I'd like to use:
* Crude Oil Production
* Natural Gas Liquids Production
* Petroleum Products Supplied
* Petroleum Stock Change

### AutoML
Multiple Time Series Forecasting with PyCaret
