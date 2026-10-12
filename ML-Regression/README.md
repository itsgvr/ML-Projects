# Predicting Cloud Infrastructure Cost per Customer Account

## Project Overview

This project uses Machine Learning regression models to predict the next month's cloud infrastructure cost for customer accounts based on account information, resource usage, and API activity.

The goal is to build a reliable regression workflow that helps estimate future cloud costs.

## Problem Statement

Cloud infrastructure costs vary depending on resource consumption and customer account characteristics. Predicting future costs can help organizations understand expected expenses and improve cost planning.

This project predicts the next month's cost for customer accounts using historical data.

## Objectives

- Explore and understand the available datasets.
- Perform data cleaning and preprocessing.
- Aggregate usage and API activity at the account level.
- Combine account information with usage data.
- Handle missing values and investigate outliers.
- Train and compare multiple regression models.
- Evaluate models using appropriate regression metrics.
- Apply cross-validation and hyperparameter tuning.
- Generate predictions for accounts without known target values.

## Dataset Description

The project uses the following datasets:

- `account_master.csv`
- `usage_logs.csv`
- `api_call_logs.csv`
- `next_month_cost_usd_labeled.csv`
- `next_month_cost_usd_to_predict.csv`

The labeled dataset is used for model training and evaluation. The prediction dataset contains accounts for which the next month's cost must be estimated.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Machine Learning Models

The following regression models are compared:

1. Linear Regression
2. Random Forest Regressor
3. Gradient Boosting Regressor

Hyperparameter tuning is performed for the Random Forest model using GridSearchCV.

## Model Evaluation

The models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

Five-fold cross-validation is used for model comparison, and a separate test set is used for final evaluation.

## Results

The final tuned Random Forest model achieved the following test-set performance:

- **MAE:** 100.86
- **RMSE:** 128.76
- **R²:** 0.788

These metrics are calculated on the held-out test set. MAE and RMSE are expressed in the target cost's units, USD.

The final notebook also includes visualizations and feature-importance analysis.

## Final Predictions

The notebook generates predictions for 44 customer accounts.

Output file:

`next_month_cost_usd_predictions_final.csv`

## How to Run

1. Clone or download this repository.
2. Install the required Python libraries.
3. Place the notebook and required CSV files in the same project folder.
4. Open `Regression_Project_FINAL_CHECKED.ipynb` in Jupyter Notebook or VS Code.
5. Run the notebook cells in order.

Install the main dependencies using:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
