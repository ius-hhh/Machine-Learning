# 🏠 Day 4 - Boston Housing Price Prediction

This is Day 4 of the **"30 Days, 30 Machine Learning Projects"** challenge.  
In this project, we aim to predict housing prices in Boston using various features such as crime rate, number of rooms, and accessibility to highways.

---

## 📌 Project Objective

To build a regression model that accurately predicts the **median house price** in different areas of Boston using the Boston Housing dataset.

---

## 📊 Dataset Description

Each row in the dataset represents a Boston neighborhood and contains the following features:

- `CRIM`: per capita crime rate by town
- `ZN`: proportion of residential land zoned for large lots
- `INDUS`: proportion of non-retail business acres per town
- `CHAS`: Charles River dummy variable (1 if tract bounds river; 0 otherwise)
- `NOX`: nitrogen oxides concentration
- `RM`: average number of rooms per dwelling
- `AGE`: proportion of owner-occupied units built before 1940
- `DIS`: weighted distances to employment centers
- `RAD`: index of accessibility to radial highways
- `TAX`: property-tax rate
- `PTRATIO`: pupil-teacher ratio by town
- `B`: 1000(Bk - 0.63)^2 (Bk = % Black population)
- `LSTAT`: % lower status of the population
- `MEDV`: **Median value of owner-occupied homes (target)**

---

## 🚀 What You Will Learn

- Load and preprocess the dataset
- Explore feature-target relationships
- Apply feature scaling
- Train Linear Regression and regularized models (Ridge, Lasso)
- Evaluate model performance using MAE, RMSE, and R²

---

## 🧠 ML Concepts Used

- Linear Regression
- Feature Scaling (StandardScaler)
- Ridge & Lasso Regression
- Evaluation Metrics (MAE, RMSE, R²)

---

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

---

## 📈 Future Improvements

- Try polynomial regression or tree-based models
- Perform hyperparameter tuning using GridSearchCV
- Analyze residuals more deeply
