# Credit Risk Prediction and Decision Support System


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

The project was developed iteratively to reflect a real-world machine learning workflow:

1. Established a baseline model using Logistic Regression
2. Evaluated performance using precision, recall, and F1-score
3. Introduced Random Forest to capture non-linear relationships
4. Applied resampling techniques (SMOTE / SMOTE-ENN) on training data to address class imbalance
5. Performed probability threshold tuning to optimize recall–precision trade-offs
6. Analyzed diminishing returns to identify data-driven performance limits

The final system emphasizes interpretability, robustness, and business-aligned decision-making rather than metric inflation.

---

## 📈 Model Evaluation
- Accuracy is reported, but emphasis is placed on:
  - Recall for defaulters
  - Confusion matrix analysis
- This reflects real-world banking priorities
Final evaluation on the test set yielded an F1-score in the range of 0.5–0.6, consistent across multiple modeling approaches.


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


## 🔁 Model Iteration & Performance Analysis

Multiple models and techniques were evaluated during development:

- Logistic Regression (baseline)
- Random Forest Classifier
- Random Forest with SMOTE
- Random Forest with SMOTE-ENN
- Probability threshold tuning for F1 optimization

Across these approaches, the F1-score plateaued around 0.5–0.6, with precision and recall exhibiting similar trade-offs. This behavior indicates significant class overlap and limited separability in the dataset.

Rather than overfitting or introducing data leakage to inflate metrics, the project prioritizes:
- Honest evaluation on unseen test data
- Recall-aware analysis for defaulters
- Probability-based risk scoring
- Business-driven decision thresholds

This mirrors real-world credit risk modeling constraints.

## 🚀 Future Improvements

Potential extensions of this project include:
- Gradient boosting models (e.g., XGBoost, LightGBM)
- Cost-sensitive learning
- Domain-specific feature engineering
- Time-aware modeling of payment behavior


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
Open `notebooks/eda.ipynb` and run all cells from top to bottom.