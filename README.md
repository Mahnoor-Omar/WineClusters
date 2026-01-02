# WineClusters
# 🍷 Wine Dataset Clustering

## 📌 Project Overview

This project demonstrates **unsupervised learning** using clustering techniques on the **Wine dataset** from scikit-learn. The goal is to explore natural groupings in the data, compare **K-Means** and **Agglomerative (Hierarchical) Clustering**, and analyze the impact of **feature dimensionality** on clustering performance.

The project includes:

* Data exploration and visualization
* Feature scaling
* Clustering using K-Means and Agglomerative methods
* Comparison of results with 2 features vs all 13 features
* PCA visualization for high-dimensional data

---

## 📊 Dataset Description

* **Samples:** 178
* **Features:** 13 (numerical)
* **Classes:** 3 wine types (used only for evaluation)

### Feature Names

* Alcohol
* Malic acid
* Ash
* Alcalinity of ash
* Magnesium
* Total phenols
* Flavanoids
* Nonflavanoid phenols
* Proanthocyanins
* Color intensity
* Hue
* OD280/OD315 of diluted wines
* Proline

---

## ⚙️ Data Preprocessing

1. **Feature Selection**

   * Initial experiments used the first 2 features: **Alcohol** and **Malic acid**
   * All 13 features were later used for full-dimensional clustering

2. **Feature Scaling**

   * Applied **StandardScaler** to normalize features (zero mean, unit variance)
   * Scaling ensures fair contribution of each feature to distance-based clustering

---

## 📈 Exploratory Visualization

* **2D Scatter Plot:** Alcohol vs Malic acid
* Observations:

  * Clusters overlap
  * Clear separation not visible
  * Indicates the need for higher-dimensional analysis

---

## 🤖 Clustering Methods

### 1️⃣ K-Means Clustering

* **Clusters (k):** 3
* **Random Seed:** 42
* **Observations (2 features):**

  * Formed three clusters with some overlap
  * Spherical cluster shapes
* **Observations (13 features):**

  * Clearer cluster separation
  * PCA shows well-defined clusters

### 2️⃣ Agglomerative Clustering

* **Clusters:** 3
* **Linkage:** Ward
* **Observations (2 features):**

  * Irregular cluster shapes
  * Boundaries differ from K-Means
* **Observations (13 features):**

  * Revealed meaningful hierarchical relationships
  * PCA visualization confirms better separation

---

## 🔎 PCA Visualization

* Applied **PCA** to reduce 13-dimensional data to 2D for visualization
* Observations:

  * Clusters become distinct
  * High-dimensional information is essential for effective clustering

---

## 📊 Comparison Summary

### Feature Dimensionality

| Criteria        | 2 Features  | 13 Features            |
| --------------- | ----------- | ---------------------- |
| Cluster Clarity | Weak        | Strong                 |
| Separation      | Overlapping | Clear                  |
| Visualization   | Limited     | Much better (with PCA) |
| Dimensionality  | Too low     | Sufficient             |

### Algorithm Comparison

| Aspect           | K-Means        | Agglomerative       |
| ---------------- | -------------- | ------------------- |
| Centroids        | Yes            | No                  |
| Cluster Shape    | Spherical      | Hierarchical        |
| Speed            | Fast           | Slower              |
| Interpretability | Easy           | Harder              |
| Best Use         | Large datasets | Exploring structure |

---

## ✅ Conclusion

* Clustering depends strongly on **feature selection** and **dimensionality**
* Using only two features gives limited insight with overlapping clusters
* Using all 13 features provides strong, meaningful separation
* **K-Means:** Efficient and clear centroid-based clusters
* **Agglomerative:** Reveals hierarchical structure
* **PCA:** Confirms that high-dimensional features are critical for uncovering natural groupings

---

## 📁 Repository Contents

* `notebook.ipynb` — Complete implementation and visualizations
* `README.md` — Project documentation

---

## 🧠 Skills Demonstrated

* Unsupervised learning & clustering
* K-Means and Agglomerative Clustering
* Feature scaling and dimensionality reduction
* Data visualization using scatter plots and PCA
* Comparative analysis of clustering algorithms

