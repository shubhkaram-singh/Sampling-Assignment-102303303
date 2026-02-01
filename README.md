# Sampling Techniques for Imbalanced Data  
### Credit Card Fraud Detection

## Overview
This project demonstrates how **sampling techniques** improve machine learning performance on **highly imbalanced datasets**, using a real-world **Credit Card Fraud Detection** dataset.

The focus is on improving **fraud (minority class) detection** without sacrificing overall model stability.

---

## Problem Statement
Fraud transactions are extremely rare compared to normal transactions.  
Standard ML models achieve high accuracy but **fail to detect fraud** due to class imbalance.

---

## Dataset Summary

| Property | Value |
|--------|-------|
| Total Samples | 772 |
| Total Features | 30 |
| Target Variable | Class (0 = Non-Fraud, 1 = Fraud) |
| Fraud Samples | 9 |
| Non-Fraud Samples | 763 |

---

## Methodology

| Step | Description |
|-----|------------|
| Train-Test Split | Stratified split to preserve class ratio |
| Scaling | StandardScaler |
| Sampling | SMOTE (Synthetic Minority Over-sampling Technique) |
| Model | Logistic Regression |
| Metrics | Precision, Recall, F1-score |

---

## Key Results

| Scenario | Fraud Recall | Fraud F1-score |
|--------|--------------|----------------|
| Before Sampling | Very Low | Poor |
| After SMOTE | **Significantly Improved** | **Improved** |

> ⚠️ Accuracy alone was misleading; recall and F1-score provided meaningful insights.

---

## Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn
- Google Colab

---

## Author
**Shubhkaram Singh**  
Roll Number: 102303303
