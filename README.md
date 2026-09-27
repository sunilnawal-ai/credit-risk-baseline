# 📘 Credit Risk Baseline Model (UCI Credit Card Dataset)

## 📌 Project Overview
This project builds a baseline credit‑risk prediction model using the UCI Credit Card Default dataset.  
The goal is to predict whether a customer will default on their next payment using historical billing and payment behavior.

This notebook represents **Day 1** of a multi‑day roadmap designed to build a complete, production‑ready credit‑risk ML pipeline.

---

## 🏦 Business Context — Why This Model Matters
Credit‑risk modeling helps lenders:

- reduce losses  
- improve approval decisions  
- optimize credit limits  
- support regulatory compliance  
- understand risk drivers  

This project sets the foundation for a full credit‑risk ML system.

---

## 📊 Dataset — UCI Credit Card Default
The dataset contains **30,000 customers** with:

- demographic features  
- payment history  
- bill amounts  
- past default behavior  
- next‑month default status (target)

Target variable: `default.payment.next.month`  
- 0 = non‑default  
- 1 = default  

The dataset is **imbalanced**, making metrics like **ROC AUC** more reliable than accuracy.

---

## ⚙️ Model — Logistic Regression Baseline
Logistic Regression is used as the baseline model because it is:

- simple  
- interpretable  
- fast  
- stable on imbalanced data  
- widely used in credit‑risk modeling  

It provides probability outputs and coefficients that help risk teams understand feature impact.

---

## 📐 Evaluation Metrics
The model is evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- ROC AUC  
- Confusion Matrix  

### 🔍 Why ROC AUC Matters
ROC AUC measures **ranking quality**, not raw correctness.

> If I pick one defaulter and one non‑defaulter, how often does the model rank the defaulter as higher risk?

This makes it ideal for imbalanced datasets.

---

## 🧱 Notebook Structure

1. Title + Overview
2. Load Libraries
3. Load Dataset
4. Train/Test Split (Stratified)
5. Preprocessing (Placeholder for Day 2)
6. Baseline Model — Logistic Regression
7. Evaluation Metrics
8. Confusion Matrix
9. Day 1 Summary
10. Next Steps (Day 2 Preview)
    
---

## 📈 Day 1 Results
Baseline model performance:

- Accuracy: ~0.78  
- Precision: ~0.52  
- Recall: ~0.61  
- F1 Score: ~0.56  
- ROC AUC: ~0.704  

Interpretation:

- The model catches **61%** of true defaulters  
- It ranks risky vs. safe customers correctly **70%** of the time  
- Strong baseline without preprocessing  

---

## Day 2 — Feature Engineering + Preprocessing
- Scaling  
- Encoding  
- Leakage‑free pipeline  
- Correlation analysis  

---

## Day 3 — Random Forest vs XGBoost (Credit Risk Modeling)

**Objective:** Compare three models — Logistic Regression, Random Forest, and XGBoost — on a credit risk dataset to understand performance, feature importance, and model selection tradeoffs.

### Key Results
- **AUC Scores:**  
  - Logistic Regression: 0.70  
  - Random Forest: 0.76  
  - XGBoost: 0.77  

- **Feature Importance Differences:**  
  - Random Forest emphasizes continuous, stable features (e.g., BILL_AMT1, AGE).  
  - XGBoost concentrates on ordinal delinquency indicators (PAY_0, PAY_1, PAY_2).  

### PM Interpretation
- Logistic Regression provides a transparent baseline.  
- Random Forest offers stability and robustness for production.  
- XGBoost delivers the strongest predictive performance by leveraging gradient boosting.  

### Deliverables
- Clean notebook with model training, evaluation, and plots  
- PM-level interpretation section  
- GitHub commit documenting modeling progress  

---

## 🚀 Roadmap — What Comes Next
### Day 4 — Threshold Tuning  
### Day 5 — ROC/AUC Deep Dive  
### Day 6 — Model Comparison  
### Day 7 — Final Model + Presentation  

---

## 🗂️ Repository Structure

```
credit-risk-baseline/
│
├── data/
├── notebooks/
│   └── day1_baseline_model.ipynb
    └── day2_feature_engineering.ipynb
    └── day3_LR_RF_XGB.ipynb
├── README.md
└── .gitignore

```
---

## 🧠 Skills Demonstrated

- ML fundamentals  
- Credit‑risk domain knowledge  
- Evaluation metrics  
- Data leakage prevention  
- Stratified splitting  
- Model interpretation  
- Professional notebook structuring  
- Clear communication  

---

