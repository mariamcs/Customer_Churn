# 🚪 Netflix Churn Prediction Project

Welcome to this end-to-end AI/ML project where we simulate Netflix-style user data and build a complete pipeline to predict customer churn — one of the most critical problems in subscription-based businesses.

---

## 📌 Project Overview

In this project, we walk through:

- 🎯 Problem Framing: What is churn? Why does it matter?
- 🛠️ Data Simulation: Generate a realistic dataset with user behavior and service metrics
- 🧼 Data Cleaning: Handle missing values and prepare the data
- 🧠 Feature Engineering: Derive meaningful signals like average watch time per login
- 🔄 Transformation: Encoding, normalization, and vector assembly
- 📈 Model Training: Use `XGBoostClassifier` for robust prediction
- 📊 Evaluation: Check metrics like AUC, Precision, Recall, and feature importance (SHAP)

---

## 🧪 Simulated Dataset (100K Users)

| Category              | Feature Name                       | Description                                                                 |
|-----------------------|------------------------------------|-----------------------------------------------------------------------------|
| 🎥 Engagement         | `daily_watch_minutes`              | Avg. minutes watched per day                                               |
|                       | `avg_session_length`               | Avg. watch session duration                                                |
|                       | `last_login_days_ago`              | How many days ago user last logged in                                      |
|                       | `binge_sessions_last_30d`          | Number of binge sessions in last 30 days                                   |
|                       | `completion_rate`                  | Ratio of completed shows                                                   |
| 💳 Subscription       | `plan_type`                        | Type of plan (Basic / Standard / Premium)                                  |
|                       | `tenure_months`                    | Months since the user subscribed                                           |
|                       | `price_per_hour_watched`           | Value proxy for cost per watch hour                                        |
|                       | `billing_failures_last_90d`        | Payment failures in the past 3 months                                      |
|                       | `upgrades_last_6mo`                | Plan upgrades in last 6 months                                             |
| 📱 Service Usage      | `has_kids_profile`                 | Whether they use a kids profile                                            |
|                       | `uses_download_feature`            | Uses download feature (True/False)                                         |
|                       | `simultaneous_streams_used`        | Avg. concurrent streams used                                               |
|                       | `primary_device_type`              | Streaming device (Mobile/TV/Desktop/etc.)                                  |
|                       | `geo_consistency_score`            | Location change pattern (lower = suspicious)                              |
| 🛎️ Customer Support   | `support_tickets_last_6mo`         | How many support interactions                                              |
|                       | `cancel_reason_code`               | Reason category for cancelation                                            |
|                       | `issue_resolution_time_avg`        | Average time to resolve support tickets                                    |
| 🎯 Target             | `churned`                          | 1 if user churned, 0 otherwise                                             |

---

## 🔧 Feature Engineering Examples

- **watch_per_session** = daily_watch_minutes / avg_session_length
- **engagement_score** = completion_rate × binge_sessions
- **churn_risk_score** = billing_failures × (1 + support_tickets)

---

## 🧼 Data Cleaning Steps

- Impute missing numerical values with mean or median
- Fill missing categoricals with "Unknown"
- One-hot encode categorical features
- Normalize skewed numeric features

---

## 🔍 Model of Choice: XGBoost

- Handles both numeric & categorical data
- Robust to outliers and missing values
- Great for structured data
- Feature importance support via SHAP

---

## 📊 Evaluation Metrics

- AUC (Area Under ROC Curve)
- Accuracy
- Precision / Recall / F1
- SHAP plots for feature impact

---

## 📂 File Structure

