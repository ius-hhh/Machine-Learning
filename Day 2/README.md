# 🚢 Day 2 - Titanic Survival Prediction

This is the second project in the **"30 Days, 30 Machine Learning Projects"** challenge. In this beginner-friendly project, we built a logistic regression model that predicts whether a passenger survived the Titanic disaster based on various personal and ticket-related features.

---

## 📌 Project Objective

To predict the **Survival** of a passenger on the Titanic using features such as:
- **Pclass** (Passenger Class)
- **Sex**
- **Age**
- **SibSp** (Number of Siblings/Spouses aboard)
- **Parch** (Number of Parents/Children aboard)
- **Fare**
- **Embarked** (Port of Embarkation)

---

## 📊 Dataset

- Source: [Kaggle Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic)
- Format: CSV files
- Total Records: 891 rows × 12 columns (for training data)
- Contains missing values in `Age`, `Cabin`, and `Embarked`

---

## 📁 Files in This Folder

| File | Description |
|------|-------------|
| `Day_2_Titanic_Logistic_Regression.ipynb` | Jupyter Notebook with full preprocessing, modeling, and evaluation |
| `train.csv` | Raw dataset file used for model training |
| `README.md` | Project summary and walkthrough |

---

## ⚙️ Steps Performed

1. **Loaded the Titanic dataset** using `pandas`
2. **Explored the data** with `.head()`, `.info()`, and `.describe()`
3. **Cleaned the data**:
   - Dropped unused or mostly-empty columns (`Cabin`, `Ticket`, `Name`, `PassengerId`)
   - Handled missing values in `Age` and `Embarked`
   - Encoded categorical features `Sex` and `Embarked` using `LabelEncoder`
4. **Visualized survival relationships** using `seaborn` plots
5. **Trained a Logistic Regression model** using `scikit-learn`
6. **Evaluated model performance** using:
   - Accuracy
   - Confusion Matrix
   - Classification Report (Precision, Recall, F1-score)

---

## ✅ Model Performance

**Confusion Matrix**:
```
[[90 15]
 [19 55]]
```

**Accuracy**: `81%`  
**Precision (Survived)**: `79%`  
**Recall (Survived)**: `74%`  
**F1-Score (Survived)**: `76%`

---

## 🧠 What I Learned

- How to clean and preprocess real-world messy data
- Label encoding of categorical variables
- Basic EDA and survival rate visualization
- Training and evaluating a logistic regression model
- Reading and interpreting confusion matrix and classification metrics

---

## 🚀 How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Machine-Learning.git
cd Machine-Learning/Day2_Titanic_Survival
```

### 2. Activate Virtual Environment

```bash
# Windows
.\venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

### 3. Run Jupyter Notebook

```bash
jupyter notebook
```

Open `Day_2_Titanic_Logistic_Regression.ipynb` and run all cells.

---
