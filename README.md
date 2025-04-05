# CryptoClustering

## Overview

In this challenge, I used **unsupervised machine learning techniques** to analyze and cluster cryptocurrency data. The objective was to explore whether cryptocurrencies are influenced by 24-hour or 7-day price changes. All analysis was performed using **Google Colab**.

---

## Objectives

- Normalize cryptocurrency data using `StandardScaler`
- Apply the **K-Means clustering algorithm** to identify patterns in price change behavior
- Visualize clustering results using `hvPlot`
- Reduce dimensionality with **Principal Component Analysis (PCA)**
- Compare cluster performance before and after PCA
- Assess the effect of using fewer features on K-Means clustering outcomes

---

## Data

- **File Used:** `crypto_market_data.csv`  
- Contains various cryptocurrencies with percentage price changes over 24 hours and 7 days.

---

## Tools & Technologies

- **Platform:** Google Colab
- **Languages:** Python
- **Libraries:**  
  - `pandas` for data handling  
  - `scikit-learn` for scaling, clustering, and PCA  
  - `matplotlib` and `hvplot.pandas` for data visualization

---

## Workflow

### 1. Load & Explore Data
- Loaded the dataset into a Pandas DataFrame in Google Colab.
- Inspected summary statistics and initial trends in the data.

### 2. Preprocessing
- Normalized numerical features using `StandardScaler`.
- Re-indexed the scaled DataFrame using the `"coin_id"` column from the original dataset.

### 3. K-Means Clustering (Original Scaled Data)
- Used the **Elbow Method** (k = 1 to 11) to find the optimal number of clusters.
- Plotted the Elbow curve to determine the best `k`.
- Fit and predicted K-Means clusters.
- Created a scatter plot using `hvPlot`, with:
  - X-axis: `price_change_percentage_24h`
  - Y-axis: `price_change_percentage_7d`
  - Clusters visualized with color
  - Coin names shown on hover

### 4. PCA Dimensionality Reduction
- Reduced features to 3 principal components using PCA.
- Checked the **explained variance ratio** to determine how much information was retained.

### 5. K-Means Clustering (PCA Data)
- Re-ran the Elbow Method on PCA-transformed data.
- Compared the optimal `k` value from this run with the original data.
- Predicted clusters on PCA data.
- Visualized new clusters using the same scatter plot format.

---

## Conclusion

This analysis highlighted how **K-Means and PCA** can work together to uncover patterns in financial datasets. Using Google Colab provided a seamless, cloud-based platform to conduct this machine learning workflow with real-time visualization and reproducibility.
