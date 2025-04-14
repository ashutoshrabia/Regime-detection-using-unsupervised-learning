# 📈 Market Regime Detection via Unsupervised Learning

This project identifies and analyzes distinct **market regimes** using unsupervised machine learning techniques on high-frequency order book and trade data. It was developed as part of an academic assignment and showcases full-cycle data preprocessing, feature engineering, clustering, and visualization.

---

## 🔍 Objective

The goal is to segment the market into interpretable regimes based on:
- **Price behavior** (Trending vs. Mean-Reverting)
- **Volatility** (High vs. Low)
- **Liquidity** (Liquid vs. Illiquid)

---

## 📁 Dataset

- **`depth20/`** — Contains order book snapshots (Top 20 bid/ask levels).
- **`aggTrade/`** — Contains aggregated trade data.
- Each file is resampled to **1-second intervals** and aligned by timestamp.

---

## ⚙️ Methods Used

- **Feature Engineering**: Bid-ask spread, microprice, imbalance, cumulative depth, returns, volatility.
- **Normalization**: `StandardScaler`
- **Dimensionality Reduction**: `PCA` for visualization
- **Clustering Algorithms**:
  - `KMeans`
  - `Gaussian Mixture Models (GMM)`
  - `BIRCH` (Best performing model)
- **Evaluation Metrics**: Silhouette Score, Calinski-Harabasz Index, Davies-Bouldin Score

---

## 📌 Highlights

-  Identified **7 unique market regimes**
-  Assigned descriptive names like _"Volatile & Illiquid"_, _"Trending & Stable"_
-  Analyzed **regime transition dynamics** using Markov-style matrices
-  Visualized regime shifts with time-series overlays and 2D projections (PCA/t-SNE)

---

## 📜 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.


