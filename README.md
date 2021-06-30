# Risky_Business

![Credit Risk] (Resources/credit-risk.jpg)

## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, a client has asked that you help them predict credit risk with machine learning techniques.

In this repository, I will build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so I will need to employ different techniques for training and evaluating models with imbalanced classes. I will use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

---

### Files

[Resampling Notebook](Notebooks/credit_risk_resampling.ipynb)

[Ensemble Notebook](Notebooks/credit_risk_ensemble.ipynb)

[Lending Club Loans Data](Resources/LoanStats_2019Q1.csv.zip)

---

### Instructions

#### Resampling

Use the [imbalanced learn](https://imbalanced-learn.readthedocs.io) library to resample the LendingClub data and build and evaluate logistic regression classifiers using the resampled data.

To begin:

1. Read the CSV file into a DataFrame.

2. Split the data into Training and Testing sets.

3. Scale the training and testing data using the 'StandardScaler' from 'sklearn.preprocessing'.

4. Use the provided code to run a Simple Logistic Regression:
    * Fit the 'logistic regression classifier'.
    * Calculate the 'balanced accuracy score'.
    * Display the 'confusion matrix'.
    * Print the 'imbalanced classification report'.

Next you will:

1. Oversample the data using the 'Naive Random Oversampler' and 'SMOTE' algorithms.

2. Undersample the data using the 'Cluster Centroids' algorithm.

3. Over- and undersample using a combination 'SMOTEENN' algorithm.


For each of the above, you will need to:

1. Train a 'logistic regression classifier' from 'sklearn.linear_model' using the resampled data.

2. Calculate the 'balanced accuracy score' from 'sklearn.metrics'.

3. Display the 'confusion matrix' from 'sklearn.metrics'.

4. Print the 'imbalanced classification report' from 'imblearn.metrics'.

#### Resampling Conslusions

* Which model had the best balanced accuracy score?

Both the SMOTE oversampling and the SMOTEENN combination(over/under sampling) yielded the highest balanced accuracy scores. The Naieve oversampling method was very close to both the SMOTE and the SMOTEENN methods.

- SMOTE = 0.9948693133232134
- SMOTEENN = 0.9948693133232134
- Naive oversampling = 0.9948426324267352


* Which model had the best recall score?

Naive oversampling, SMOTE, and SMOTEENN all yielded the highest Recall Scores at:

- High Risk = 1.00
- Low Risk = 0.99


* Which model had the best geometric mean score?

All of the resampling techniques in my analysis yielded the same results in f1 scores:

- High Risk = 0.92
- Low Risk = 1.00
- avg / total = 0.99


#### Ensemble Learning