## How to Perform EDA on Time Series Data

References-
1.https://towardsai.net/p/data-visualization/statistical-modeling-of-time-series-data-part-2-exploratory-data-analysis
2.https://blog.jovian.ai/time-series-analysis-data-exploration-and-visualization-9dbede5cbb8d

This repository Explains about how we can performed EDA on Time series data so that we can build models on this data.EDA on timeseries data require few more processing steps which are explained below-

## what is time series data?
A Time Series Data is simply a sequence of data in chronological order (i.e following the order of occurrence) which is used by businesses to analyze past data and make better decisions.

## Steps in Time series EDA-
#### 1.Understand the data
In EDA we try to understand our overall data by visualising and applying some stats on it
1.Read the data and merge different dataset and create a flat file.
2.check for missing values and fill those values with suitable values such as mean,mode,median or if missing values are less then drop the columns
3.Perform the feature engineering such as feature transformation,finding correlating,feature scaling etc.
4.Check distribution of data
#### 2.Data Decomposition (Additive and Multiplicative)
Data decomposition is the process of breaking the time series into 3 components: Trend, Seasonality, and Noise. Doing so gives us insights into repeating patterns in our data that could be used during model building. In python, the statsmodels library is used to do this decomposition. The library provides support for 2 types of decomposition: Additive and Multiplicative.
#### 3 Correlation Plots (Autocorrelation and Partial Autocorrelation Plot: ACF&PACF)
These are important plots for time series. They graphically summarize the strength of the relationships of observations in time series.In Autocorrelation, we calculate the correlation for time-series observations with previous time steps, called lags. Because the correlation of the time series observations is calculated with values of the same series at previous times, hence are called a serial correlation or an autocorrelation.
A partial autocorrelation is a summary of the relationship between an observation in a time series with observations at prior time steps with the relationships of intervening observations removed. Meaning… The effects of the lags in between are removed and we can see the direct impact a previous observation has on the value to be predicted at a time(t).PACF can be computed by regression.Regression is a statistical method to determine the strength and character of the relationship between one dependant value and other variables that are independent.
#### 4 Check data is stationary or not
1) Summary Statistics:
One of the most basic methods to check if our data is stationary is to the summary statistics. This is not much of an accurate way, sometimes the outcome of this test can be a statistical fluke.

2) Dickey-Fuller test:
Another method to check for stationarity in our data is statistical tests. I have used The Augmented Dickey-Fuller test which is called a unit root test. The null hypothesis of the test is that the time series can be represented by a unit root concluding our data as not stationary.

p-value > 0.05: Fail to reject the null hypothesis (H0), the data has a unit root and is non-stationary.
p-value <= 0.05: Reject the null hypothesis (H0), the data does not have a unit root and is stationary.
