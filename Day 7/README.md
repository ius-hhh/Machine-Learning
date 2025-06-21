# 🧪 Day 7 - Customer Segmentation with K-Means Clustering

Welcome to Day 7 of the **"30 Days, 30 Machine Learning Projects"** challenge.  
Today’s project focuses on **unsupervised learning** using **K-Means Clustering** to group customers based on their annual income and spending score.

---

## 📌 Objective

To segment customers into clusters based on similar purchasing behavior, allowing businesses to:
- Target specific customer groups
- Personalize marketing strategies
- Understand customer types (e.g., low-income low spenders, high-income high spenders)

---

## 📊 Dataset Description

We use the **Mall Customer Segmentation Dataset** which includes:

| Column        | Description                          |
|---------------|--------------------------------------|
| `CustomerID`  | Unique customer ID                   |
| `Gender`      | Male or Female                       |
| `Age`         | Age of the customer                  |
| `Annual Income (k$)` | Yearly income in thousands USD |
| `Spending Score (1-100)` | Score assigned by the mall based on customer behavior and spending nature |

---

## 🧠 Concepts Covered

- Exploratory Data Analysis (EDA)
- Feature Scaling (Standardization)
- Elbow Method for optimal number of clusters
- K-Means Clustering
- Cluster visualization using 2D plots
- Business insights from clustering results

---

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## 🚀 Steps

1. Load and explore the dataset.  
2. Visualize data distributions and relationships.  
3. Select features for clustering (`Annual Income` and `Spending Score`).  
4. Scale features to standardize ranges.  
5. Use the Elbow Method to find optimal number of clusters (K = 5).  
6. Train K-Means with optimal K and assign clusters.  
7. Visualize clusters and cluster centers.  
8. Interpret clusters and extract business insights.

---

## 🎯 Observing the Elbow

- Big drops occur from **K = 1 to K = 3**, and then a little more from **K = 3 to K = 5**.  
- After **K = 5**, the WCSS drops become much smaller, indicating **diminishing returns**.  
- So, the **“elbow point”** appears at **K = 5**, where:  
  - The **WCSS drop slows down noticeably**  
  - **Additional clusters don’t significantly improve** the compactness of the clusters

---

## 🖼️ Cluster Visualization and Interpretation

- Customers are grouped into 5 clusters based on income and spending behavior.  
- Each cluster represents distinct customer types:  
  - Low income & low spending  
  - High income & high spending  
  - Low income & high spending  
  - Medium income & medium spending  
  - Other varied behaviors  
- Cluster centers are marked with black “X” on the plot.  
- These insights help businesses **target marketing, product recommendations, and customer retention** strategies more effectively.

---

## 📈 Future Enhancements

- Include more features such as **Age** and **Gender** to get richer clusters.  
- Experiment with other clustering algorithms like **DBSCAN** or **Hierarchical Clustering**.  
- Use **PCA** to reduce dimensionality for higher feature sets.

---

Happy clustering! 🚀
