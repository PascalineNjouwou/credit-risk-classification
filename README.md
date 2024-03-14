# Module 12 Report

## Overview of the Analysis

* Purpose of the analysis.

The purpose of this analysis was to develop and evaluate a machine learning model capable of predicting the risk associated with loans. By using logistic regression, a method well-suited for binary classification problems, we aimed to classify loans into two categories: low-risk (healthy) loans and high-risk loans. This classification helps in identifying potentially defaulting loans before approving them, thereby reducing financial risks and losses. The model was trained and tested on historical lending data, which included various features such as loan amount, term, interest rates, borrower's income, and credit history.


* Financial information and Predictions Goal:

The data was focused on loan applications and included various financial and personal information about the applicants. Variables likely encompassed loan amounts, the	interest rate,	borrower income	debt to income rate, the number of accounts, the derogatory marks, the	total debt, and the	loan status.
The primary objective was to predict whether a loan would be low-risk ("Healthy") or high-risk ("High-risk Loan"), essentially determining the likelihood of the borrower defaulting on the loan.


* Variables Predicted:

The variables predicted was 'loan_status', categorized into two classes:

Low-risk Loan: Loans that are expected to be repaid without issues.
High-risk Loan: Loans that have a high likelihood of default.

value_counts for loan_status would provide the distribution of these classes, indicating how many loans were classified as low risk vs. high risk in the dataset. This is crucial for understanding the balance of classes and potentially adjusting the modeling approach for imbalanced data.

* Stages of the Machine Learning Process:
The stages involved in this analysis included:

-> Data Preparation: Loading the data, exploring its structure, and preprocessing it (e.g., handling missing values, encoding categorical variables).

-> Feature Selection: Choosing relevant features that could potentially influence the loan's risk status.

-> Model Training: Using the train_test_split method to divide the data into training and test sets, then applying logistic regression to train the model on the training set.

-> Model Evaluation: Predicting loan risk on the test set and evaluating the model's performance using metrics like accuracy, precision, recall, and the F1-score.



* Methods Used:
The primary algorithm used was LogisticRegression from Scikit-learn, a popular choice for binary classification problems due to its simplicity and effectiveness in cases where the relationship between the independent variables and the dependent binary variable is logistic in nature.


## Results

* Machine Learning Model 1: Logistic Regression
-> Accuracy: 99% - The model correctly predicted the loan status 99% of the time.

-> Precision for Low-risk Loan: 100% - When the model predicted a loan as low-risk, it was correct every time.

-> Recall for Low-risk Loan: 99% - The model identified 99% of all actual low-risk loans.

-> Precision for High-risk Loan: 85% - When the model predicted a loan as high-risk, it was correct 85% of the time.

-> Recall for High-risk Loan: 91% - The model identified 91% of all actual high-risk loans



## Summary

Based on the provided classification report, the logistic regression model shows exceptional performance in predicting both low-risk and high-risk loans. The key points to consider are:

The model's high accuracy (99%) demonstrates its overall effectiveness in classifying loans.
The precision and recall for low-risk loans are nearly perfect, indicating strong performance in identifying safe loans.
For high-risk loans, while precision is slightly lower (85%), recall is high (91%), suggesting the model is quite capable of identifying most high-risk loans, albeit with some false positives.
Given the importance of both identifying high-risk loans (to minimize financial losses) and correctly approving low-risk loans (to maintain profitability), this model strikes a commendable balance. Therefore, I recommend the logistic regression model for use by the company in its loan approval process. Its high precision and recall for both classes make it a valuable tool for reducing risk and ensuring healthy lending practices.

Performance does depend on the problem we are trying to solve. 
If minimizing false negatives (failing to identify high-risk loans) is more critical, the model's high recall for high-risk loans is beneficial. 
Conversely, if minimizing false positives (incorrectly classifying loans as high risk) is more important, the model's precision, especially for low-risk loans, meets this need effectively.
