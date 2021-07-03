# Risky_Business

![Credit Risk] (Resources/credit-risk.jpg)

## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, a client has asked that you help them predict credit risk with machine learning techniques.

In this repository, I will build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so I will need to employ different techniques for training and evaluating models with imbalanced classes. I will use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. Resampling
2. Ensemble Learning

---

### Files

Resampling Notebook

Ensemble Notebook

Lending Club Loans Data

LoanStats_2019Q1

---

#### Resampling

Use the [imbalanced learn](https://imbalanced-learn.readthedocs.io) library to resample the LendingClub data and build and evaluate logistic regression classifiers using the resampled data.

The following resampling techniques were used:

- Naive Random Oversampler and SMOTE oversampling algorithms

- Cluster Centroid algorithm was used for undersampling

- SMOTEENN algorithm used over and under sampling

#### Resampling Conslusions

* Which model had the best balanced accuracy score?

SMOTE yielded the higest balanced accuracy score, with Naive oversampling and SMOTEENN algorithms very close behind.

- SMOTE =  0.9964419277417877 
- Naive oversampling = 0.9964152894892571
- SMOTEENN = 0.9963087364791345


* Which model had the best recall score?

Naive oversampling, SMOTE, and SMOTEENN all yielded the highest Recall Scores at:

- High Risk = 1.00
- Low Risk = 0.99


* Which model had the best geometric mean score?

Naive oversampling, SMOTE, and SMOTEENN algorithm techniques in my analysis yielded the same perfect results in f1 scores:

- High Risk = 1.00
- Low Risk = 1.00
- avg / total = 1.00


#### Ensemble Learning

The following ensemble classifiers were used to predict the loan risk:

- Balanced Random Forest Classifier

- Easy Ensemble Classifier

#### Ensemble Conclusions

Which model had the best balanced accuracy score?

- The Easy Ensemble Classifier yielded the highest balanced accuracy score.
- 0.9050199629954231

Which model had the best recall score?

- the Easy Ensemble Classifier yielded the highest recall score.
- high risk = 0.86
- low risk = 0.95
- avg/total = 0.95

Which model had the best geometric mean score?

The Easy Ensemble Classifier yielded the highest geometric mean score.
- high risk = 0.90
- low risk  = 0.90
- avg/total = 0.90

What are the top three features?

The top 3 features are:
- 'total_rec_prncp'
- 'total_pymnt'
- 'total_rec_int'