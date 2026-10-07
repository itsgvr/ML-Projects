# Customer Churn Prediction

## Project Overview

Customer Churn Prediction is a machine learning project developed to predict whether a customer is likely to churn based on customer account information, usage behavior, and support ticket activity.

The project uses customer-level data from multiple sources and applies data preprocessing, feature engineering, model training, evaluation, and final churn prediction.

The main objective is to help identify customers who are at risk of leaving so that appropriate retention strategies can be planned.

---

## Problem Statement

Customer churn is a major challenge for subscription-based and SaaS businesses.

The objective of this project is to build a machine learning classification system that predicts customer churn using:

- Customer account information
- Usage activity
- Support ticket information

The project also compares multiple classification models and selects the most suitable model based on churn-class performance.

---

## Dataset

The project uses the following datasets:

- `account_master.csv` – Customer account information
- `usage_logs.csv` – Customer usage activity
- `support_tickets.csv` – Customer support ticket information
- `churned_labeled.csv` – Historical customer churn labels
- `churned_to_predict.csv` – Customers for whom churn needs to be predicted

---

## Data Preparation

The datasets were combined using customer/account identifiers.

The following preprocessing and feature engineering steps were performed:

- Data loading and inspection
- Missing-value checking
- Data type checking
- Duplicate checking
- Feature selection
- Dataset merging
- Handling class imbalance
- Feature engineering

Important engineered features include:

- `tenure_months`
- `total_usage`
- `ticket_count`

These features were used to represent customer tenure, usage behavior, and support interaction.

---

## Machine Learning Models

The following classification approaches were evaluated:

1. Baseline Model
2. K-Nearest Neighbors (KNN)
3. Logistic Regression
4. Balanced Logistic Regression

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score

Because customer churn is an imbalanced classification problem, special attention was given to the performance of the churn class.

---

## Model Selection

The final model was selected based on the **F1-score of the churn class**, rather than accuracy alone.

The **Balanced Logistic Regression** model was selected as the final model because it provided the best churn-class F1-score among the evaluated models.

### Final Churn-Class F1-Score

**36.36%**

Using the churn-class F1-score as the selection criterion helps ensure that the model does not simply favor the majority class.

---

## Final Prediction

The trained model was applied to the customers in `churned_to_predict.csv`.

The final prediction process identified:

- **58 total customer accounts**
- **53 predicted as churn**
- **5 predicted as no churn**

The final predictions were saved in:

`final_churn_predictions.csv`

The output contains:

- `account_id`
- `churn_prediction`

---

## Project Workflow

```text
Raw Customer Data
        ↓
Data Cleaning & Validation
        ↓
Data Merging
        ↓
Feature Engineering
        ↓
Train/Test Split
        ↓
Model Training
        ↓
Model Comparison
        ↓
Evaluation
        ↓
Balanced Logistic Regression
        ↓
Final Churn Prediction
        ↓
final_churn_predictions.csv

Technologies Used
Python
Pandas
NumPy
Scikit-learn
Jupyter Notebook
Project Files
Customer-Churn-Prediction/
│
├── account_master.csv
├── churned_labeled.csv
├── churned_to_predict.csv
├── final_churn_predictions.csv
├── support_tickets.csv
├── usage_logs.csv
├── saas_churn_final.ipynb
└── README.md
Notebook

The complete implementation, including data preprocessing, feature engineering, model training, model evaluation, and final predictions, is available in:

saas_churn_final.ipynb

Conclusion

This project demonstrates an end-to-end machine learning workflow for customer churn prediction.

The project combines customer account, usage, and support information to identify customers who are likely to churn.

After comparing different classification approaches, Balanced Logistic Regression was selected based on the highest churn-class F1-score.

The final prediction results provide a practical output that can be used for further customer retention analysis.
