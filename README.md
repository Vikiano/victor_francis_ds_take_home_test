# Fraud Detection Machine Learning Model

## Overview
This project aims to develop a machine learning model to detect fraudulent behavior on a website. The model is designed to balance between preventing frauds while reducing frictions for legitimate users.

## Table of Contents
- [Dataset Description](#dataset-description)
- [Data Analysis](#data-analysis)
- [Modeling](#modeling)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [Visualization](#visualization)
- [Bonus Questions](#bonus-questions)

## Dataset Description
The data provided by the client includes:
1. `requests.csv`:
   - Contains information about each request made to the website.
   - Features related to counts (`count_feat_0` to `count_feat_17`), anomalies (`anomaly_feat_0` to `anomaly_feat_3`), and user interactions (`interaction_feat_0` to `interaction_feat_3`).
   - `is_attack`: Target variable indicating if the request was fraudulent.
   - `timestamp`: Time stamp of the request (anonymized).

2. `device_info.csv`:
   - Contains device-related information for each user.
   - `device_info_1` and `device_info_2`: Information about the user’s device.

## Data Analysis
- Data from `requests.csv` and `device_info.csv` were merged based on the account ID.
- Addressed missing values and encoded categorical features.
- Visualized the distributions of features and analyzed their relationships with the target variable (`is_attack`).

## Modeling
- Multiple models were evaluated, including Logistic Regression, Decision Tree, Random Forest, SVM, KNN, GBMs, and XGBoost.
- XGBoost emerged as the best model based on a combination of performance metrics and interpretability.

## Key Findings
- Anomaly features, particularly `anomaly_feat_0` to `anomaly_feat_3`, play a pivotal role in determining fraudulent behavior.
- Some count and device features also show notable correlations with fraudulent activities.
- The ROC curve of the XGBoost model indicates a good trade-off between True Positive Rate and False Positive Rate.

## Recommendations
- Deploy the XGBoost model for production use after further fine-tuning and based on business requirements.
- Continuously monitor model performance and retrain with new data to ensure accuracy.

## Visualization
- Engaging interactive visualizations have been created using Plotly to delve deeper into feature distributions, correlations, and pairwise relationships.

## Bonus Questions
Addressed various concerns regarding:
- Model deployment and considerations for real-time predictions.
- Handling datasets with incomplete fraudulent information.
- Strategies for retraining and updating the model in production.
