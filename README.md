# credit-risk-classification

# Module 12 Report Template

## Overview of the Analysis



 ##purpose of the analysis:
                          
 In this analyis  techniques have been used  to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company is used to build a model that can identify the creditworthiness of borrowers.

 ##financial information :

The dataset is related to loans and includes various financial information about borrowers as follows: 
loan_size: The amount of the loan requested by the borrower.
interest_rate: The interest rate associated with the loan.
borrower_income: The income of the borrower.
debt_to_income: The ratio of the borrower's debt to their income.
num_of_accounts: The number of accounts the borrower has.
derogatory_marks: The number of derogatory marks (negative remarks) on the borrower's credit report.
total_debt: The total debt amount of the borrower.

##prediction :

We are predicting the creditworthiness of borrowers based on a dataset of historical lending activity. The primary prediction task is to determine whether a loan is considered risky or not, which is typically represented by a binary target variable.

#basic information about the variables we were trying to predict (e.g., `value_counts`).

Used the value_counts function  to count the occurrences of each unique value in the target variable y. The output indicates the distribution of the target variable loan_status in our dataset.
Class 0 (presumably representing low-risk or healthy loans) has a count of 75,036.
Class 1 (presumably representing high-risk or potentially problematic loans) has a count of 2,500.

##stages of the machine learning process :
 1. Splitting the Data into Training and Testing Sets
 2. Instantiating the Logistic Regression Model
 3. Fitting the model with the training data
 4. Making predictions using the testing data.
 5. Evaluating the model's performance by clculating the accuracy score , generating a confusion matrix and printing a classification report


##Resampling method used:  RandomOverSampler method is used in the analysis which is a resampling technique commonly used in dealing with imbalanced datasets, where one class significantly outnumbers the other. The primary goal of RandomOverSampler is to address class imbalance by randomly duplicating instances from the minority class(high_risk_loans in our dataset) until a more balanced distribution is achieved.

## Results

## Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

* Balanced Accuracy Score: 0.967
A high score indicates good overall performance in correctly predicting both healthy (Class 0) and high-risk (Class 1) loans.

Class 0 (Healthy Loan):

* High precision (1.00): Few false positives, indicating accurate predictions of healthy loans.
* High recall (0.99): Capturing the majority of healthy loans in the predictions
* High F1-score (1.00): Balancing precision and recall for healthy loans.


Class 1 (High-Risk Loan):

* Good precision (0.84): Indicates some false positives, misclassifying high-risk loans as healthy.
* High recall (0.94): Capturing a significant portion of high-risk loans in the predictions.
* Good F1-score (0.89): Balancing precision and recall for high-risk loans.



## Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

 * Balanced Accuracy Score: 0.994
A very high score indicates excellent overall performance in correctly predicting both healthy (Class 0) and high-risk (Class 1) loans.

Class 0 (Healthy Loan):

* Precision: 1.00
Indicates accurate predictions of healthy loans.
* Recall: 0.99
Captures the majority of healthy loans in the predictions.
* F1-score: 1.00
Balances precision and recall for healthy loans.


Class 1 (High-Risk Loan):

* Precision: 0.84
Indicates some false positives, misclassifying high-risk loans as healthy.
* Recall: 0.99
Captures a significant portion of high-risk loans in the predictions.
* F1-score: 0.91
Balances precision and recall for high-risk


## Summary
Both models perform exceptionally well in predicting loan risk, with high balanced accuracy, precision, recall, and F1-scores.
The RandomOverSampler model shows a slight improvement in recall for high-risk loans, suggesting effectiveness in addressing class imbalance.

Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Yes the perfomance does depend on the problem we are trying to solve. In a credit card fraud detection scenario:
Predicting 1 (fraud):
High recall is essential to capture as many fraudulent transactions as possible.
Predicting 0 (no fraud):
High precision is crucial to avoid inconveniencing customers with false alarms.
In summary, the performance goal depends on the specific problem, its context, and the consequences of different types of errors. It is essential to align model objectives with business objectives and stakeholder priorities to make informed decisions about model performance and evaluation.





