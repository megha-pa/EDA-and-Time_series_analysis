#Links
#This repository tells about how we can do EDA and perform forecasting on timeseries data.
##What is timeseries?
A time series is nothing but a sequence of various data points that occurred in a successive order for a given period of time.
##Components of Time Series Analysis
Trend: In which there is no fixed interval and any divergence within the given dataset is a continuous timeline. The trend would be Negative or Positive or Null Trend
Seasonality: In which regular or fixed interval shifts within the dataset in a continuous timeline. Would be bell curve or saw tooth
Cyclical: In which there is no fixed interval, uncertainty in movement and its pattern
Irregularity: Unexpected situations/events/scenarios and spikes in a short time span.
##What are the limitations of Time Series Analysis?
Time series has the below-mentioned limitations, we have to take care of those during our analysis,
Similar to other models, the missing values are not supported by TSA
The data points must be linear in their relationship.
Data transformations are mandatory, so a little expensive.
Models mostly work on Uni-variate data.
Data Types of Time Series
Let’s discuss the time series’ data types and their influence. While discussing TS data-types, there are two major types.
Stationary
Non- Stationary
6.1 Stationary: A dataset should follow the below thumb rules, without having Trend, Seasonality, Cyclical, and Irregularity component of time series
The MEAN value of them should be completely constant in the data during the analysis
The VARIANCE should be constant with respect to the time-frame
The COVARIANCE measures the relationship between two variables.
6.2 Non- Stationary: This is just the opposite of Stationary.
Methods to check Stationarity 
During the TSA model preparation workflow, we must access if the given dataset is Stationary or NOT. Using Statistical and Plots test.
7.1 Statistical Test: There are two tests available to test if the dataset is Stationary or NOT.
Augmented Dickey-Fuller (ADF) Test
Kwiatkowski-Phillips-Schmidt-Shin (KPSS) Test
7.1.1 Augmented Dickey-Fuller (ADF) Test or Unit Root Test: The ADF test is the most popular statistical test and with the following assumptions.
Null Hypothesis (H0): Series is non-stationary
Alternate Hypothesis (HA): Series is stationary
p-value >0.05 Fail to reject (H0)
p-value <= 0.05 Accept (H1)
7.1.2 Kwiatkowski–Phillips–Schmidt–Shin (KPSS): these tests are used for testing a NULL Hypothesis (HO), that will perceive the time-series, as stationary around a deterministic trend against the alternative of a unit root. Since TSA looking for Stationary Data for its further analysis, we have to make sure that the dataset should be stationary.
####Converting Non- stationary into stationary
Let’s discuss quickly how to convert Non- stationary into stationary for effective time series modeling. There are two major methods available for this conversion.
Detrending
Differencing
Transformation
8.1 Detrending: It involves removing the trend effects from the given dataset and showing only the differences in values from the trend. it always allows the cyclical patterns to be identified.

Detrending Variable
8.2 Differencing: This is a simple transformation of the series into a new time series, which we use to remove the series dependence on time and stabilize the mean of the time series, so trend and seasonality are reduced during this transformation.
Yt= Yt – Yt-1
Yt=Value with time
Detrending and Differencing extractions
Detrending and Differencing
8.3 Transformation: This includes three different methods they are Power Transform, Square Root, and Log Transfer., most commonly used one is Log Transfer.
Moving Average Methodology
The commonly used time series method is Moving Average. This method is slick with random short-term variations. Relatively associated with the components of time series.
The Moving Average (MA) (Or) Rolling Mean: In which MA has calculated by taking averaging data of the time-series, within k periods.
Let’s see the types of moving averages:
Simple Moving Average (SMA),
Cumulative Moving Average (CMA)
Exponential Moving Average (EMA)
9.1 Simple Moving Average (SMA)
The SMA is the unweighted mean of the previous M or N points. The selection of sliding window data points, depending on the amount of smoothing is preferred since increasing the value of M or N, improves the smoothing at the expense of accuracy.
9.2 Cumulative Moving Average (CMA)
The CMA is the unweighted mean of past values, till the current time.
This article was published as a part of the Data Science Blogathon
time series image
This article was published as a part of the Data Science Blogathon
 

####Synopsis of Time Series Analysis
A Time-Series represents a series of time-based orders. It would be Years, Months, Weeks, Days, Horus, Minutes, and Seconds
A time series is an observation from the sequence of discrete-time of successive intervals.
A time series is a running chart.
The time variable/feature is the independent variable and supports the target variable to predict the results.
Time Series Analysis (TSA) is used in different fields for time-based predictions – like Weather Forecasting, Financial, Signal processing, Engineering domain – Control Systems, Communications Systems.
Since TSA involves producing the set of information in a particular sequence, it makes a distinct from spatial and other analyses.
Using AR, MA, ARMA, and ARIMA models, we could predict the future.
Introduction to Time Series Analysis
Time Series Analysis is the way of studying the characteristics of the response variable with respect to time, as the independent variable. To estimate the target variable in the name of predicting or forecasting, use the time variable as the point of reference. In this article we will discuss in detail TSA Objectives, Assumptions, Components (stationary, and Non- stationary). Along with the TSA algorithm and specific use cases in Python.

What is Time Series Analysis
Definition: If you see, there are many more definitions for TSA. But make it simple.
A time series is nothing but a sequence of various data points that occurred in a successive order for a given period of time
Objectives:
To understand how time series works, what factors are affecting a certain variable(s) at different points of time.
Time series analysis will provide the consequences and insights of features of the given dataset that changes over time.
Supporting to derive the predicting the future values of the time series variable.
Assumptions: There is one and the only assumption that is “stationary”, which means that the origin of time, does not affect the properties of the process under the statistical factor.
How to analyze Time Series?
Quick steps here for your reference, anyway. Will see this in detail in this article later.
Collecting the data and cleaning it
Preparing Visualization with respect to time vs key feature
Observing the stationarity of the series
Developing charts to understand its nature.
Model building – AR, MA, ARMA and ARIMA
Extracting insights from prediction
Significance of Time Series and its types
TSA is the backbone for prediction and forecasting analysis, specific to the time-based problem statements.
Analyzing the historical dataset and its patterns
Understanding and matching the current situation with patterns derived from the previous stage.
Understanding the factor or factors influencing certain variable(s) in different periods.

Components of Time Series Analysis
Trend
Seasonality
Cyclical
Irregularity
Trend: In which there is no fixed interval and any divergence within the given dataset is a continuous timeline. The trend would be Negative or Positive or Null Trend
Seasonality: In which regular or fixed interval shifts within the dataset in a continuous timeline. Would be bell curve or saw tooth
Cyclical: In which there is no fixed interval, uncertainty in movement and its pattern
Irregularity: Unexpected situations/events/scenarios and spikes in a short time span.
Components of Time Series Analysis
What are the limitations of Time Series Analysis?
Time series has the below-mentioned limitations, we have to take care of those during our analysis,
Similar to other models, the missing values are not supported by TSA
The data points must be linear in their relationship.
Data transformations are mandatory, so a little expensive.
Models mostly work on Uni-variate data.
Data Types of Time Series
Let’s discuss the time series’ data types and their influence. While discussing TS data-types, there are two major types.
Stationary
Non- Stationary
6.1 Stationary: A dataset should follow the below thumb rules, without having Trend, Seasonality, Cyclical, and Irregularity component of time series
The MEAN value of them should be completely constant in the data during the analysis
The VARIANCE should be constant with respect to the time-frame
The COVARIANCE measures the relationship between two variables.
6.2 Non- Stationary: This is just the opposite of Stationary.
Mean, Variance and Covariance of Time Series
Methods to check Stationarity 
During the TSA model preparation workflow, we must access if the given dataset is Stationary or NOT. Using Statistical and Plots test.
7.1 Statistical Test: There are two tests available to test if the dataset is Stationary or NOT.
Augmented Dickey-Fuller (ADF) Test
Kwiatkowski-Phillips-Schmidt-Shin (KPSS) Test
7.1.1 Augmented Dickey-Fuller (ADF) Test or Unit Root Test: The ADF test is the most popular statistical test and with the following assumptions.
Null Hypothesis (H0): Series is non-stationary
Alternate Hypothesis (HA): Series is stationary
p-value >0.05 Fail to reject (H0)
p-value <= 0.05 Accept (H1)
7.1.2 Kwiatkowski–Phillips–Schmidt–Shin (KPSS): these tests are used for testing a NULL Hypothesis (HO), that will perceive the time-series, as stationary around a deterministic trend against the alternative of a unit root. Since TSA looking for Stationary Data for its further analysis, we have to make sure that the dataset should be stationary.
Converting Non- stationary into stationary
Let’s discuss quickly how to convert Non- stationary into stationary for effective time series modeling. There are two major methods available for this conversion.
Detrending
Differencing
Transformation
8.1 Detrending: It involves removing the trend effects from the given dataset and showing only the differences in values from the trend. it always allows the cyclical patterns to be identified.

Detrending Variable
8.2 Differencing: This is a simple transformation of the series into a new time series, which we use to remove the series dependence on time and stabilize the mean of the time series, so trend and seasonality are reduced during this transformation.
Yt= Yt – Yt-1
Yt=Value with time
Detrending and Differencing extractions
Detrending and Differencing
8.3 Transformation: This includes three different methods they are Power Transform, Square Root, and Log Transfer., most commonly used one is Log Transfer.
Moving Average Methodology
The commonly used time series method is Moving Average. This method is slick with random short-term variations. Relatively associated with the components of time series.
The Moving Average (MA) (Or) Rolling Mean: In which MA has calculated by taking averaging data of the time-series, within k periods.
Let’s see the types of moving averages:
Simple Moving Average (SMA),
Cumulative Moving Average (CMA)
Exponential Moving Average (EMA)
9.1 Simple Moving Average (SMA)
The SMA is the unweighted mean of the previous M or N points. The selection of sliding window data points, depending on the amount of smoothing is preferred since increasing the value of M or N, improves the smoothing at the expense of accuracy.
Simple Moving Average
To understand better, will use the Air-Temperature.

import pandas as pd
from matplotlib import pyplot as plt
from statsmodels.graphics.tsaplots import plot_acf
df_temperature = pd.read_csv('temperature_TSA.csv', encoding='utf-8')
df_temperature.head()
Head of Dataframe
df_temperature.info()
Information of Data Frame

9.3 Exponential Moving Average (EMA)
EMA is mainly used to identify trends and to filter out noise. The weight of elements is decreased gradually over time. This means It gives weight to recent data points, not historical ones. Compared with SMA, the EMA is faster to change and more sensitive.
α –>Smoothing Factor.

It has a value between 0,1.
Represents the weighting applied to the very recent period.
Lets will apply the exponential moving averages with a smoothing factor of 0.1 and 0.3 in the given dataset.
 
