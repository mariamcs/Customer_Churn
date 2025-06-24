# 📉 Customer Churn Prediction with XGBoost + SHAP

This project predicts churn using the Telco Customer dataset. XGBoost is used as the model, and SHAP is applied for interpretability.

## 🔍 Problem Statement
Predict whether a customer will cancel their subscription based on their usage, contract, payment method, and services used.

## 📊 Features
- Contract type
- MonthlyCharges, TotalCharges
- Tenure
- InternetService, StreamingTV
- Tech support, Online security
- Payment method

## 🔧 Tools
- XGBoost
- SHAP
- Scikit-learn, Pandas, Seaborn

## 🧠 Key Insights from SHAP
- Long-term contracts reduce churn risk
- Short tenure and high monthly charges increase churn
- Not using online services (e.g., tech support) increases churn

## ▶️ Run This Project in Colab
Upload the dataset and run `netflix_churn_prediction.ipynb`.
