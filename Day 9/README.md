# Day 9: Loan Default Prediction

## Project Overview
In this project, we predict whether a loan applicant will default or not using a real-world loan dataset.  
This is an imbalanced binary classification problem, common in banking and fintech.

---

## Objectives
- Understand and handle imbalanced data.
- Perform feature engineering and preprocessing.
- Train a Random Forest classifier using class weighting and SMOTE.
- Tune classification threshold to balance recall and precision.
- Evaluate model with metrics like ROC AUC, confusion matrix, and classification report.

---

## Steps Performed

### 1. Data Loading & Preprocessing
- Loaded dataset and identified categorical features.
- Encoded categorical variables using Label Encoding.
- Split data into train (80%) and test (20%) sets with stratification to maintain class distribution.

### 2. Handling Imbalanced Data
- Used `class_weight='balanced'` in Random Forest to address imbalance.
- Trained model and evaluated — recall for minority class was low (~3%).

### 3. Improving Model with SMOTE
- Applied SMOTE to generate synthetic minority samples only on training data.
- Trained a new Random Forest on balanced data.
- Improved recall to ~23%, with trade-off of more false positives and slightly lower accuracy.

### 4. Threshold Tuning
- Lowered classification threshold from 0.5 to 0.3 to improve recall further.
- At threshold 0.3, recall improved to 55%, with precision ~21% and accuracy ~71%.
- Tested multiple thresholds (0.1, 0.2, 0.3, 0.4, 0.5) to find best tradeoff.

### 5. Evaluation Metrics Used
- **Confusion Matrix:** Shows true positives, false positives, true negatives, false negatives.
- **Classification Report:** Precision, recall, and F1-score per class.
- **ROC AUC Score:** Measures model’s ability to rank positive cases higher than negatives.
- **ROC Curve:** Visualizes tradeoff between true positive rate and false positive rate.

---

## Key Learnings
- Class imbalance requires special handling (class weights, SMOTE).
- Precision-recall tradeoff can be tuned using classification thresholds.
- Higher recall means catching more defaults but increases false alarms.
- ROC AUC is threshold-independent and useful for model comparison.

---

## Next Steps
- Explore hyperparameter tuning (GridSearchCV) for better model performance.
- Try other models or cost-sensitive learning approaches.
- Further feature engineering and data cleaning.

---

Feel free to ask questions or request code snippets for any step!
