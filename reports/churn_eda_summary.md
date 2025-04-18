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

## 🧠 Key Findings & Insights

- Customers on **month-to-month contracts** churned significantly more than those on long-term contracts.
- Lack of **tech support**, **fiber internet**, and **electronic check payment** were also associated with higher churn rates.
- The logistic regression model achieved:
  - **Accuracy**: ~79.5%
  - **Precision (Churn)**: 63%
  - **Recall (Churn)**: 54%
- This suggests the model is solid overall but slightly struggles to catch all actual churners (common with imbalanced data).

---

## 🧰 Tools & Techniques Used

- Python (Pandas, NumPy, Seaborn, Scikit-learn)
- Jupyter Notebooks
- Data cleaning, encoding, feature engineering
- EDA visualizations + churn analysis
- Logistic Regression modeling + evaluation

