# Module 12 - Credit Risk Classification

## Overview of the Analysis

This analysis seeks to predict which loans are likely to be healthy and which are likely to be high-risk, which could be incredibly useful to lending companies who are looking to invest wisely. The model was trained on a dataset that included the size of the loan, interest rate, borrower income, borrower debt, the number of acccounts, and the number of derogatory marks on the borrower's record. This information was used to predict what the status of the loan would be--whether it would turn out to be healthy or unhealthy.

In order to create this model, I first separated the "loan_status" column into it's own dataframe. After this I split the data into training and testing datasets, so that I can see how well the model works and allow it to learn and improve. I then created a logistic regression model which seeks to predict the y data (or the loan status). After allowing the model to train, I evaluated it's performance by generating a confusion matrix for the model and printing a classification report.

## Results

              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

* Precision: The precision score represents the ratio of correctly predicted positive observations (true positives) to the total predicted positives (true positives + false positives). Basically, it shows the accuracy of the model's positive predictions. For class 0, or healthy loans, the precision is 1.00. This means that the model was 100% effective at positively predicting healthy loans. For class 1, or unhealthy loans, the precision is 0.85. This means the model was only 85% effective at positively predicting unhealthy loans.

* Recall: Recall is the ratio of correctly predicted positive observations (true positives) to the total actual positives (true positives + false negatives). This measures how well the model is able to identify positive results. For class 0, healthy loans, the recall is 0.99, indicating that 99% of healthy loans were correctly identified. For class 1, unhealthy loans, the recall is 0.91, meaning that 91% of the actual class 1 instances were correctly identified.

* Accuracy: Accuracy is the ratio of correct predictions (both true positives and true negatives) to the total number of predictions. This is intended to measure overall model performance. The overall accuracy of the model is 0.99, which means that 99% of the model's predictions were correct.

## Summary

I would reccomend this model for use by lending companies. Overall, it's accuracy was strong. Particularly I would reccomend it as a way to determine a set of loans that are most likely to be healthy, which would be the ones the company would want to take on. I would not reccomend this model as a way to weed out unhealthy loans, as it's precision was much lower when it came to predicting which loans would be unhealthy. 
