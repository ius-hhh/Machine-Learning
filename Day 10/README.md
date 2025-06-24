# 🎬 Day 10 – Movie Recommendation System

Welcome to Day 10 of the **"30 Days, 30 Machine Learning Projects"** challenge.  
Today, we build a **movie recommendation system** using **collaborative filtering** and **cosine similarity** with the MovieLens dataset.

---

## 📊 Dataset

The MovieLens dataset contains:
- Movie metadata (`movies.csv`) with movie IDs, titles, and genres
- User ratings (`ratings.csv`) with user IDs, movie IDs, ratings, and timestamps

---

## 🧠 Concepts Covered

- Collaborative Filtering (item-item)
- Cosine Similarity to measure movie similarity
- Data transformation with pivot tables
- Handling missing values by filling NaNs
- Building a recommendation function

---

## 🛠️ Tools & Libraries Used

- Python
- Pandas
- NumPy
- Scikit-learn (cosine_similarity)

---

## 📌 Objective

Build an item-based collaborative filtering movie recommender system that suggests similar movies based on user ratings.

---

## 📈 Project Summary

- Load and merge user ratings with movie metadata
- Create a user-movie ratings matrix (users as rows, movies as columns)
- Normalize the matrix by filling missing ratings with zeros and transpose to have movies as rows
- Compute cosine similarity between movies
- Build a function to recommend the top-N similar movies given a movie title

---

## ✅ Evaluation

- The recommender suggests movies similar to a given movie title based on user rating patterns
- Example: For "Toy Story (1995)", the top recommended movies include "Toy Story 2 (1999)", "Jurassic Park (1993)", and "Independence Day (1996)"

---

## 📊 Sample Usage

```python
recommend_movies("Toy Story (1995)")
