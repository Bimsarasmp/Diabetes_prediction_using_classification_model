# Diabetes Prediction Model

## Overview

This project focuses on predicting the likelihood of diabetes based on various health metrics using machine learning models. The dataset includes features such as Glucose levels, BMI, age, etc., and the target variable indicates the presence or absence of diabetes.

## Dataset

- **Structure:** (768, 9)
- **Null Values:** None
- **Duplicates:** None
- **Handling Missing Values:** Certain numerical values like Blood Pressure, skin thickness, etc., are realistically non-zero. Missing values are replaced with the mean for improved accuracy.

## Data Preprocessing

### Oversampling

To address class imbalance and enhance the prediction of true positives (TP), oversampling is performed.

## Correlation Analysis

Certain features like Glucose, Age, and BMI exhibit notable correlations with the target variable, providing initial insights into potential predictors.

## Model Performance Metrics

### 1. Logistic Regression (Without SMOT)

- **Precision:** 0.686
- **Recall:** 0.636
- **F1 Score:** 0.660
- **Accuracy:** 0.766

### 2. Logistic Regression (With SMOT)

- **Precision:** 0.755
- **Recall:** 0.792
- **F1 Score:** 0.773
- **Accuracy:** 0.765

### 3. Logistic Regression (C=0.01)

- **Precision:** 0.760
- **Recall:** 0.782
- **F1 Score:** 0.771
- **Accuracy:** 0.765

### 4. SGD Classifier (CV=2)

- **Precision:** 0.688
- **Recall:** 0.712
- **F1 Score:** 0.700
- **Accuracy:** 0.7275

## Insights from Model Coefficients

- Positive coefficients: Glucose, Age, and BMI contribute positively to the likelihood of diabetes.
- Negative coefficients: Certain features have an inverse relationship with the likelihood of diabetes.

## Model Selection Recommendation

Considering the importance of precision in healthcare applications, **Logistic Regression with SMOT** is recommended. It demonstrates a balance between precision, recall, and F1 score, making it suitable for predicting diabetes with minimized false positives.



