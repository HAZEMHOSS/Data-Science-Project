# Assignment 1 – Superstore Dataset Profitability Classification

## 📌 Objective
This project cleans and transforms the Superstore dataset to predict whether an order is profitable. It applies two different preprocessing and feature engineering strategies.

## 📊 Dataset
The dataset includes sales transaction records from a fictional US Superstore. It contains fields such as order dates, customer info, categories, sales, profit, and shipping details.

## ⚠️ Issues Identified
- **Incorrect Formats:** `Order Date` and `Ship Date` stored as text
- **No Missing or Duplicate Data**
- **High Cardinality/Irrelevant Fields:** IDs, names, `Postal Code`, and `Country`
- **Categoricals:** 15 out of 21 columns are `object` type
- **Outliers:** Extreme `Profit` values skew distribution

## 🧪 Methods Used

### ✅ Method 1 – Basic Clean + Date Features
- Drops IDs, names, postal code, and country
- Converts date strings to datetime and extracts features
- Removes outliers in `Profit` via IQR
- One-hot encodes categorical variables

### ✅ Method 2 – Label Encode + Feature Engineering
- Label encodes main categoricals
- Engineers features like `Order Month`, `Shipping Delay`
- Drops raw IDs, date columns, and `Profit`
- Retains more compact representation while enriching features

## 📈 Evaluation Summary

| Metric      | Method 1 | Method 2 |
|-------------|----------|----------|
| Accuracy    | 92.98%   | 94.50%   |
| Precision   | 93.37%   | 94.68%   |
| Recall      | 98.51%   | 98.77%   |
| F1-Score    | 95.87%   | 96.68%   |

### ✅ Conclusion
Method 2 offers superior performance across all metrics, thanks to richer feature engineering and efficient encoding. It is the recommended approach.

## 🛠 Tools Used
- Python
- pandas
- numpy
- seaborn / matplotlib
- scikit-learn

## 🚀 How to Run
1. Open the notebook in the `notebooks/` folder.
2. Follow the documented steps for both methods.
3. Review model metrics and insights.

---

🎓 Authored by: **Hazem Hossam Hassan (202101119)**
