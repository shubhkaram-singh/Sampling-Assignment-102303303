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

## Dataset
- Total samples: **772**
- Features: **30**
- Target variable:
  - `0` → Non-Fraud  
  - `1` → Fraud

### Class Distribution (Before Sampling)
- Non-Fraud: **763**
- Fraud: **9**

---

## Methodology
1. Stratified Train-Test Split  
2. Feature Scaling  
3. Sampling Technique:
   - **SMOTE (Synthetic Minority Over-sampling Technique)**
4. Model Used:
   - **Logistic Regression**
5. Evaluation Metrics:
   - Precision, Recall, F1-score (focus on Fraud class)

---

## Key Results
- Sampling significantly **improved recall for fraud detection**
- Model learned meaningful fraud patterns instead of biasing toward majority class
- Demonstrates why **accuracy alone is misleading** in imbalanced problems

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
