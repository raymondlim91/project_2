# Project 2: Predicting sales prices with the Ames,Iowa Housing dataset

### Problem Statement
As real estate analysts in Iowa, we are responsible for managing our organization's real estate holdings.
By understanding the real estate market trends helps to minimize current and future real estate holding risks. The purpose of this analysis is to better understand a property price and provide suitable insights to management and potential buyers of the organization's real estate.<br>
Data analysis will be used on the Iowa real estate market data to determine the factors that affects property prices.

---

### Executive Summary

Ames is a city located in Iowa, United States. As of 2020, the population of Ames reaches 66,427 which makes it the ninth largest city of the states. ([*source*](https://en.wikipedia.org/wiki/Ames,_Iowa)). Over the past 10 years, the Ames home prices has appreciate by 28%. As compared to median housing prices over a decades for all markets was 18%. ([*source*](https://www.littlebighomes.com/real-estate-ames.html)).

There are different factors that will affect the sales price of a house within the same neighborhood. The factors that generally viewed as important includes the number of rooms, especially bedrooms, condition of the kichen. The year built and physical condition of the house are equally important. This project aims to examine how features of the house will affect the SalesPrice. The approach machine learning tools used to analyse the dataset will be ordinary least squares, Ridge and Lasso regression models. 

---

### Conclusions and Recommendations

In conclusion, Ridge regression model is the preferred model out of three prediction models used. The ridge model has a 0.8895 R2 score, shows that the model explains 88.95% of the variability of the response data round its means. The model is more suitable to be used at the same district or city area due to property price are different depends on area. <br>
Lasso regression model has high score on test dataset, however the test score is lower. This could means that the model has overfitted the test dataframe which cause high variance to the model. Linear regression has the least score out of three models. <br>
New features such as housing age, total square feet, total bathroom has been explored to help reduce the noise to the models and improve the accuracy of the predictions.

Based on the model analysis, the features that affects the housing prices the most can be categories under: 
1. Age of the house
2. Area of the house
3. Quality of the house

Based on the 3 main features, the younger the house age, the higher the housing Sale price due to appreciation of housing price. The Saleprice also increase with larger house area. The age and area of houses are fixed and cannot be changed. Quality of the house is one of the features that can be manipulated. External quality and the Overall Quality of the house are some of the features under Quality categories that increase the housing Saleprice as compared to the house with the same area. 

Recommendation for houseowner to sell their house at higher price is to maintain the quality of the houses, such as overall quality, external quality, kitchen quality, etc. This helps to retain the value of the house so that the house can be sold at higher price in future. Remodel the house also played an important factor to increase the house sale price. 


### Model improvement recommendation

Effective/Weighted age of the property are the general practice in property market to measure the age of the property. The effective age is calculated by taking the percentage of the remodeling or modernization in relation to the whole. Additional data such as 'Percentage of remodelling' and 'area of remodelling' be used to calculate the weighted age of the property, which could help the model to predict property sales price better. 

---

### Data

* [`train.csv`](./datasets/train.csv): Train dataset
* [`train_cleaned.csv`](./datasets/train_cleaned.csv): Cleaned Train dataset
* [`train_processed.csv`](./datasets/train_processed.csv): Preprocessed Train dataset
* [`test.csv`](./datasets/test.csv): Test dataset
* [`test_cleaned.csv`](./datasets/test_cleaned.csv): Cleaned Train dataset
* [`test_processed.csv`](./datasets/test_processed.csv): Preprocessed Test dataset
* [`lasso_sub.csv`](./datasets/lasso_sub.csv): Lasso Regression Model Kaggle submission
* [`ridge_sub.csv`](./datasets/ridge_sub.csv): Ridge Regression Model Kaggle submission
* [`linear_sub.csv`](./datasets/lasso_sub.csv): Lasso Regression Model Kaggle submission<rb>

---
### Data dictionary

Original data dictionary for train and test dataset can be found from attached link: <br>
https://www.kaggle.com/c/dsi-us-11-project-2-regression-challenge/data

Data dictonary for new features added: 

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**'house_age'**|*integer*|train_processed.csv|Age of the house| 
|**remod/add_year**|*integer*|train_processed.csv|Age of the house afer remodeling| 
|**age_remod**|*integer*|train_processed.csv|Years between house remodded and built|
|**total_sf**|*integer*|train_processed.csv|Total surface area of the house include basement, 1st floor, and 2nd floor|
|**total_bath**|*integer*|train_processed.csv|Number of total bathroom|
|**total_porch**|*integer*|train_processed.csv|Total porch surface area|

---
    
### Kaggle Submission score


![Kaggle submission](kaggle_submission_score.JPG)