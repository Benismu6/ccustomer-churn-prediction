# 📊 Customer Churn Prediction

This project uses the [Telco Customer Churn Dataset](https://www.kaggle.com/datasets/puja19/telcom-customer-churn) to predict which customers are likely to leave a telecom service, using Python and machine learning.

## 🚀 Project Highlights

- Cleaned and preprocessed customer data
- Performed EDA to identify churn risk patterns
- Built and evaluated a logistic regression model
- Shared visual findings and final model evaluation
- Includes real-world insights applicable to retention strategies

## 📁 Project Structure
- customer-churn-prediction/
  - data/ → Raw dataset (CSV)
  - notebooks/ → Jupyter notebooks for EDA and modeling
  - models/ → Trained model files (e.g., .pkl)
  - reports/ → Markdown summaries and insights
  - .gitignore → Git exclusions
  - README.md → Project overview

## ✅ Results

- **Accuracy**: 79.5%
- **Precision (Churn)**: 63%
- **Recall (Churn)**: 54%
- Customers with month-to-month contracts and no tech support were most likely to churn

## 📎 Tools

- Python • Pandas • NumPy • Scikit-learn • Seaborn • Jupyter

---

## 📌 Next Steps

- Try other models (e.g., Random Forest, XGBoost)
- Address class imbalance using SMOTE or class weights
- Deploy model or dashboard using Streamlit or Flask

### 📦 Trained Model File

- `logistic_regression_churn.pkl` – Serialized trained model using `joblib`
- To load the model in Python:

```python
import joblib
model = joblib.load('models/logistic_regression_churn.pkl')

