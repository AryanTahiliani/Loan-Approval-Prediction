# 🚀 Loan Approval Prediction

**An end-to-end ML pipeline that ingests, cleans, models, and serializes a classifier to predict term-deposit subscription.**

## 📖 Project Overview

**Goal:**  
Predict whether a bank client will subscribe to a term deposit (`y` = yes/no).

**Why it matters:**  
Helps banks target the right customers and boost conversion.

## 📂 Dataset

- **Source:** Proprietary dataset from intellipaat 
- **Rows after cleaning:** 41,183  
- **Features:** 20 customer & campaign attributes  
- **Target:** `y` (yes=1, no=0)

## 🧹 Data Cleaning & Preprocessing

1. Dropped 15 duplicate rows.  
2. Removed 1 row missing the target.  
3. Handled remaining missing values via median (numeric) and most-frequent (categorical) imputation.  
4. One-hot encoded categoricals; scaled numeric features.

## 🔬 Modeling & Evaluation

We trained three models inside `sklearn` Pipelines:

| Model               | ROC AUC | Accuracy | Precision | Recall | F1   |
|---------------------|--------:|---------:|----------:|-------:|-----:|
| Logistic Regression | 0.939   | 0.910    | 0.646     | 0.440  | 0.523 |
| Random Forest       | 0.943   | 0.914    | 0.664     | 0.487  | 0.562 |
| XGBoost (Tuned)     | 0.952   | 0.919    | 0.665     | 0.569  | 0.613 |

## 📈 Top Features (XGBoost)

1. **nr.employed**  
2. **duration**  
3. **poutcome_success**  
4. **cons.conf.idx**  
5. **emp.var.rate**

