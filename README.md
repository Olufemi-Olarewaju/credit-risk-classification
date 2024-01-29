# Module 12 Report

## Overview of the Analysis

* The purpose of this challenge is to use supervised learning to build a model that can predict and identify the creditworthiness of future borrowers based on the known creditworthiness and information of past borrowers.
* The financial information provided by the dataset includes the following about the borrower and the loan:
  * Loan size: Size of the loan.
  * Interest rate: Interest rate of the loan.
  * Borrower income: Income of the borrower.
  * Debt-to-income: Ratio of how much the borrower owe vs the borrower's income.
  * Number of accounts: Number of loan and credit accounts.
  * Derogatory marks: Indicates borrower's failure to pay an outstanding debt.
  * Total debt: Total debt owed by the borrower.
  * Loan Status: Indicates if the loan is a healthy one or a risky one.

* The target outcome to be predicted is the `loan_status` column.

* The predictive model was built using the `LogisticRegression` model and the data was resampled using the `RandomOverSampler`module.

## Results

* Machine Learning Model 1:
  * The model is very good at predicting if a loan will be a healthy loan (`0`) because of the high precision score of 100%, recall score of 99% and f1 score of 100%. 
  The model is somewhat good at predicting if a loan will be a high-risk loan (`1`) because of its lower precision, recall and f1 scores when compared to the scores of a healthy loan prediction. This maybe because the model had way more label inputs for healthy loans (`0s`) than high-risk loans (`1s`).
  The original data had 30 times more label inputs for healthy loans (`0s`) than for high-risk loans (`1s`) as seen from the `label_input_ratio` variable.



* Machine Learning Model 2:
  * For the second model, the label input values had to be resampled so that the number of label input values for both the healthy loans (`0s`) and for the high-risk loans (`1s`) are equal.

  * The second model is very good at predicting the resampled data to detect a healthy loan (`0`) because of the high precision score of 100%, recall score of 99% and f1 score of 100%. The model became better at predicting a high-risk loan (`1`) because of its higher recall and f1 scores when compared to its recall and f1 scores produced by the first model.

## Summary

Both models seem to be very accurate at predicting most of the data points as they both had an accuracy score of 99%.

However, the second model seems to perform better because it had a `balanced_accuracy` of 99%, while the first model had a `balanced_accuracy` of 95% when comparing the actual target values to the predicted values produceed by the model. The second model is recommended because it predicts both outcomes correctly without being biased to the majority target value because both target values have been equalized.

