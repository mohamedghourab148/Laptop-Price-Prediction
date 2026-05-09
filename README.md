# Laptop Price Prediction

This project builds a machine learning regression pipeline to predict laptop prices (in Euros) based on hardware specifications and product characteristics.

## Problem Statement
Laptop pricing depends on multiple interacting factors such as CPU type, RAM, storage configuration, GPU, and display quality. The goal of this project is to model these relationships and accurately predict laptop prices using supervised machine learning.

## Dataset Overview
The dataset contains laptop specifications including:
- Company, Product series
- CPU characteristics (family, generation, frequency)
- RAM, Storage type and capacity
- GPU category
- Screen size and resolution

**Target variable:** `Price (Euro)`

## Data Preprocessing & Feature Engineering
- Removed irrelevant identifiers
- Extracted structured features from text columns (CPU, GPU, Memory, Resolution)
- Engineered new numerical features (e.g. PPI, total storage)
- One‑hot encoded categorical variables
- Applied feature scaling using StandardScaler
- Ensured no missing values or data leakage

## Exploratory Data Analysis (EDA)
Key insights:
- RAM, CPU frequency, and weight show strong correlation with price
- Gaming and workstation laptops are significantly more expensive
- Intel‑based laptops dominate the higher price range

## Models Implemented
- Linear Regression
- Ridge Regression (regularized & tuned)
- Lasso Regression
- Polynomial Regression
- Decision Tree Regression

Each model was evaluated using cross‑validation with R², RMSE, and MAE.

## Model Selection
✅ **Ridge Regression** achieved the best performance:
- R² ≈ 0.89
- Improved generalization due to L2 regularization

## Technologies
- Python
- Pandas, NumPy
- Scikit‑learn
- Matplotlib, Seaborn
- Jupyter Notebook

## Future Improvements
- Try ensemble models (Random Forest, Gradient Boosting)
- Apply log‑target transformations systematically
- Interpret feature importance using SHAP

## Kaggle Competition
This project was developed as part of a Kaggle machine learning competition focused on predicting laptop prices.

- A complete preprocessing, modeling, and prediction pipeline was implemented
- Final predictions were generated and submitted in Kaggle-compatible format
- Submission file: `submissions/kaggle_submission.csv`

Kaggle competition link: <https://www.kaggle.com/competitions/project-1-laptop-price-prediction/leaderboard>
**Result:0.875** Achieved competitive R² score using Ridge Regression with extensive feature engineering.
