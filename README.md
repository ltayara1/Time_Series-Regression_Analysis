# Time-Series-Homework

### Background
This project uses the many time-series tools (Hodrick-Prescott Filter, ARMA model, GARCH model, linear regression, etc.) to predict future movements in the value of the Japanese yen versus the U.S. dollar.

## Time Series Analysis
I started out by loading historical Dollar-Yen exchange rate and applied time series analysis and modeling to determine whether there is any predictable behavior. I performed a decomposition using a Hodrick-Prescott Filter to divide the "settle" price into trend and noise. I forecasted returns using and the "settle" Price using an ARIMA Model. Last, I forecasted volatility with a GARCH model.

Based on this time series analysis, I would not buy the yen yet because the ARMA model shows stationary values rather than an increase in value. By the highly positive AIC and BIC we can also see that that this is not a good time to buy. We can also tell that the the risk is going to increase.

Based on the model evaluation, I would not feel confident in using these models for trading, because the p-values showed that the data was not a good fit. I would not want to risk my money with that much of an increase in volatility.

## Regression Analysis
In this notebook, I built a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with lagged Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

I started out by creating Returns and Lagged Returns and splitting the data into training and testing data. Next, I fit a Linear Regression Model.
Making predictions using the testing data using Out-of-sample and In-sample performance.

The out-of-sample RMSE is lower than the in-sample RMSE, although, it should be lower for training data. It fits better for the out-of sample than in-sample.
