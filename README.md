# 📌 Loan Default Risk Prediction with Business Cost Optimization

## 📖 Project Overview

This project builds an end-to-end machine learning system to predict loan default risk using the **Home Credit Default Risk Dataset**.  

Unlike traditional ML projects that optimize for accuracy alone, this project focuses on **business cost optimization**, adjusting the decision threshold to minimize financial loss from incorrect loan decisions.

The solution includes:

- Data cleaning & preprocessing  
- Class imbalance handling (SMOTE vs Class Weights)  
- Model training (Logistic Regression & CatBoost)  
- Business cost-based threshold optimization  
- SHAP explainability (Top 5 feature drivers)  
- Deployment-ready model artifacts  

---

## 🎯 Problem Statement

Financial institutions face significant losses due to loan defaults.  
Approving a high-risk applicant (False Negative) is far more expensive than rejecting a reliable applicant (False Positive).

The challenge is to:

- Predict the probability of default
- Optimize decision thresholds
- Minimize total business cost

---

## 🚀 Objectives

- Build a binary classification model to predict loan defaults.
- Handle severe class imbalance.
- Compare Logistic Regression vs CatBoost.
- Define business costs for misclassification.
- Optimize model threshold based on financial impact.
- Explain predictions using SHAP.
- Prepare the system for deployment.

---

## 📂 Dataset

**Home Credit Default Risk Dataset**

- 307,511 applications
- 120+ engineered features after preprocessing
- Target variable:
  - `0` → Non-default
  - `1` → Default

---

## ⚙️ Technologies Used

- Python
- Pandas & NumPy
- Scikit-learn
- CatBoost
- Imbalanced-learn (SMOTE)
- SHAP
- Matplotlib & Seaborn
- Joblib (model saving)

---

## 🔍 Project Workflow

### 1️⃣ Data Inspection
- Checked dataset shape and structure
- Analyzed missing values
- Explored class imbalance

### 2️⃣ Data Preprocessing
- Missing value imputation
- One-hot encoding for categorical features
- Feature scaling
- Train-test split

### 3️⃣ Handling Class Imbalance
- SMOTE oversampling
- Class-weighted modeling
- Performance comparison

### 4️⃣ Model Training
- Logistic Regression (baseline)
- CatBoost (primary model)
- Evaluated using AUC, confusion matrix, classification report

### 5️⃣ Business Cost Definition

Defined custom financial costs:

- False Positive (FP) → Cost = 1  
- False Negative (FN) → Cost = 10  

This reflects real-world risk: approving a defaulter is significantly more expensive.

### 6️⃣ Threshold Optimization

- Tested thresholds from 0.1 to 0.9
- Computed business cost at each threshold
- Selected threshold minimizing total cost
- Compared SMOTE vs Class-weight models

### 7️⃣ SHAP Explainability

- Identified Top 5 most influential features
- Visualized feature importance
- Increased transparency for business stakeholders

---

## 📊 Key Results

- CatBoost outperformed Logistic Regression in AUC.
- SMOTE improved minority class detection.
- Default threshold (0.5) was NOT optimal.
- Adjusting threshold significantly reduced total business cost.
- SHAP revealed the strongest predictors of loan default.

---

## 💡 Business Insight

Optimizing for accuracy alone is misleading.

The optimal model is the one that minimizes **financial loss**, not classification error.

This project demonstrates how machine learning should be aligned with real business objectives.

---

## 📈 Model Deployment Ready

The following artifacts are saved:

- `model.pkl`
- `scaler.pkl`

These can be directly integrated into:

- Streamlit app
- API endpoint
- Internal decision support systems

---

## 🏁 Final Conclusion

This project demonstrates:

- End-to-end ML pipeline development
- Handling imbalanced financial datasets
- Business-aware threshold optimization
- Explainable AI integration
- Deployment readiness

It reflects **real-world financial decision systems**.

---

## 👩‍💻 Author

Tehmina Afzal  
Artificial Intelligence & Data Science at ITSOLERA PVT LTD

---

