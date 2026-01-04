# Credit Risk Prediction using Logistic Regression

## 📌 Project Overview
This project builds a machine learning–based credit risk assessment system that predicts the probability of a customer defaulting on a credit payment.  
The model is designed as a **decision-support system** to help banks decide whether to approve, review, or reject loan applications.

---

## 🎯 Problem Statement
Banks face financial losses when loans are approved for high-risk customers who later default.  
The goal of this project is to:
- Predict default risk using historical customer data
- Convert model predictions into actionable business decisions

---

## 📊 Dataset
- Source: UCI Machine Learning Repository – Credit Card Default Dataset
- Size: ~30,000 customer records
- Target Variable:
  - `Y = 0` → No default
  - `Y = 1` → Default

---

## 🧠 Approach
1. Data cleaning and preprocessing
2. Feature scaling using StandardScaler
3. Train–test split with stratification
4. Logistic Regression model training
5. Model evaluation using confusion matrix and recall
6. Probability-based risk scoring
7. Business rule–based loan decision system

---

## 📈 Model Evaluation
- Accuracy is reported, but emphasis is placed on:
  - Recall for defaulters
  - Confusion matrix analysis
- This reflects real-world banking priorities

---

## 🏦 Decision Logic
Based on predicted default probability:
- **< 30%** → APPROVE
- **30–60%** → REVIEW
- **> 60%** → REJECT

---

## 🔍 Explainability
Logistic Regression coefficients are analyzed to understand:
- Which features increase default risk
- Which features reduce risk

This ensures transparency, which is critical in financial applications.

---

## 🛠️ Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 🚀 How to Run
```bash
pip install -r requirements.txt
