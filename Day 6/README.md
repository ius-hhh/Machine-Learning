# 🗣️ Day 6 - Spam Email Detection with NLP

Welcome to Day 6 of the **"30 Days, 30 Machine Learning Projects"** challenge.  
In this project, we build a text classification model that detects whether an SMS message is **spam** or **ham (not spam)** using real-world text data and modern NLP techniques.

---

## 📌 Objective

To classify messages into `spam` or `ham` using:
- Natural Language Processing for text cleaning and feature extraction
- Logistic Regression for classification
- Oversampling to handle imbalanced datasets

---

## 📊 Dataset

We're using the **SMS Spam Collection Dataset** from UCI, containing 5,574 labeled SMS messages.

- Format:
  - `label`: `"spam"` or `"ham"`
  - `message`: SMS content as plain text

We loaded the dataset from this URL:
https://raw.githubusercontent.com/justmarkham/pycon-2016-tutorial/master/data/sms.tsv


---

## 🧠 Concepts Covered

- Text preprocessing:
  - Lowercasing
  - Removing punctuation
  - Removing stopwords
  - Stemming (using NLTK’s PorterStemmer)
- Feature extraction with **TF-IDF** (Term Frequency–Inverse Document Frequency)
- Splitting data into training/testing sets
- Handling **imbalanced datasets** using `RandomOverSampler` from `imbalanced-learn`
- Training with **Logistic Regression**
- Evaluating the model using:
  - Accuracy
  - Precision, Recall, F1-score
  - Confusion Matrix & Heatmap

---

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- NLTK (Natural Language Toolkit)
- Scikit-learn (sklearn)
- imbalanced-learn (`imblearn`)
- Seaborn and Matplotlib for visualization

---

## ⚖️ Handling Imbalanced Data

The dataset is imbalanced (far more ham messages than spam), which can mislead the model into favoring the majority class.

We handled this by:
- Using `RandomOverSampler` to duplicate spam samples in the training set
- Balancing class distribution before training

This significantly improved the **recall** and **F1-score** for spam classification.

---
