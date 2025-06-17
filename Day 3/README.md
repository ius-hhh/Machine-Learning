# 🍷 Day 3 - Wine Quality Prediction

This is Day 3 of the **"30 Days, 30 Machine Learning Projects"** challenge. In this project, we built a machine learning model to predict the **quality of red wine** using physicochemical features.

---

## 📌 Objective

To classify wines as **"Good"** or **"Not Good"** based on their chemical properties such as acidity, alcohol, pH, and residual sugar.

---

## 🧪 Dataset

We used the **Red Wine Quality** dataset from the UCI Machine Learning Repository.

- **File:** `winequality-red.csv`
- **Features:** 11 physicochemical inputs
- **Target:** Quality (integer score between 0 and 10)

We converted this score into binary classification:
- 1 → Good quality (score ≥ 7)
- 0 → Not good quality (score < 7)

---

## 🛠️ Tech Stack

- Python 🐍
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn (Random Forest Classifier)

---

## 🧠 ML Workflow

1. **Data Loading & Inspection**
2. **Preprocessing**
   - Handled missing values (if any)
   - Binary target transformation
3. **Data Visualization**
   - Distribution of quality
   - Heatmap of correlations
4. **Model Training**
   - Used `RandomForestClassifier`
5. **Evaluation**
   - Confusion matrix
   - Classification report
   - Accuracy score

---

## 📈 Results

Our model was able to classify wine quality with decent accuracy. Feature correlation revealed that **alcohol** is a strong positive indicator of wine quality.

---

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/ius-hhh/Machine-Learning.git
   cd Machine-Learning/Day 3
