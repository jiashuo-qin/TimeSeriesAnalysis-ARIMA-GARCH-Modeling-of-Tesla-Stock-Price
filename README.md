# TimeSeriesAnalysis-ARIMA-GARCH-Modeling-of-Tesla-Stock-Price
In this problem, we are going to analyze the Tesla stock price data from 2011 through the end of July 2021. We will use the ARIMA-GARCH to model daily and weekly stock price (adjusted close price at the end of a day for daily data or at the end of the week for weekly data), with a focus on the behavior of its volatility as well as forecasting both the price and the volatility
Individual stock prices tend to exhibit high amounts of non-constant variance, and thus ARIMA models built upon that data would likely exhibit non-constant variance in residuals. In this problem, we are going to analyze the Tesla stock price data from 2011 through the end of July 2021. We will use the ARIMA-GARCH to model daily and weekly stock price (adjusted close price at the end of a day for daily data or at the end of the week for weekly data), with a focus on the behavior of its volatility as well as forecasting both the price and the volatility. The files for the Tesla stock price data are provided below:
Daily TSLA Price Download Daily TSLA Price
Weekly TSLA Price Download Weekly TSLA Price

Question 1: Exploratory Data Analysis (20 points)
1a. Based on your intuition, when would you use daily vs weekly stock price data?
1b. Plot the time series plots comparing daily vs weekly data. How do the daily vs weekly time series data compare?
1c. Fit a non-parametric trend using splines regression to both the daily and weekly time-series data. Overlay the fitted trends. How do the trends compare?
1d. Consider the return stock price computed as follows:
                            
Apply this formula to compute the return price based on the daily and weekly time-series data. Plot the return time series and their corresponding ACF plots. How do the return time series compare in terms of stationarity and serial dependence?

Question 2: ARIMA(p,d,q) for Stock Price (20 Points)

2a. Divide the (original) stock price data into training and testing data set, where the training data exclude the last week of data (July 26th-July 30th) with the testing data including the last week of data. Apply the iterative model to fit an ARIMA(p,d,q) model with max AR and MA orders of 8 and difference orders 1 and 2 separately to the training datasets of the daily and weekly data. Display the summary of the final model fit.

2b. Evaluate the model residuals and squared residuals using the ACF and PACF plots as well as hypothesis testing for serial correlation. What would you conclude based on this analysis?

2c. Apply the model identified in (2a) and forecast the last week of data. Plot the predicted data to compare the predicted values to the actual observed ones. Include 95% confidence intervals for the forecasts in the corresponding plots.

2d. Calculate Mean Absolute Percentage Error (MAPE) and Precision Measure (PM). How many observations are within the prediction bands?  Compare the accuracy of the predictions for the daily and weekly time series using these two measures. 

Question 3: ARMA(p,q)-GARCH(m,n) for Return Stock Price (20 Points)

3a. Divide the return data into training and testing data set, where the training data exclude the last week of data (July 26th-July 30th) with the testing data including the last week of data. Apply the iterative model to fit an ARMA(p,q)-GARCH(m,n) model by selecting the orders for p & q up to 5 and orders for m & n up to 2.  Display the summary of the final model fit. Write up the equation of the estimated model.

3b. Evaluate the model residuals and squared residuals using the ACF and PACF plots as well as hypothesis testing for serial correlation. What would you conclude based on this analysis?

3c. Apply the model identified in (3a) and forecast the mean and the variance of the last week of data. Plot the predicted data to compare the predicted values to the actual observed ones. Include 95% confidence intervals for the forecasts in the corresponding plots. Interpret the results, particularly comparing forecast using daily versus weekly data.

3d. Calculate Mean Absolute Percentage Error (MAPE) and Precision Measure (PM) for the mean forecasts.  Compare the accuracy of the predictions for the daily and weekly time series using these two measures. Compare the accuracy of the forecasts with those obtained in (2d). Interpret the results.

Question 4: Reflection on the Modeling and Forecasting (10 points) 

Based on the analysis above, discuss the application of ARIMA on the stock price versus the application of ARMA-GARCH on the stock return. How do the models fit the data? How well do the models predict?  How do the models perform when using daily versus weekly data? Would you use one approach over another for different settings? What are some specific points of caution one would need to consider when applying those models?
