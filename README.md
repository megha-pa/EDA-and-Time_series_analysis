## links
https://www.analyticsvidhya.com/blog/2021/10/a-comprehensive-guide-to-time-series-analysis/

#### This repository tells about how we can do EDA and perform forecasting on timeseries data.
## What is timeseries?
A time series is nothing but a sequence of various data points that occurred in a successive order for a given period of time.
## Components of Time Series Analysis
1.Trend: In which there is no fixed interval and any divergence within the given dataset is a continuous timeline. The trend would be Negative or Positive or Null Trend
2.Seasonality: In which regular or fixed interval shifts within the dataset in a continuous timeline. Would be bell curve or saw tooth
3.Cyclical: In which there is no fixed interval, uncertainty in movement and its pattern
4.Irregularity: Unexpected situations/events/scenarios and spikes in a short time span.
## What are the limitations of Time Series Analysis?
1.Time series has the below-mentioned limitations, we have to take care of those during our analysis,
2.Similar to other models, the missing values are not supported by TSA
3.The data points must be linear in their relationship.
4.Data transformations are mandatory, so a little expensive.
5.Models mostly work on Uni-variate data.
## Data Types of Time Series
Let’s discuss the time series’ data types and their influence. While discussing TS data-types, there are two major types.
#### 1 Stationary: A dataset should follow the below thumb rules, without having Trend, Seasonality, Cyclical, and Irregularity component of time series
The MEAN value of them should be completely constant in the data during the analysis
The VARIANCE should be constant with respect to the time-frame
The COVARIANCE measures the relationship between two variables.
#### 2 Non- Stationary: This is just the opposite of Stationary.
Methods to check Stationarity 
During the TSA model preparation workflow, we must access if the given dataset is Stationary or NOT. Using Statistical and Plots test.
#### Statistical Test: There are two tests available to test if the dataset is Stationary or NOT.
1 Augmented Dickey-Fuller (ADF) Test or Unit Root Test: The ADF test is the most popular statistical test and with the following assumptions.
Null Hypothesis (H0): Series is non-stationary
Alternate Hypothesis (HA): Series is stationary
p-value >0.05 Fail to reject (H0)
p-value <= 0.05 Accept (H1)
2 Kwiatkowski–Phillips–Schmidt–Shin (KPSS): these tests are used for testing a NULL Hypothesis (HO), that will perceive the time-series, as stationary around a deterministic trend against the alternative of a unit root. Since TSA looking for Stationary Data for its further analysis, we have to make sure that the dataset should be stationary.
#### Converting Non- stationary into stationary
Let’s discuss quickly how to convert Non- stationary into stationary for effective time series modeling. There are two major methods available for this conversion.
1 Detrending: It involves removing the trend effects from the given dataset and showing only the differences in values from the trend. it always allows the cyclical patterns to be identified.
2 Differencing: This is a simple transformation of the series into a new time series, which we use to remove the series dependence on time and stabilize the mean of the time series, so trend and seasonality are reduced during this transformation.
Yt= Yt – Yt-1
Yt=Value with time
3 Transformation: This includes three different methods they are Power Transform, Square Root, and Log Transfer., most commonly used one is Log Transfer.
