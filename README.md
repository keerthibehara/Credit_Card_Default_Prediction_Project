# Credit Card Default Prediction
<p align="center"> 
  <img src="![image](https://user-images.githubusercontent.com/99960098/172370131-40dc47b2-8d80-4ed5-a455-07b4e5fb46f8.png)" alt="Email Logo.png" width="80px" height="80px">
</p>
## Overview
This project is aimed at predicting the case of customers default payments in Taiwan.
From the perspective of risk management, the result of predictive accuracy of the
estimated probability of default will be more valuable than the binary result of
classification - credible or not credible clients. The main objective is to build a
predictive model, which could help them in predicting the customers who might
default in upcoming months.From the perspective of risk management, understanding the customer characteristics that lead to this outcome can aid creditors in deciding reasonable credit limits to prevent this.

Credit card default happens when you have become severely delinquent on your
credit card payments. Missing credit card payments once or twice does not count as
a default. A payment default occurs when you fail to pay the Minimum Amount Due
on the credit card for a few consecutive months.

## Data Understanding
The dataset contains 30000 rows and 25 columns. This project employed a binary
variable, default payment (Yes = 1, No = 0), as the response variable. After reviewing
the literature and the 23 variables are taken as explanatory variables.
![image](https://user-images.githubusercontent.com/99960098/172366978-0a6e26ee-bb3e-4f42-80f9-0f6fca9b45d2.png)
The dataset had a class imbalance where only 22% of the customers defaulted on their payment.

## Dataset
![image](https://user-images.githubusercontent.com/99960098/172367323-f54935b2-694b-4026-96f6-23d51dc6ba11.png)
The measurement scale for the repayment status is:

    -1 = pay duly
    1 = payment delay for one month
    2 = payment delay for two months
    [...]
    8 = payment delay for eight months
    9 = payment delay for nine months and above
    
## Models Used and Result
This is a binary classification problem where the target variable is whether or not a client will default on their payment (Yes = 1, No = 0). After cleaning the data, handling class imbalance using SMOTE and feature engineering, several baseline models were fit to the training data. Baselines included Logistic Regression, Random Forest Classifier, XGBoost Classifier, Gradient Boost Classifier, K Nearest Neighbors, Support Vector Machines, Naïve Bayes Classifier and Decision Tree Classifier. Each model iteration's hyperparameters were tuned with GridSearchCV and RandomSearchCV. Predictions were evaluated using the ROC_AUC Score.

The final XG Boost model achieved an ROC_AUC score of 0.867.
![image](https://user-images.githubusercontent.com/99960098/172368442-06afb068-1c7c-4713-be11-0965128a81f6.png)

