# Sampling Techniques for Imbalanced Data  
## Credit Card Fraud Detection

## Overview
This project focuses on handling highly imbalanced datasets using sampling techniques.  
A real-world Credit Card Fraud Detection dataset is used to study how class imbalance affects model performance and how sampling improves minority-class detection.

The goal is to improve fraud detection performance while maintaining overall model stability.

---

## Problem Statement
In fraud detection, fraudulent transactions are extremely rare compared to normal transactions.  
Traditional machine learning models tend to favor the majority class, leading to poor fraud detection despite high accuracy.

Objective:
- Handle class imbalance using sampling techniques
- Improve recall for the minority (fraud) class
- Evaluate model performance using appropriate metrics

---

## Dataset Description
- Dataset: Credit Card Fraud Detection
- Total Samples: 772
- Total Features: 30
- Target Variable:
  - 0 → Non-Fraud
  - 1 → Fraud

### Class Distribution (Before Sampling)
- Non-Fraud (0): 763
- Fraud (1): 9

The dataset is highly imbalanced.

---

## Methodology

### 1. Data Loading and Exploration
- Loaded the dataset using pandas
- Checked dataset shape and feature structure
- Verified class imbalance using value counts

---

### 2. Train-Test Split
- Performed stratified train-test split
- Preserved original class distribution in test data
- Prevented data leakage

---

### 3. Sampling Technique
**SMOTE (Synthetic Minority Over-sampling Technique)** was applied on training data only.

After SMOTE:
- Non-Fraud (0): 534
- Fraud (1): 534

This balanced the dataset and allowed the model to learn fraud patterns.

---

### 4. Feature Scaling
- Used StandardScaler
- Improved model convergence
- Necessary for Logistic Regression

---

### 5. Model Used
**Logistic Regression**
- Simple and interpretable baseline model
- Increased max iterations for convergence
- Trained on SMOTE-balanced data

---

### 6. Evaluation Strategy
Evaluation focused on:
- Precision
- Recall
- F1-score
- Special emphasis on fraud recall

Accuracy alone was not considered sufficient.

---

## Results and Observations

### Default Threshold (0.5)
- High overall accuracy
- Very poor fraud detection
- Model biased towards majority class

### Custom Threshold (0.3)
- Fraud recall improved significantly
- Better detection of fraudulent transactions
- Slight drop in accuracy (acceptable trade-off)

Key Insight:
In fraud detection, missing fraud is costlier than false positives.  
Threshold tuning plays a critical role.

---

## Key Learnings
- Accuracy is misleading for imbalanced datasets
- Sampling should be applied only on training data
- SMOTE improves minority-class learning
- Threshold tuning is a business-driven decision
- Logistic Regression remains a strong baseline model

---


---

## How to Run
1. Clone the repository
2. Open the notebook in Jupyter Notebook or Google Colab
3. Install required libraries:
   - pandas
   - numpy
   - scikit-learn
   - imbalanced-learn
4. Run all cells sequentially

---

## Future Improvements
- Use ensemble models like Random Forest or XGBoost
- Compare SMOTE with undersampling methods
- Evaluate using Precision-Recall AUC
- Apply cost-sensitive learning

---

## Author
Shubhkaram Singh  
Roll Number: 102303303

