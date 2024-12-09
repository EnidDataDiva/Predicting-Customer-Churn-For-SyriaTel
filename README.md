# Predicting Customer Churn for SyriaTel

## Overview
This project aims to build a predictive model to identify customers at risk of churning for SyriaTel, a telecommunications provider. Customer churn is a critical issue that impacts revenue and profitability, and this project leverages data analysis and machine learning to develop actionable insights and retention strategies.

## Table of Contents
- [Overview](#overview)
- [Business Understanding](#business-understanding)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Conclusions](#conclusions)
- [Recommendations](#recommendations)
- [Next Steps](#next-steps)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)
- [Repository Structure](#repository-structure)

## Business Understanding
Customer churn refers to customers discontinuing a service or switching to competitors. For SyriaTel, predicting churn is vital for reducing revenue loss and improving customer retention. By using historical data and machine learning, this project aims to help SyriaTel take proactive retention measures.

### Challenges
- Class imbalance in churn data.
- Identifying non-linear relationships between features and churn.
- Ensuring interpretability of the churn model for stakeholders.

## Objectives
1. **Develop a Predictive Model:** Identify customers likely to churn using decision tree-based models.
2. **Feature Insights:** Analyze customer behavior to uncover churn predictors like international plans and customer service interactions.
3. **Retention Strategies:** Provide actionable recommendations based on data-driven insights.

## Dataset
The dataset contains 3,333 rows and 21 columns, including features like `total_day_minutes`, `international_plan`, `customer_service_calls`, and the target variable `churn`. It is sourced from Kaggle and includes both categorical and numerical features.

### Key Features:
- **Numerical:** `total_day_minutes`, `total_international_calls`, `charge_per_minute`.
- **Categorical:** `international_plan`, `voice_mail_plan`, `region`.

### Target Variable:
- `churn` (1 = Churned, 0 = Not Churned).

## Exploratory Data Analysis (EDA)
1. **Univariate Analysis:** Examined the distribution of features and identified class imbalance in the target variable (`churn`).
2. **Bivariate Analysis:** Highlighted strong correlations between usage metrics (e.g., `total_day_minutes`) and churn.
3. **Multivariate Analysis:** Identified interaction effects, such as high usage coupled with international plans, as strong predictors of churn.

## Modeling
Three decision tree models were built:
1. **Baseline Decision Tree:** A simple model without hyperparameter tuning or class balancing.
2. **Tuned Decision Tree:** Used SMOTE to handle class imbalance and optimized hyperparameters using GridSearchCV.
3. **Further Tuned Decision Tree:** Expanded hyperparameter grid and included pruning techniques for improved precision and recall balance.

### Metrics of Success:
- Precision
- Recall
- F1-Score
- AUC-ROC

## Evaluation
The further tuned decision tree achieved the best results:
- **Precision:** 0.94
- **Recall:** 0.79
- **F1-Score:** 0.86
- **AUC-ROC:** 0.88

## Conclusions
- Customers with international plans and frequent customer service calls are more likely to churn.
- High usage metrics like `total_day_minutes` and `total_day_charge` indicate dissatisfaction when paired with poor service.
- Retention efforts should focus on these high-risk segments.

## Recommendations
1. Introduce loyalty programs for high-usage customers with international plans.
2. Enhance customer service to address dissatisfaction among frequent callers.
3. Conduct regular satisfaction surveys to identify pain points and improve service.

## Next Steps
- Deploy the churn prediction model into SyriaTel’s CRM system for real-time insights.
- Collect additional data points like customer satisfaction scores and competitor offers.
- Continuously monitor and refine the model based on new data and feedback.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/EnidDataDiva/customer-churn-prediction.git
