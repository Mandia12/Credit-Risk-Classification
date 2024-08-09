# Credit-Risk-Classification

## Overview of the Analysis

The purpose of this analysis is to evaluate the performance of a logistic regression model developed for predicting credit risk. The model aims to classify loans as either "healthy" (0) or "high-risk" (1) based on a variety of financial indicators. This classification is crucial for lenders to make informed decisions regarding loan approvals and risk management.

The dataset contains financial information on various borrowers, including:

* Loan Size: The amount of the loan.
* Interest Rate: The interest rate applied to the loan.
* Borrower Income: The annual income of the borrower.
* Debt-to-Income Ratio: The ratio of the borrower’s total monthly debt payments to their gross monthly income.
* Number of Accounts: The number of financial accounts the borrower holds.
* Derogatory Marks: Negative marks on the borrower’s credit report.
* Total Debt: The total amount of debt the borrower has.

The target variable, loan_status, is binary, with values of 0 indicating a healthy loan and 1 indicating a high-risk loan.

The machine learning process involved the following stages:

1. Feature Selection: The relevant financial indicators were selected as input features (X-values) for the model.
2. Model Development: A logistic regression model was implemented to predict the loan status.
3. Model Evaluation: The model's performance was evaluated using a confusion matrix, from which key metrics like accuracy, precision, recall, and the F1 score were calculated.

## Results

The results of the logistic regression model are summarized below:

* Accuracy: 99.18%
* Precision:
> * Class 0 (Healthy Loans): 1.00
> * Class 1 (High-Risk Loans): 0.85
* Recall:
> * Class 0 (Healthy Loans): 0.99
> * Class 1 (High-Risk Loans): 0.91
* F1 Score:
> * Class 0 (Healthy Loans): 1.00
> * Class 1 (High-Risk Loans): 0.88
* Specificity: 99.46%
* Macro Avg:
> * Precision: 0.92
> * Recall: 0.95
> * F1 Score: 0.94
* Weighted Avg:
> * Precision: 0.99
> * Recall: 0.99
> * F1 Score: 0.99

## Summary

The logistic regression model exhibits high overall accuracy (99.18%), driven largely by its effectiveness in identifying healthy loans (Class 0). The model demonstrates perfect precision (1.00) and nearly perfect recall (0.99) for healthy loans, indicating it is highly reliable in predicting the majority class.

For high-risk loans (Class 1), the model achieves a recall of 0.91, meaning it correctly identifies 91% of the high-risk loans. However, the precision for this class is 0.85, indicating that some loans predicted as high-risk are actually healthy, leading to false positives. The F1 score for high-risk loans is 0.88, reflecting a balanced consideration of precision and recall.

Given the context of credit risk, where identifying high-risk loans is crucial to minimizing potential financial losses, the model's high recall for high-risk loans is a valuable asset. However, the trade-off between precision and recall suggests that the model may be too conservative, leading to more false positives than desired.

The model is recommended for deployment in scenarios where the priority is to avoid missing high-risk loans, even at the cost of some false positives. However, if the goal is to balance between minimizing false positives and accurately identifying high-risk loans, further tuning of the model or exploring alternative algorithms could be beneficial.

Overall, the logistic regression model provides strong performance and is suitable for use in credit risk classification, particularly where high recall is a key priority.