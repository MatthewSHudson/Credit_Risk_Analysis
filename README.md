# Credit_Risk_Analysis

## Overview
The purpose of this analysis is to implement a linear classifier with over sampling, undersampling and a combinations of both used on the dataset. Additionally, we implement 2 ensemble classifiers. These classifiers are attempting to model the relationship between consumers and their credit score. It is a binary classification task, so the target labels are simply: high risk or low risk.

## Results
The balanced accuracy scores, precision, and recall of the logistic regression models that were fit on each sampling method are summarized in the below table:

Sampling Method|Balanced Accuracy|Precision|Recall
---|---|---|---
random oversampling|0.6047| 0.99|0.63
SMOTE oversampling|0.5889| 0.99| 0.63
cluster centroids undersampling|0.4749|0.99|0.42
SMOTEENN combination sampling|0.5107|0.99|0.48

Accuracy scores, precision, and recall for the two ensemble learning methods are summarized in the table below:

Ensemble Method|Balanced Accuracy|Precision|Recall
---|---|---|---
balanced random forest|0.7885|0.99|0.87
adaboost easy ensemble|0.9317|0.99|0.94

## Summary
Overall the results show that ensemble methods perform much better on the task of classifying creditors into high and low risk. We recommend either of the ensemble learners for this task, however when we look at the precision and recall for high_risk credits we see that the adaboost ensemble method has a precision score of 0.09 and recall of 0.92 meaning that 9% of those classified as `high_risk` acutally are, but that 92% of those that are high risk are classified as such. While this still outperforms every other models precision and recall score for high risk credits, we would hesitate to actually use this model in production since there would be many people who would be denied loans and should be approved/
