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



## 🔍 Real-World Considerations for Churn Modeling

While this project uses the Telco dataset as a teaching example, real-world churn modeling at companies like Netflix is significantly more complex. Here's how a production-grade churn model would differ:

### 🔑 Feature Categories in Real-World Use:
- **User Behavior & Engagement**
  - `daily_watch_minutes`, `binge_sessions_last_30d`, `completion_rate`, `last_login_gap_days`
- **Subscription & Billing**
  - `plan_type`, `tenure_months`, `billing_failures`, `price_per_hour_watched`
- **Customer Support**
  - `support_interactions_count`, `cancel_reason`, `csat_score`
- **Device & Access Patterns**
  - `device_diversity`, `primary_device_type`, `geo_consistency`, `simultaneous_streams_used`
- **Social / Network Influence**
  - `referral_source`, `shared_account_likelihood`, `household_engagement_diff`

### 🧠 Advanced Techniques
- **Time-decay features** to capture behavior trends
- **Latent embeddings** for user similarity
- **Sequential modeling** with LSTMs or Transformers
- **Text mining** from customer reviews or support tickets

These features help streaming companies personalize retention strategies, surface better content, and detect early signs of disengagement.


## 💡 Real-World Complexity Beyond This Example

This project uses a simplified Telco dataset to demonstrate churn modeling with XGBoost and SHAP.

In production settings (like Netflix), churn prediction involves:
- Session-level data with behavioral signals
- Subscription metadata, billing anomalies, plan changes
- Customer support transcripts (NLP)
- Sequential data modeling (e.g., session trends over time)
- Explainability + fairness monitoring in deployment

Future versions of this project will incorporate synthetic datasets and real-time modeling pipelines to simulate production-grade churn systems.

