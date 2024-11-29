# Our Team
- Mohamed Ahmed
- Hassan Abdelsattar
- Mostafa Mohamed
- Nada Elgendy
- Eslam Mohamed
# Customer Churn Prediction

This project aims to predict customer churn for a telecommunications company using a dataset of customer details and services. The focus is on building machine learning models to determine the likelihood of customer churn based on various factors like internet service, monthly charges, contract type, and more.

## Table of Contents
- [Introduction](#introduction)
- [Business Problem](#business-problem)
- [Data Overview](#data-overview)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Conclusion](#conclusion)

## Introduction
Customer churn prediction is a critical task for companies in competitive industries. By predicting churn, businesses can take action to retain customers who are likely to leave. This project explores different machine learning techniques to solve the problem of churn prediction.

## Business Problem
The goal is to predict whether a customer will leave (churn) based on their historical service data and usage patterns. Identifying these customers can help the company take proactive steps to improve customer retention.

## Data Overview
The dataset contains customer information such as:
- **Demographics**: Gender, Senior Citizen, Partner, Dependents
- **Services**: PhoneService, InternetService, Contract, PaymentMethod, etc.
- **Account Information**: Tenure, MonthlyCharges, TotalCharges, etc.

The target variable is `Churn`, which indicates whether a customer has left the service (Yes) or not (No).

## Data Preprocessing
Steps taken for cleaning and preparing the data:
- Missing data handling for the `TotalCharges` column.
- Conversion of categorical variables to numerical values using techniques like one-hot encoding.
- Handling of multi-category features and binary variables.
- Dropping duplicates and irrelevant columns like `customerID`.

## Modeling
Two models were used for the prediction of customer churn:

1. **K-Nearest Neighbors (KNN)**:
   - The KNN classifier was used to predict churn based on the nearest neighbors' voting system.
   - Steps include splitting the data into training and testing sets, standardizing numerical features, and evaluating performance using metrics like precision, recall, and F1-score.

2. **Random Forest Classifier**:
   - A Random Forest model was also implemented to capture more complex relationships between features. This model uses multiple decision trees to make robust predictions.
   - The same steps were followed for data splitting, training, and testing. Random Forest provides better interpretability and can handle non-linear relationships in the data.

## Evaluation
The models' performance is evaluated using a confusion matrix and classification reports:

### KNN Model:
- **Accuracy**: 81%
- **F1-score for churn class**: 0.55

### Random Forest Model:
- **Accuracy**: 73%
- **F1-score for churn class**: 0.51

Both models show that the Random Forest classifier outperforms KNN, particularly in predicting the minority churn class.

## Conclusion
The Random Forest model provided better results compared to KNN, with higher accuracy and F1-score for the churn class. The next steps could include further tuning of the models or exploring other algorithms like logistic regression or gradient boosting to improve performance further.
