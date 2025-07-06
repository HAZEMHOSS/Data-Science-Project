# Assignment 2 – Titanic Dataset Cleaning & Preprocessing

## 📌 Objective
This project explores and cleans the Titanic dataset to prepare it for modeling. The notebook applies two different data preprocessing strategies and evaluates the implications of each.

## 📊 Dataset
The dataset is the Titanic passenger manifest used in many binary classification tasks (Survived vs. Not Survived). It contains features such as age, fare, cabin, and passenger class.

## ⚠️ Issues Identified
- **Missing Values:** High in `Cabin` (77%) and moderate in `Age` (∼20%)
- **Outliers:** Detected in `Age` and `Fare` via IQR method
- **Imbalance:** Survived class is imbalanced (62% vs. 38%)
- **High Cardinality:** `Name`, `Ticket`, and `Cabin` have excessive unique values

## 🧪 Methods Used

### ✅ Method 1 – Drop Missing & Remove Outliers
- Drops all rows with missing values
- Removes extreme outliers based on IQR
- Drops high-cardinality columns (`Name`, `Ticket`, `PassengerId`)

### ✅ Method 2 – Impute, Cap, and Engineer
- Zero-imputes `Age`, and fills `Embarked` with `"Unknown"`
- Caps outliers using percentile and IQR
- Extracts Deck info from `Cabin`
- Drops raw `Name` and `Ticket` but suggests advanced feature engineering
- Applies SMOTE to balance classes

## 💡 Insights
Both methods reflect different real-world scenarios:
- Method 1 is faster and cleaner but sacrifices data.
- Method 2 retains more data with advanced feature engineering and class balancing.

## 🛠 Tools Used
- Python
- pandas
- seaborn / matplotlib
- scikit-learn
- imbalanced-learn (for SMOTE)

## 🚀 How to Run
1. Open the notebook in the `notebooks/` folder.
2. Follow the markdown guidance and run the cells step-by-step.
3. Experiment with both methods and their effect on models.

---

🎓 Authored by: **Hazem Hossam Hassan (202101119)**
