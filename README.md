# 👔 Employee Performance Analysis – INX Future Inc.

A machine learning project to analyze and predict employee performance ratings using HR data from INX Future Inc., developed as part of the IABAC certification project.

---

## 📌 Project Overview

INX Future Inc. observed a decline in employee performance, with service delivery issues rising and client satisfaction dropping by 8 percentage points. This project uses data analysis and machine learning to:

- Understand department-wise performance trends
- Identify the key factors influencing employee performance
- Build a predictive model to classify employee performance ratings
- Provide actionable recommendations to management

---

## 📂 Dataset

- **File:** INX_Future_Inc_Employee_Performance_CDS_Project2_Data_V1.csv
- **Records:** 1,200 employees
- **Features:** 28 columns (demographic, job-related, compensation, work environment)
- **Target Variable:** `PerformanceRating` (2 = Low, 3 = Average, 4 = High)

---

## 🔍 Project Workflow

1. **Data Understanding & Cleaning**
   - No missing values or duplicates found
   - Dropped `EmpNumber` (unique identifier, not useful for prediction)
   - Handled class imbalance in target variable using SMOTE

2. **Exploratory Data Analysis (EDA)**
   - Univariate analysis on 9 continuous features
   - Department-wise performance distribution
   - Relationship between features and performance ratings

3. **Feature Engineering & Encoding**
   - Label Encoding for ordinal categorical variables
   - One-Hot Encoding for nominal categorical variables

4. **Model Training & Evaluation**
   - Trained 4 tree-based models: Decision Tree, Random Forest, Gradient Boosting, XGBoost
   - Evaluated using Accuracy, F1 Score, Precision, Recall, and Accuracy Gap

5. **Hyperparameter Tuning**
   - GridSearchCV applied on best model (Random Forest)
   - Cross-validation with F1 weighted scoring

---

## 📊 Model Results

| Model              | Train Accuracy | Test Accuracy | Accuracy Gap | F1 Score |
|-------------------|----------------|---------------|--------------|----------|
| Decision Tree      | 1.00           | 0.85          | 0.15         | 0.85     |
| Random Forest      | 1.00           | 0.93          | 0.07         | 0.92     |
| Gradient Boosting  | 0.99           | 0.92          | 0.07         | 0.92     |
| XGBoost            | 1.00           | 0.90          | 0.10         | 0.90     |
| **RF (Tuned) ✅**  | **0.98**       | **0.91**      | **0.07**     | **0.91** |

✅ **Best Model:** Tuned Random Forest — most stable and production-ready

---

## 🔑 Top 3 Factors Affecting Employee Performance

1. **Job Involvement** – Higher engagement leads to better performance
2. **Environment Satisfaction** – A positive workplace directly improves productivity
3. **Training Opportunities** – Employees with more training perform significantly better

---

## 🛠️ Libraries Used

- `pandas`, `numpy` — data handling
- `matplotlib`, `seaborn` — visualization
- `scikit-learn` — preprocessing, modeling, evaluation
- `xgboost` — XGBoost classifier
- `imbalanced-learn (SMOTE)` — handling class imbalance

---

## 💡 Business Recommendations

- Enroll low performers in mentorship and skill development programs
- Improve work environment satisfaction across underperforming departments
- Integrate the model into the hiring process to identify high-potential candidates
- Retrain the model every 6–12 months as employee data evolves
- Use model predictions as a **decision-support tool**, not a final verdict

---

## ⚠️ Ethical Note

This model is designed to support HR decisions, not replace human judgment. Transparency and fairness must be maintained when using predictions that impact employee careers.

