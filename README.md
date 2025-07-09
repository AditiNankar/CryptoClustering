# CryptoClustering: Unsupervised Learning on Cryptocurrency Data

## 📖 Overview

This project uses **unsupervised machine learning**—specifically **K-Means Clustering** and **Principal Component Analysis (PCA)**—to group cryptocurrencies based on their short-term price movements.

The objective is to analyze whether **24-hour** and **7-day** price changes can reliably indicate different groups of cryptocurrencies, using clustering algorithms. This approach can help in identifying patterns or behaviors in the crypto market, useful for investors and analysts alike.

---

## 📊 Key Objectives

- Normalize cryptocurrency market data.
- Use the **Elbow Method** to determine the optimal number of clusters (k).
- Visualize K-Means clustering results using:
  - The **original scaled features**
  - The **PCA-reduced components**
- Compare clustering performance with and without dimensionality reduction.
- Evaluate the impact of reduced feature space on clustering behavior.
---

## 🧠 Tools & Libraries

- Python
- Pandas
- Scikit-learn
- HVPlot (interactive visualization)
- NumPy
- Matplotlib / Seaborn (optional)
- Jupyter Notebook

---

## 🛠️ Steps & Methodology

### 1. Load and Explore Data
- Dataset: `crypto_market_data.csv`
- Summarized, explored, and visualized price change data for cryptocurrencies.

### 2. Normalize the Data
- Used `StandardScaler` from Scikit-learn to standardize features.
- Created a scaled DataFrame indexed by `coin_id`.

### 3. Find Optimal k (Elbow Method)
- Applied KMeans with k = 1 to 11.
- Plotted **inertia** vs. k to find the “elbow point.”

### 4. Cluster Using Scaled Data
- Fitted KMeans to scaled data.
- Created a **scatter plot** of `price_change_percentage_24h` vs `price_change_percentage_7d` with color-coded clusters.

### 5. PCA for Dimensionality Reduction
- Reduced data from n-features to 3 principal components.
- Examined **explained variance**.

### 6. Re-cluster Using PCA Data
- Applied the Elbow Method again.
- Fitted KMeans to PCA data and visualized clusters using PC1 and PC2.

### 7. Comparison
- Created **composite plots** of elbow curves and clustering results before vs after PCA.
- Discussed trade-offs of reduced dimensionality.

---

## ❓ Insights

- **Best k** was found using the Elbow Method for both scaled and PCA data.
- PCA reduced data dimensionality while preserving variance (>95% in 3 components).
- Results showed **clear clusters** in both cases, but PCA helped in **faster computation** and simpler visualization.
- Using fewer features had **minimal impact** on clustering quality but improved interpretability.

---

## 🚀 How to Run

1. Clone the repository:
git clone https://github.com/yourusername/CryptoClustering.git
cd CryptoClustering
2. Open in jupyter notebook
3. Follow notebook cells to run preprocessing, clustering, and visualization
---

## 👩‍💻 Author

Aditi Nankar
