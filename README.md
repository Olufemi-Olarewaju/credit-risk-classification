# Module 12 Report

## Overview of the Analysis

* The purpose of challenge is to use supervised learning is to build a model that can predict and identify the creditworthiness of future borrowers based on the known creditworthiness and information of past borrowers.
* Explain what financial information the data was on, and what you needed to predict.
The financial information provided by the dataset includes the following about the borrower and the loan:
  * Loan size: Size of the loan.
  * Interest rate: Interest rate of the loan.
  * Borrower Income: Income of the borrower.
  * Debt-to-Income: Ratio of how much the borrower owe vs the borrower's income.
  * Number of accounts: Number of loan and credit accounts
  * Derogatory marks: Indicates borrower's failure to pay an outstanding debt.
  * Total debt: Total debt owed by the borrower.
  * Loan Status: Indicates of the loan is a healthy one or a risky one.

* The target was to predict the `loan_status`.

* The predictive model was built using the `LogisticRegression` model and the data was resampled using the `RandomOverSampler`module.

## Results

* Machine Learning Model 1:
  * The model is very good at predicting if a loan will be a healthy loan (`0`) because of the high precision score of 100%, recall score of 99% and f1 score of 100%. 
  The model is somewhat good at predicting if a loan will be a high-risk loan (`1`) because of its lower precision, recall and f1 scores when compared to the scores of a healthy loan prediction. This maybe because the model had way more label inputs for healthy loan (`0`) than high-risk (`1`) loan.
  The original data had 30 times more label inputs for healthy loans (`0s`) than for high-risk loans (`1s`) as seen from the `label_input_ratio` variable.



* Machine Learning Model 2:
  * For the second model, the label input values had to be resampled so that the number of label input values for both the healthy loans (`0s`) and for the high-risk loans (`1s`) are equal.

  * The second model is very good at predicting the resampled data to detect if a loan will be a healthy loan (`0`) because of the high precision score of 100%, recall score of 99% and f1 score of 100%. The model became better at predicting if a loan will be a high-risk loan (`1`) because of its higher recall and f1 scores when compared to its recall and f1 scores produced by the first model.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
