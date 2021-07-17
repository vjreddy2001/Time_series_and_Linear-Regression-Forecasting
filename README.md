# Time_series_and_Linear-Regression-Forecasting
# A Yen for the Future

![GettyImages](https://user-images.githubusercontent.com/83671629/126046952-5ae58654-ddc4-446c-8a79-27c88e69dc35.jpg)



## Background

The financial departments of large companies often have to make foreign currency transactions when doing international business, while hedge funds are also interested in anything that will provide an edge in predicting currency movements. Hence, both are always eager to gain a better understanding of the future direction and risk of various currencies. 

This tool tests the many time series model in order to predict future movements in the value of the Canadian dollar versus the Japanese yen.

The main area of focus is :

1. Time series forecasting
2. Linear regression modelling

- - -

### Files

[Time-Series Starter Notebook](time_series_analysis.ipynb)

[Linear Regression Starter Notebook](regression_analysis.ipynb)

[CAD/JPY Data CSV File](cad_jpy.csv)

- - -

### Time-Series Forecasting

In the notebook time_series_analysis.ipynb, you will find historical CAD-JPY exchange rate data to which time series analysis and modelling is applied to determine if there is any predictable behaviour.

You will find the following steps outlined in the time series starter notebook :

1. Plotting the Settle price to check for long or short-term patterns.
   
    * Long term trend shows that the value of Yen is going down. Short term trend shows some seasonal fluctuations.

2. Decomposition using a Hodrick-Prescott filter (decompose the settle price into trend and noise).
    
     *  There definitely is a pattern for both long term and short term. Long term the value of Yen is dropping. Short term there seems to be seasonal fluctuations.

3. Forecasting returns using an ARMA model.
    
    * The p-values are > 0.05, so this model is not a good fit.

4. Forecasting the exchange rate price using an ARIMA model.
    
    * The ARIMA model forecasts that the Yen value is droping in the fext five days by 0.08 Yen.

5. Forecasting volatility with GARCH.
   
    * As per the GARCH model, there is an increase in maket volatility for Yen in the near future.

Use the results of the completed time series analysis and modelling to answer the following questions:

1. Based on this time series analysis it is not the right time to buy Yen.

2. The ARMA modle predicts the returns of Yen, in this case it predicts that the returns are going down.
The ARIMA modle predicts that the price of Yen, in this case it predicts that the price is going down.
The GARCH modle predicts that the volatility of the market, in this case the GARCH model predicts that market volatility is high or is increasing. All three modle show that it is risky to invest in Yen at the given time.

3. In this model evaluation, ARMA and ARIMA models do not meet the p-value threshold (0.05). 
The GARCH model meets the p-value threshold. By tweaking the ARMA and ARIMA model to meet the threshold value of 0.05 they can be used. The GARCH model can definitely be used.

#### Linear Regression Forecasting

In the notebook regression_analysis.ipynb, you will find a Scikit-Learn linear regression model to predict CAD/JPY returns with *lagged* CAD/JPY futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

You will find the following steps outlined in the regression_analysis notebook:

1. Data preparation (creating returns and lagged returns, and splitting the data into training and testing data)
2. Fitting a linear regression model.
3. Making predictions using the testing data.
4. Out-of-sample performance.
5. In-sample performance.

Useing the results of the linear regression analysis and modelling the following can be concluded:

* The out-of-sample RMSE is lower than the in-sample RMSE. RMSE is typically lower for training data, but is higher in this case.

- - -
