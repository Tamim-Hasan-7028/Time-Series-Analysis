<h1 align="center"><b><u>Time Series Analysis</u></b></h1>

<p>
Predictive analysis are 2 types.
 
1. Non time series prediction
(KNN, Linear regression, Decision Tree etc). <br>
2. Time series prediction
(ARIMA, SARIMA, GARCH etc).

<b>Time series has only 1 variable with its different time series.</b>

<h3 align="center"><b><u>Time series Decomposition:</u></b></h3>

If we decompose a time series plot we will find 4 components:<br>
1. Trend<br>
2. Seasonality<br>
3. Cyclic variation<br>
4. Irregularity

<h3 align="center"><b><u>General approach to time series modeling:</u></b></h3>

1. Plot series & check if  there is trend, seasonality, irregularity components or not.<br>
2. If there is, then remove those components to achieve stationary.<br>
3. Choose a model<br>
4. Forecast<br>

<h3 align="center"><b><u>Stationarity:</u></b></h3>
Properties:

1. Mean needs to be constant.<br>
2. Std needs to be constant.<br>
3. No seasonality.<br>

<h3 align="center"><b><u>Checking Stationarity:</u></b></h3>

There is 2 way:

1. Rolling mean & std method (visualization method)<br>
2. ADFuller test:

    The null and alternative hypotheses for the ADF Test are defined as:
   
     <b>Null hypothesis:</b> The Time Series is non-stationary<br>
     <b>Alternative hypothesis:</b> The Time Series is stationary


<h3 align="center"><b><u>Making Stationarity:</u></b></h3>
 
There are several ways. Most common are:

 1. Time shift difference (removing trend)
 2. log transformation
 3. Taking sqrt or cube
 4.  Combinations of above

<h3 align="center"><b><u>Model Selection:</u></b></h3>

<b>ARIMA (Autoregressive Integrated Moving Average):</b>

Use Cases: Best for data where the time series is stationary after differencing and no seasonal patterns exist. Suitable for forecasting stock prices, sales forecasting, economic data, etc.

Key Features: Integrates differencing (to make data stationary), autoregression (relationship between an observation and a number of lagged observations), and moving average (dependency between an observation and a residual error from a moving average model applied to lagged observations).

<br>
<br>

<b>SARIMA (Seasonal ARIMA):</b>

Use Cases: Ideal for handling seasonal variations in data, such as monthly sales data with a clear seasonal pattern, electricity demand, seasonal weather data, etc.

Key Features: Extends ARIMA by adding seasonal terms, which accounts for seasonality (repeating trends) in time series data.

<br>
<br>

<b>ETS (Error, Trend, Seasonality):</b>

Use Cases: Useful when the data exhibits clear trend and/or seasonal patterns. It's particularly effective with forecasting tasks where these components are prominent, like retail sales through the year.

Key Features: Models the data with exponential smoothing to handle trend and seasonality, which can adaptively estimate the level, trend, and seasonal components.

<br>
<br>

<b>Prophet:</b>

Use Cases: Developed by Facebook for forecasting time series data that has strong seasonal patterns with large numbers of missing values or large outliers, such as website traffic, yearly and weekly seasonality of queries.

Key Features: It is robust to missing data and shifts in the trend, and typically handles outliers well.

<br>
<br>

<b>VAR (Vector Autoregression):</b>

Use Cases: Suitable for multivariate time series data where the variable of interest is influenced by other variables. Commonly used in econometrics, for example, to forecast interconnected economic variables like GDP, inflation, and employment.

Key Features: Each variable is a linear function of past lags of itself and past lags of other variables, making it powerful for capturing the linear interdependencies among multiple time series.

<br>
<br>

<b>GARCH (Generalized Autoregressive Conditional Heteroskedasticity):</b>

Use Cases: Primarily used in financial markets to model the volatility (variance) of returns or prices, such as stocks or foreign exchange.

Key Features: Focuses on modeling the conditional variance based on past variances, capturing time-varying volatility which is typical in financial time series.

<br>
<br>

<b>Machine Learning Models:</b>

Use Cases: When the relationship between the input and output variables is nonlinear, complex, or involves interactions between a large number of features. Examples include using RandomForest or Neural Networks for predicting demand or sales based on multiple input features.

Key Features: Can incorporate a wide variety of inputs (lags, other time series, external variables) and can capture complex nonlinear relationships.

<h3 align="center"><b><u>Model Evaluation:</u></b></h3>

1. MSE
2. RMSE
3. AIC
4. BIC
5. MAPE

Lowest value means good model.</p>

<h3 align="center"><b><u>Thank you</u></b></h3>
