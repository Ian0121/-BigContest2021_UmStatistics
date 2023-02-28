## Abstract

This is the 1st prize in 2021 Big Contest Data Analysis ECO JEJU.
+ Aim
  + To make a prediction on the quantity of food waste that will be generated in Jeju for the months of July and August in 2021
  + Put forth various policies aimed at reducing the amount of food waste in Jeju
+ Team Name : UmStatistics
+ Team member : Kwon Namtaek, Oh Jungmin, Yu Gyeongmin, and Lee Sanghyun
+ Description : All members of our team hold degrees in Statistics from SungKyunKwan University. In the course of this project, we have utilized a diverse range of statistical and machine learning techniques including causal inference, spatial and time series data analysis, and Bayesian methods. Specifically, we have employed causal inference to establish a logical relationship between data analysis and policy-making.

## Overview
![index](https://user-images.githubusercontent.com/122112150/221743208-441cc824-2fef-4189-a1b0-c9611672974c.png)

## Preprocessing
1. Identifying missing data and outliers  

In certain cities, we encountered missing data that occurred 1) consecutively over multiple days, 2) in a recurring pattern, and 3) across several observation points. Additionally, we observed that this pattern of missing data was similar to that of the adjacent cities. Upon further investigation, we were able to trace the cause of this missing data to a news article, which reported that it was due to equipment replacement in Seogwipo-si and supply expansion in Jeju-si.

![preprocess](https://user-images.githubusercontent.com/122112150/221745455-dc70b284-a119-43f5-93c0-9de12b89b998.png)

2. Handling missing data and outliers

There were several techniques available to interpolate the missing data and outliers, including linear interpolation, spline interpolation, exponential smoothing, Kalman filtering, and others. However, instead of utilizing these techniques, we opted to estimate the pattern using harmonic regression based on the seasonality of a week, half a year, and a full year, and subsequently generated the data accordingly.


3. Identifying the relationship between different variables

We recognized that solely considering the correlation between different variables could potentially overlook their true relationship, especially given our understanding that a causal relationship must exist, given that the data were in the form of time series. As such, we took a two-pronged approach to identifying the causal mechanism between the variables.

Firstly, we utilized Bayesian network modeling to generate a graph that would help us identify the causal relationships between the variables. Secondly, we employed the Granger causality test to account for the time series nature of the data. By adjusting for potential confounding variables, we were able to accurately identify the true relationship between the variables.


4. Creating several derived variables

To account for seasonality within the data, we generated additional variables using sine and cosine functions. These variables were specifically designed to capture the cyclical patterns observed in the data over time, thereby enabling us to gain a better understanding of the seasonal effects on the variables of interest.

In addition, we also developed latitude and longitude variables to account for spatial data. These variables allowed us to incorporate the location-specific aspects of the data into our analysis, thereby providing a more nuanced understanding of the relationships between the variables.

Finally, we generated three new variables, namely 'emission before a year', 'emission before 35 days', and 'emission before 63 days', due to their high correlation with the current emission data. By incorporating data from these timeframes, we were able to gain a more comprehensive understanding of the underlying patterns and relationships within the data.

