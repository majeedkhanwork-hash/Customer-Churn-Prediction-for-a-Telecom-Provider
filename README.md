# Customer Churn Prediction for a Telecom Provider  
**End-to-End Predictive Analytics & Machine Learning Project**

## Overview
Customer churn is a major challenge for subscription-based businesses, where retaining existing customers is often significantly cheaper than acquiring new ones. This project focuses on predicting customer churn for a telecom provider and identifying the key drivers behind customer attrition.

The goal is twofold:
1. Build and evaluate predictive models that estimate the likelihood of customer churn.
2. Translate model outputs into actionable business insights that can support retention strategies and revenue stability.

The project follows a complete end-to-end workflow, from data preprocessing and exploratory analysis to model development, evaluation, and business recommendations.

---

## Business Context
Telecom companies manage large customer bases with varying contract types, service usage patterns, and billing behaviors. Understanding which customers are most likely to churn allows the business to:
- Prioritize targeted retention campaigns
- Reduce revenue loss from unexpected cancellations
- Improve customer lifetime value through proactive engagement

This analysis simulates how a data team might support decision-making for a telecom provider using historical customer data.

---

## Dataset
- **Records:** ~7,000 customers  
- **Features:** Demographics, account details, service usage, billing information  
- **Target Variable:** Churn (Yes / No)

**Key Attributes Include**
- Contract type and tenure
- Monthly and total charges
- Internet and add-on services
- Payment method and billing preferences
- Demographic indicators

**Data Quality Notes**
- `TotalCharges` required cleaning due to missing and non-numeric values
- Dataset exhibits moderate class imbalance (~26% churn)

---

## Tools & Technologies
- **Python:** Pandas, NumPy, Scikit-learn
- **Machine Learning:** Logistic Regression, Random Forest, Gradient Boosting
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score, ROC-AUC
- **Visualization:** Matplotlib, Seaborn
- **Workflow:** Scikit-learn Pipelines for preprocessing and modeling

---

## Data Preparation & Feature Engineering
Key preprocessing and feature engineering steps included:
- Cleaning and converting billing fields to numeric formats
- Handling missing values and removing invalid records
- Encoding categorical variables using one-hot encoding
- Standardizing numeric features
- Creating derived features such as tenure groups to capture lifecycle behavior
- Stratified train–test split to preserve churn distribution

---

## Modeling Approach
Three classification models were trained and evaluated:
- **Logistic Regression** (interpretable baseline with class balancing)
- **Random Forest** (nonlinear relationships and feature interactions)
- **Gradient Boosting** (high-performance ensemble model)

All models were implemented using Scikit-learn Pipelines to ensure consistent preprocessing and reliable evaluation.

---

## Model Evaluation
Models were evaluated on a held-out test set using multiple metrics to account for class imbalance:
- Accuracy
- Precision and Recall
- F1-score
- ROC-AUC
- Confusion matrices

**Key Result**
- Gradient Boosting achieved the strongest overall performance, with an ROC-AUC of approximately **0.84**, offering a strong balance between precision and recall.
- Logistic Regression provided a competitive and more interpretable alternative, particularly valuable when recall is prioritized.

---

## Key Insights
- Customers on **month-to-month contracts** are significantly more likely to churn than those on longer-term contracts.
- **Low-tenure customers** represent the highest churn risk, indicating the importance of early engagement.
- Higher monthly charges are associated with increased churn probability.
- Customers paying via **electronic check** show higher churn risk compared to automated payment methods.
- Add-on services such as online security and technical support are associated with improved retention.

---

## Business Recommendations
Based on the analysis, the following actions could help reduce churn:
- Encourage migration from month-to-month to longer-term contracts through targeted incentives.
- Strengthen onboarding and early-life engagement for new customers.
- Improve pricing transparency and proactively address billing increases.
- Promote automatic payment methods to reduce friction.
- Bundle or highlight value-added services such as security and technical support.

---

## Repository Structure
├── data/
│ └── Telco_Customer_Churn.csv
├── notebooks/
│ └── Telco_Churn_Analysis.ipynb
├── models/
│ └── model_results_and_evaluation.ipynb
├── reports/
│ └── Customer_Churn_Prediction_Report.pdf
└── README.md
