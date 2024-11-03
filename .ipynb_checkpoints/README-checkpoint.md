# CreditRiskClassification

This project involves using various techniques to train and evaluate a supervised learning model based on loan risk. This model can identify the credit worthiness of borrowers from a dataset of historical lending activity from a peer-to-peer lending services company.

#Original code sources: Data Analytics course Module 20 Challenge files. Data Analytics course instructor, Andrew Hoang's, speed run Zoom recording for Module 20 Challenge.

#Code for the model can be found in credit_risk_classification.ipynb

#Data source file is lending_data.csv in Resources folder

## Overview of the Analysis

* The purpose of this analysis is to use historical data of lending activity to create a supervised learning model based on loan risk that can identify and predict the credit worthiness of borrowers (healthy loan OR high-risk loan).
* The financial information included in the data was loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts,	derogatory_marks, and total_debt
* The data was first designated with the target as a labels set (y) from the "loan_status" column. A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
* The remainder of the data was then designated as the features (X) in a DataFrame
* Data was then split into training and testing datasets using test_train_split
* A Logistic Regression Model was then created with the original data. Model was first fit usin gthe training data (X_train, y_train). Predictions were then saved for the testing data labels by using the testing feature data (X_test) and the fitted model
* The model's performance was then evaluated by creating a confusion matrix and printing a classification report.

## Results

* Machine Learning Model scores:
    * Overall Accuracy: 99%
    * Healthy Loan (0) Precision: 100%
    * High-Risk Loan (1) Precision: 84%
    * Healthy Loan (0) Recall: 99%
    * High-Risk Loan (1) Recall: 94%

## Summary

This logistic regression model predicts healthy loan and high-risk loan labels with high certainty (99% accuracy). Precision for the healthy loan label (0) is 1.00, meaning the model predicted correctly 100%. Precision for the high-risk loan label (1) is 0.84, meaning the model predicted correctly only 84% of the time for high-risk loans. Overall, the model performance is reliable and can predict high-risk loans with a good level of certainty. I can recommend this model for use by the company, with the understanding that it won't be able to predict high-risk loans about 16% of the time.
