# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2 - Ames Housing Data and Kaggle Challenge


### Problem Statement

To predict the price of a house at sale by creating a regression model based on the Ames Housing Dataset from Kaggle.

Two datasets were provided (train.csv) and (test.csv)
We are tasked to create a regression model using the training data and predicting the price by usng the test data also a submission is needed on the Kaggle link.

### Summary

I've been hired by a group of real estate agents that needed help to properly assess the value of the houses in Ames, Iowa. They traditionally search the web and compare the prices manually on all websites however that was tedious and time consuming. 

They needed a faster way to predict the prices to be stay competitive within this real estate market. A presentation will be made to clearly explain the model's ability to predict the prices.


### Process

Columns that were dropped were 'Pool QC', 'Misc Feature', 'Alley', 'Fence', 'Fireplace Qu' as it has a high percentage of null values.

Columns that were also dropped are 'Id' and 'PID' as it does not contribute to the predicition of sale price. The columns that have missing values are given 0 for float/int data and 'na' for string data.

Categorical variables were converted to one-hot encoded columns using .get_dummies() this however is not a good way to encode it as it will get messy. In future I will avoid doing this.

The training data was split using scikit-learn train_test_split for cross-validation and it is scaled using the StandardScaler. However more can be done by log-ing it and exponentiate it to make the model better.

I tested the models with linear regression and lasso. Both gave similar results and minimal variation from one another.

|Model|Test R^2 Score | Test RMSE |
|---|---|---|---|
|Linear Regression | 0.9062 | 25,657 | 
|Lasso | 0.9056 | 25,740 |


### Conclusion

As mentioned above, certain tweaks and changes will be able to improve the model. Both Lasso and Linear Regression give similar percentage on the testing data with 90.6 and 90.5 percent respectively. Eg, dropping more columns that are not important can help with the prediction accuracy as well as to log the data or exponentiate it.

