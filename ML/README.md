# Customer Churn Prediction

## Project Overview

Customer Churn Prediction is a machine learning classification project that predicts whether a customer is likely to churn based on customer usage and support-related information.

The project follows a complete machine learning workflow including data preprocessing, feature engineering, exploratory data analysis, model training, evaluation, comparison, and final prediction.

## Project Type

- Machine Learning
- Binary Classification

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Jupyter Notebook

## Dataset

The project uses customer information collected from multiple data sources:

- Account information
- Usage logs
- Support ticket information
- Historical churn labels

The datasets are combined using `account_id`.

## Features Used

The final model uses the following important features:

- `tenure_months`
- `total_usage`
- `ticket_count`

These features represent customer tenure, product usage, and support interaction.

## Machine Learning Models

The following classification algorithms were evaluated:

1. K-Nearest Neighbors (KNN)
2. Logistic Regression
3. Random Forest

Model performance was compared using:

- Accuracy
- Precision
- Recall
- F1-score

Cross-validation was also used during model evaluation.

## Data Preprocessing

The project includes:

- Data quality checks
- Merging multiple customer datasets
- Missing value handling
- Categorical and numerical feature processing
- Feature preparation
- Class imbalance analysis

## Exploratory Data Analysis

Exploratory analysis was performed to understand:

- Customer churn distribution
- Feature distributions
- Relationships between customer usage and churn
- Support ticket patterns
- Important patterns in customer behaviour

Matplotlib was used for visualization.

## Class Imbalance

The churn and non-churn classes were not perfectly balanced.

Therefore, multiple evaluation metrics were considered instead of relying only on accuracy. A balanced Logistic Regression model using `class_weight="balanced"` was also evaluated.

## Model Evaluation

The models were evaluated using stratified cross-validation and classification metrics.

The final model was selected based on its overall performance, with particular importance given to the F1-score for the churn class.

## Final Prediction

The trained model was used to predict churn for previously unseen customers.

The final predictions are stored in:

`final_churn_predictions.csv`

The output contains:

- `account_id`
- `Predicted_Churn`

Possible prediction values are:

- `Churn`
- `No Churn`

## Project Files

- `saas_churn_final_faculty_complete.ipynb` – Complete machine learning notebook
- `account_master.csv` – Customer account information
- `usage_logs.csv` – Customer usage information
- `support_tickets.csv` – Support ticket information
- `churned_labeled.csv` – Historical churn labels
- `churned_to_predict.csv` – Customers used for final prediction
- `final_churn_predictions.csv` – Final prediction results
- `requirements.txt` – Required Python libraries
- `ML Mini Project - Final.docx` – Project documentation

## Conclusion

This project demonstrates an end-to-end machine learning workflow for customer churn prediction, from data preparation and exploratory analysis to model training, evaluation, model selection, and final prediction.

The project can help businesses identify customers who may be at risk of churn and support data-driven customer retention strategies.
