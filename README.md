# AI Job Market and Salary Trends - Final Project

## Project Overview
This project analyzes the **Global AI Job Market and Salary Trends (2025)** dataset to explore factors affecting AI job roles and salaries worldwide. The goal is to perform data analysis and build machine learning models to predict salary trends and job market insights.

## Dataset
The dataset is sourced from Kaggle:

[Global AI Job Market and Salary Trends 2025](https://www.kaggle.com/datasets/bismasajjad/global-ai-job-market-and-salary-trends-2025)

You can download the CSV file and place it in the `/data` folder of this repository.

## Project Requirements
The project covers:

- **Data Loading & Preparation:** Imported and cleaned the dataset, handled missing data, and engineered new features.
- **Exploratory Data Analysis (EDA):** Visualized and explored relationships between features.
- **Feature Engineering:**
  - Created `num_skills` from the comma-separated skills column.
  - Removed extreme salary outliers (top 1% and bottom 0.1%) to improve model robustness.
- **Machine Learning Models:** Implemented and evaluated:
  - Linear Regression
  - Random Forest Regressor
- **Model Tuning:** Performed hyperparameter tuning using `GridSearchCV` for both Random Forest and regularized linear models (Ridge and Lasso).
- **Model Evaluation:** Used MAE, RMSE, and R² for model evaluation.

## Key Concepts Used

**GridSearchCV:**  
A scikit-learn tool used to find the best combination of hyperparameters for a model by performing an exhaustive search across specified parameter values using cross-validation.

**MAE (Mean Absolute Error):**  
The average of the absolute differences between predicted and actual values. It gives a straightforward sense of how far off the predictions are on average.

**RMSE (Root Mean Squared Error):**  
The square root of the average squared differences between predicted and actual values. It penalizes larger errors more than MAE and is sensitive to outliers.

**R² Score (Coefficient of Determination):**  
Measures how well the model explains the variance in the target variable.  
- `R² = 1` means perfect prediction.  
- `R² = 0` means the model does no better than simply predicting the average.

## Original Results

### Without tuning, using all primary features:
- **Linear Regression Evaluation**
MAE : 15,953.41
RMSE: 21,010.50
R² : 0.8561

- **Random Forest Regressor Evaluation**
MAE : 15,164.81
RMSE: 21,035.32
R² : 0.8558

## Fine-Tuned Results

### Tuned Random Forest (Expanded Grid - 30+ mins)
Performed grid search over 324 combinations with 3-fold cross-validation:
- **Tuned Random Forest Evaluation**
MAE : 14,268.83
RMSE: 19,513.56
R² : 0.8759

### Polynomial Ridge Regression (Few Seconds)
- **Polynomial Ridge Regression Evaluation**  
  MAE : 14,966.45  
  RMSE: 20,032.77  
  R²  : 0.8692

## Getting Started

1. Clone this repository:
    ```bash
    git clone https://github.com/HansenBlakestudentgreenriveredu/AI-Job-Market-and-Salary-Trends.git
    cd AI-Job-Market-and-Salary-Trends
    ```

2. Place the dataset CSV file inside the `/data` folder.

3. Open the Jupyter notebook located in `/notebooks` to start exploring the data and building models.

## Tools & Libraries

- Python 3.x  
- Jupyter Notebooks  
- Pandas  
- NumPy  
- Matplotlib / Seaborn  
- Scikit-learn  