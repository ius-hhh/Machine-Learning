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

- **Source**: [Kaggle Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic)
- **Files**:
  - `train.csv` — training dataset with labels (`Survived`)
  - `test.csv` — test dataset (unlabeled)
  - `submission.csv` — output file for predictions on the test set

---

## 🔧 Features Used

| Feature     | Description                       |
|-------------|-----------------------------------|
| Pclass      | Passenger class (1st, 2nd, 3rd)   |
| Sex         | Gender (encoded as 0/1)           |
| Age         | Age of passenger (filled with median) |
| SibSp       | Number of siblings/spouses aboard |
| Parch       | Number of parents/children aboard |
| Fare        | Fare paid                         |
| Embarked    | Port of embarkation (encoded)     |

---

## 🧼 Preprocessing Steps

- Dropped less useful or sparse columns: `Cabin`, `Ticket`, `Name`, `PassengerId`
- Filled missing values:
  - `Age`: median
  - `Embarked`: mode
- Encoded categorical features (`Sex`, `Embarked`) using `LabelEncoder`

---

## 📈 Model Used

- **Logistic Regression**
  - `max_iter = 1000` to ensure convergence
  - Evaluated using:
    - Accuracy
    - Confusion Matrix
    - Precision / Recall / F1 Score

---

## ✅ Evaluation Results

| Metric       | Score |
|--------------|-------|
| Accuracy     | ~81%  |
| Precision    | Good  |
| Recall       | Good  |
| Confusion Matrix | Clean separation |

---

## 📤 Submission

- `submission.csv` generated using model predictions on `test.csv`
- Format:

```csv
PassengerId,Survived
892,0
893,1
...