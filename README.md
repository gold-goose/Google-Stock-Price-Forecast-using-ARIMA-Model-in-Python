# Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python

This time, I would like to simulate an ARIMA process in Python with the time series data of Adjusted closing price of Google Stock. The data is downloaded from yahoo finance in period range between 2004-2021.

1. Import related library and convert the data into pandas data frame

![textimage](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%201.png)


2. Plot the data, which is the adjusted closing price data and see the trend. As we can see the trend is quadratic, so that, we take the d value as 2.

![textimage](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%202.png)


3. Run the autocorrelation plot

![textimage](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%203.png)


4. Run the  Partial autocorrelation in Python to find out the value of p (AR) and q (MA). As both diagram shows that the line crossed the confidence interval (bluecolour-filled space) between line 2 and 3, we took p=2 and q=2


![textimage](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%204.png)


5. Run ARIMA process in Python with order 2,1,2  as we have obtained the p, d, and q value beforehand. We took the AR and MA variable that has p value < 5% as p d and 

![textimage5](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%205.png)
![textimage6](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%206.png)


6. Plot the residuals. As we can see, there is no trend and showing pure white noise

![text image](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%207.png)


7. Forecast the model. First we run only for the next period we got 2543.89688782 for the forecasted value, 12.95333698 for the standard deviation, and [2518.50881385, 2569.28496179] for the confidence interval

![textimage](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%208.png)


8. Run the forecasted model for the next 5 period

![textimage](https://github.com/altheanabila/Google-Stock-Price-Forecast-using-ARIMA-Model-in-Python/blob/main/pic%209.png)
