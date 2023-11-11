# credit-risk-classification

## Overview of the Analysis

The purpose of this analysis is to build a model that can identify the creditworthiness of borrowers as healthy or high risk using Machine learnig.
The dataset was based on Loan Risk and the dataset of historical lending activity from a peer-to-peer lending services company was used, Here we are predicting if it is healthy or high risk to approve fund for borrowers.
A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
The stages of machine learning includes splitting the data into test and train, creating a model, fit the model using training data, make a prediction using the testing data and evaluate the performance by calculating the accuracy score of the model, generate a confusion matrix and printing the classification report.
One of the method used is LogisticalRegression which was imported from SKlearn, it was instantiated using a random state of 1.

## Results

. Machine Learning Model 1:

Balanced Accuracy Score: 0.95

Confusion Matrix of Testing Data:

[[18663,   102],[56,   563]]

Classification report precision recall f1-score support

                  precision    recall  f1-score   support

healthy loan 1.00 0.99 1.00 18765
high-risk loan 0.85 0.91 0.88 619

      accuracy                           0.99     19384
     macro avg       0.92      0.95      0.94     19384

weighted avg 0.99 0.99 0.99 19384

The balanced accuracy score of the first model is approximately 95%. This model is better at predicting low-risk loans than it is for high-risk. As the recall for healthy loans is 0.99, whereas the recall for high risk loans is 0.91. In the confusion matrix we see there were 56 false positives, and 102 false negatives.

. Machine Learning Model 2:

Balanced Accuracy Score: 0.99

Confusion Matrix of Resampled Data:

[[18649 116] [ 4 615]]

Classification report precision recall f1-score support

                precision    recall  f1-score   support

healthy loan 1.00 0.99 1.00 18765
high-risk loan 0.84 0.99 0.91 619

      accuracy                           0.99     19384
     macro avg       0.92      0.99      0.95     19384

weighted avg 0.99 0.99 0.99 19384

The balanced accuracy score of this second model is approximately 99%. This is also true for the recall, which is 0.99 for both low and high-risk loans. This model predicts high-risk loans much better than the first. In the confusion matrix there were 4 false positives and 116 false negatives.

## Summary

Considering the balanced accuracy score and recall, the second model performs better when predicting high-risk loans, while the first and second model can predict low-risk loans at the same accuracy. While the confusion matrix predicts slightly more false negatives in the second model, it predicts a considerable amount less of false positives. Therefore, I would recommend using Model 2, the logistic regression model fitted with oversampled data.
