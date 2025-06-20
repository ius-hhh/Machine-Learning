# 🗣️ Day 6 - Spam Email Detection with NLP

Welcome to Day 6 of the **"30 Days, 30 Machine Learning Projects"** challenge.  
In this project, we’ll build a text classification model that detects whether an email (or SMS) is **spam** or **ham (not spam)** using real-world text data.

---

## 📌 Objective

To classify messages into `spam` or `ham` using NLP techniques and machine learning.

---

## 📊 Dataset

We'll use the **SMS Spam Collection Dataset** from UCI, which contains 5,574 labeled text messages (spam/ham).

- Format:
  - `label`: "spam" or "ham"
  - `message`: the SMS/email content

---

## 🧠 Concepts Covered

- Text preprocessing (lowercasing, punctuation removal, stopwords)
- Tokenization and vectorization using **TF-IDF**
- Logistic Regression classifier
- Model evaluation with confusion matrix, accuracy, and precision-recall

---

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- Scikit-learn
- NLTK (for stopwords and text processing)

---

## 🚀 Future Enhancements

- Try Naive Bayes, SVM, or XGBoost
- Use word embeddings (Word2Vec, BERT)
- Apply deep learning with LSTM/CNN for better performance
