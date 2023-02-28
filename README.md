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
