# 📊 Customer Churn Prediction – EDA & Data Cleaning Summary

## 🔹 Dataset Overview
- Source: Telco Customer Churn Dataset (Kaggle)
- Rows: `~7043` | Columns: `21`
- Target Variable: `Churn` (Yes/No → Converted to 1/0)

## 🔹 Initial Cleaning Steps
- Dropped `customerID` (unique identifier, not useful for modeling)
- Identified and handled missing values in `TotalCharges`:
  - Converted `TotalCharges` to numeric using `pd.to_numeric()`
  - Coerced invalid entries to `NaN` and dropped affected rows (`~11`)
- Checked for and confirmed absence of duplicate rows

## 🔹 Categorical Column Handling
- Identified binary categorical columns (`Yes`/`No`)
- Converted to numeric (`1` = Yes, `0` = No) for modeling:
  - `Partner`, `Dependents`, `PhoneService`, `PaperlessBilling`, `Churn`

## 💡 Next Steps
- Perform deeper exploratory data analysis (EDA)
- Handle multi-class categorical variables (e.g., `InternetService`)
- Perform feature engineering and scaling for model training
