# ElectricityProductionTimeSeries

### Introduction

Time series analysis is a method for analyzing data in order to spot trends and predict what will happen in the future. I will carry out time series analysis and forecast of electricity production in United States. This project will provide a procedure to analyze and fit a time series model in R. The data comprises of units of electricity produced on monthly level. I've followed the Box-Jenkins approach in the project in order to fit an appropriate time series model.

### Methodology

I follow Box-Jenkins Models to tackle the time-series data and fit an appropriate model to the data. The Box-Jenkins Model comprises of six steps that needs to be followed.

1.  Stationarity
2.  Estimating Models
3.  Parameter Redundancy
4.  Parameter Estimation
5.  Residual Analysis
6.  Forecast

Step 1: Stationarity: To check if the data is stationary, if the data is stationary we can move to the next step, else we need to make the data stationary using Differencing, Detrending or Transformation. To check stationarity we perform Dicky Fuller Test.

Step 2: Estimating Models: We estimate the p and q values of ARIMA model, based on the ACF and PACF plots on the stationary data. We also use EACF plot to estimate the models.

Step 3: Parameter Redundancy: We work with all the estimated models. We fit the model to all the combinations of estimated p,d,q values.

Step 4: Parameter Estimation: Once we fit all the models, we compare the models and check the loglikelihood, AIC and BIC value. We select the model with lowest AIC and BIC values, and lower number of parameters. We can selected the model with slightly higher AIC or BIC, if it reduces the number of parameters in the model significantly.

Step 5: Residual Analysis: Based on the model that we find to be the best fit, we perform analysis on the residuals of the model. We plot the ACF plot to check if the residuals are uncorrelated. We check the normality of the residuals by plotting Q-Q plot, histogram and performing Shapiro-Wilk Test. We perform Ljung-Box Test to know if the residual is white noise or not.

Step 6: Forecast: The final step of Time Series Analysis, is to forecast data for the future. We fit the best model we found above on the original data and forecast the future values.

### Conclusion

We can see that SARIMA(1,1,1)x(2,1,1)[12] is a great fit to the data, and is able to forecast the Electricity Production by capturing the seasonality trends.
