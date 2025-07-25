# 🛠️ Predictive Maintenance Using Machine Learning

This project aims to predict machine failure using sensor data collected from industrial machinery. The dataset is based on real-world simulations and includes features like temperature, torque, rotational speed, and tool wear.

Machine learning models such as Random Forest, Decision Tree, Logistic Regression, KNN, SVC, and XGBoost were applied. XGBoost, when combined with feature engineering, SMOTE, and hyperparameter tuning via GridSearchCV, delivered the best performance.

---

## 📁 Dataset

- **Source**: `ai4i2020.csv` from [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)
- **Size**: 10,000 rows, 14 columns
- **Target Variable**: `Machine failure` (0 = No failure, 1 = Failure)

---

## 🔍 Exploratory Data Analysis (EDA)

- Checked for missing values and duplicates.
- Removed outliers using both **IQR** and **Z-score**.
- Visualized distributions with histograms and boxplots.
- Explored failure distribution across machine types (`L`, `M`, `H`).
- Feature correlations visualized using a heatmap.

---

## ⚙️ Feature Engineering

Created new features to enhance model performance:

- `Torque_Speed_Ratio` = Torque / Rotational Speed
- `Power(W)` = (2π × Rotational Speed × Torque) / 60
- `Temp_diff` = Process Temperature − Air Temperature

---

## 🧠 Model Building

- **Train-test split**: 80-20 with stratification.
- **SMOTE** used to handle class imbalance.
- **StandardScaler** used for feature scaling.
- Applied multiple algorithms:
  - Logistic Regression
  - Random Forest
  - K-Nearest Neighbors
  - Support Vector Classifier
  - Decision Tree
  - **XGBoost** (Best performing)

---

## 🔎 Hyperparameter Tuning (XGBoost)

Used `GridSearchCV` on a pipeline including SMOTE, StandardScaler, and XGBoost:

param_grid = {
    'xgb__n_estimators': [100, 200],
    'xgb__max_depth': [3, 5, 7],
    'xgb__learning_rate': [0.01, 0.1, 0.2],
    'xgb__subsample': [0.8, 1]
}
---

## 📫 About Me

**Muhammad Umer**  
🎓 Electrical Engineering Graduate (June 2025)  
🔍 Aspiring Data Scientist | Machine Learning & IoT Enthusiast 

