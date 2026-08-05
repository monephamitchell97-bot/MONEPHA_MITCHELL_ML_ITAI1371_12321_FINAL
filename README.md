Customer Churn Classification Using Machine Learning
Project Information

Student: Monepha Mitchell
Course: ITAI 1371 – Machine Learning
Project Type: Binary Classification
Target Variable: Churn

Project Overview

This project uses machine learning to predict whether a telecommunications customer will churn. Customer churn occurs when a customer stops using a company’s products or services.

The project compares six individual classification models and two ensemble models. Each model was evaluated using validation and test datasets to determine which approach provided the strongest customer-churn predictions.

Dataset

The project uses the Telco Customer Churn dataset, which contains 7,043 customer records and information related to:

Customer demographics
Account tenure
Phone and internet services
Contract type
Payment method
Monthly charges
Total charges
Customer churn

Dataset source:

https://raw.githubusercontent.com/VedD376/ITAI-1371-ML-Dataset/main/WA_Fn-UseC_-Telco-Customer-Churn.csv

Data Preparation

The following data-preparation steps were completed:

Converted TotalCharges from text to numerical values
Replaced 11 missing TotalCharges values with zero
Removed the non-predictive customerID column
Created the TenureGroup feature
Created the NumberOfServices feature
One-hot encoded categorical features
Standardized numerical features
Balanced only the training data using RandomOverSampler
Data Split

The dataset was divided using stratified sampling:

Training set: 70%
Validation set: 15%
Test set: 15%

The training set was used to train the models. The validation set was used to compare models and select the strongest approaches. The test set remained untouched until the final evaluation.

Models

The following individual models were trained:

Logistic Regression
Decision Tree Classifier
Random Forest Classifier
Gradient Boosting Classifier
K-Nearest Neighbors Classifier
Support Vector Classifier

Two ensemble models were also created:

Average Ensemble
Bayesian Ensemble
Evaluation Metrics

Each model was evaluated using:

Accuracy
Precision
Recall
F1-score
ROC-AUC
Final Results

Gradient Boosting was the strongest individual validation model, producing a validation ROC-AUC of 0.8376.

The Bayesian Ensemble produced the strongest final test performance:

Metric	Score
Accuracy	0.7711
Precision	0.5470
Recall	0.7893
F1-Score	0.6462
ROC-AUC	0.8531

The Bayesian Ensemble identified approximately 79% of customers who actually churned.

Repository Contents
data/ — Dataset and source information
notebooks/ — Complete Jupyter Notebook
reports/ — Written report and model-comparison PDF
presentation/ — Final presentation deck
reflection/ — Reflection journal
results/ — Model results and visualizations
How to Run the Notebook
Download or clone this repository.
Install the required Python libraries.
Open notebooks/Monepha_Mitchell_Final_ML_Project.ipynb.
Run the notebook cells in order from beginning to end.
Main Python Libraries
pandas
NumPy
Matplotlib
scikit-learn
imbalanced-learn
Conclusion

The results demonstrate that machine learning can use customer account, service, contract, and billing information to estimate churn risk. The Bayesian Ensemble produced the strongest overall test performance by combining predictions from the best individual models.
