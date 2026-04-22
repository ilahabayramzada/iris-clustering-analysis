# 🌸 Iris Clustering Analysis

An unsupervised machine learning project that applies **K-Means** and **Hierarchical Clustering** on the classic Iris dataset. Results are visualized in 2D using **PCA** and compared against the real species labels.

---

## 📌 Project Overview

This project demonstrates two popular clustering algorithms on the Iris dataset and evaluates how well they can group flowers without using any labels — purely based on their measurements.

**Dataset:** Iris.csv (150 samples, 4 features, 3 species)  
**Language:** Python  
**Type:** Unsupervised Learning

---

## 📁 Project Structure

```
iris-clustering-analysis/
│
├── iris_clustering.py   # Main script — clustering, PCA, visualization
├── Iris.csv             # Dataset (150 samples: Setosa, Versicolor, Virginica)
└── README.md
```

---

## 🌿 Dataset

The Iris dataset contains 150 flower samples across 3 species:

| Feature | Description |
|---|---|
| `SepalLengthCm` | Sepal length in cm |
| `SepalWidthCm` | Sepal width in cm |
| `PetalLengthCm` | Petal length in cm |
| `PetalWidthCm` | Petal width in cm |
| `Species` | Target label (Setosa / Versicolor / Virginica) |

> `Id` column is dropped as it carries no useful information for modeling.

---

## ⚙️ Methodology

### 1. Preprocessing
- `Id` column removed
- Features scaled using `StandardScaler`
- `LabelEncoder` applied to species for reference comparison

### 2. K-Means Clustering
- `n_clusters=3`, `random_state=42`
- Fit on scaled features
- Cluster labels stored in `kmeans_cluster`

### 3. Hierarchical Clustering
- Linkage method: **Ward**
- Dendrogram plotted for visual inspection
- `fcluster` used to extract 3 flat clusters

### 4. PCA Visualization
- `PCA(n_components=2)` applied for 2D projection
- Both clustering results plotted on the same PCA axes for comparison

---

## 📊 Outputs

| Output | Description |
|---|---|
| K-Means scatter plot | PCA projection colored by K-Means cluster |
| Dendrogram | Hierarchical linkage tree |
| Hierarchical scatter plot | PCA projection colored by hierarchical cluster |
| Crosstab (K-Means) | Cluster vs real species overlap |
| Crosstab (Hierarchical) | Cluster vs real species overlap |

---

## 🛠️ Tech Stack

| Library | Usage |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical operations |
| `scikit-learn` | KMeans, PCA, StandardScaler, LabelEncoder |
| `scipy` | Hierarchical clustering, dendrogram |
| `matplotlib` | Plotting |
| `seaborn` | Scatter plot visualization |

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/iris-clustering-analysis.git
cd iris-clustering-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn scipy

# 3. Run the script
python iris_clustering.py
```

---

## 👤 Author

Built as a machine learning portfolio project to demonstrate unsupervised learning techniques.
