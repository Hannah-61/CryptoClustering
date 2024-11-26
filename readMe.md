# CryptoClustering Project

## Overview

This project demonstrates the use of unsupervised machine learning techniques to cluster cryptocurrencies based on market data. By applying dimensionality reduction with Principal Component Analysis (PCA) and clustering with K-Means, the project explores whether cryptocurrencies can be grouped effectively based on their 24-hour and 7-day price changes.

## Goals

1. Identify the optimal number of clusters (`k`) for grouping cryptocurrencies using the Elbow Method.
2. Perform clustering on the original dataset and a PCA-transformed dataset.
3. Compare clustering results to evaluate the impact of dimensionality reduction.
4. Visualize the clustering results and interpret their significance.

---

## Files in the Repository

* `Crypto_Clustering.ipynb`: The main Jupyter Notebook containing the code for data preprocessing, PCA transformation, clustering, and visualizations.
* `crypto_market_data.csv`: The dataset containing cryptocurrency market data (e.g., 24-hour and 7-day price changes).
* `README.md`: This file explaining the project and its components.

---

## Steps in the Project

### 1. Data Preprocessing

* The cryptocurrency market data is loaded into a Pandas DataFrame.
* The data is scaled using `StandardScaler` to normalize the features for clustering.

### 2. Dimensionality Reduction with PCA

* PCA is applied to reduce the dataset to 3 principal components while retaining most of the variance.
* Explained variance for the PCA components is calculated to evaluate the effectiveness of dimensionality reduction.

### 3. Finding the Optimal Number of Clusters

* The Elbow Method is used to determine the best value of `k` for clustering.
* Inertia values are computed for `k` values ranging from 1 to 11.
* A line chart (Elbow Curve) is plotted to visualize the results and identify the "elbow" point.

### 4. Clustering with K-Means

* K-Means clustering is applied to both the original dataset and the PCA-transformed dataset.
* Cluster labels are added to the respective datasets.

### 5. Visualizing the Results

* Scatter plots are created to visualize the clusters for both datasets.
* The results are compared to analyze the impact of using PCA on clustering.

---

## Results

1. **Best Value of `k`:**
   * The Elbow Method identified the optimal value of `k` as  **4** .
2. **Cluster Visualization:**
   * Clusters are more distinct and easier to interpret after applying PCA.
3. **Impact of PCA:**
   * PCA reduced noise and dimensionality, improving cluster clarity and computational efficiency.

---

## Technologies Used

* **Python Libraries:**
  * `pandas` for data manipulation.
  * `matplotlib` and `hvplot` for visualizations.
  * `sklearn` for PCA and K-Means clustering.

---

## How to Run the Project

1. **Clone the Repository:**
2. **Install Required Libraries:**
   Make sure you have the following libraries installed:
   <pre class="!overflow-visible"><div class="contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative bg-token-sidebar-surface-primary dark:bg-gray-950"><div class="flex items-center text-token-text-secondary px-4 py-2 text-xs font-sans justify-between rounded-t-md h-9 bg-token-sidebar-surface-primary dark:bg-token-main-surface-secondary select-none">bash</div><div class="sticky top-9 md:top-[5.75rem]"><div class="absolute bottom-0 right-2 flex h-9 items-center"><div class="flex items-center rounded bg-token-sidebar-surface-primary px-2 font-sans text-xs text-token-text-secondary dark:bg-token-main-surface-secondary"><span class="" data-state="closed"><button class="flex gap-1 items-center select-none py-1"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="icon-sm"><path fill-rule="evenodd" clip-rule="evenodd" d="M7 5C7 3.34315 8.34315 2 10 2H19C20.6569 2 22 3.34315 22 5V14C22 15.6569 20.6569 17 19 17H17V19C17 20.6569 15.6569 22 14 22H5C3.34315 22 2 20.6569 2 19V10C2 8.34315 3.34315 7 5 7H7V5ZM9 7H14C15.6569 7 17 8.34315 17 10V15H19C19.5523 15 20 14.5523 20 14V5C20 4.44772 19.5523 4 19 4H10C9.44772 4 9 4.44772 9 5V7ZM5 9C4.44772 9 4 9.44772 4 10V19C4 19.5523 4.44772 20 5 20H14C14.5523 20 15 19.5523 15 19V10C15 9.44772 14.5523 9 14 9H5Z" fill="currentColor"></path></svg>Copy code</button></span></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="!whitespace-pre hljs language-bash">pip install pandas scikit-learn matplotlib hvplot
   </code></div></div></pre>
3. **Run the Jupyter Notebook:**
   Open the notebook in Jupyter and run the cells step by step:
   <pre class="!overflow-visible"><div class="contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative bg-token-sidebar-surface-primary dark:bg-gray-950"><div class="flex items-center text-token-text-secondary px-4 py-2 text-xs font-sans justify-between rounded-t-md h-9 bg-token-sidebar-surface-primary dark:bg-token-main-surface-secondary select-none">bash</div><div class="sticky top-9 md:top-[5.75rem]"><div class="absolute bottom-0 right-2 flex h-9 items-center"><div class="flex items-center rounded bg-token-sidebar-surface-primary px-2 font-sans text-xs text-token-text-secondary dark:bg-token-main-surface-secondary"><span class="" data-state="closed"><button class="flex gap-1 items-center select-none py-1"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="icon-sm"><path fill-rule="evenodd" clip-rule="evenodd" d="M7 5C7 3.34315 8.34315 2 10 2H19C20.6569 2 22 3.34315 22 5V14C22 15.6569 20.6569 17 19 17H17V19C17 20.6569 15.6569 22 14 22H5C3.34315 22 2 20.6569 2 19V10C2 8.34315 3.34315 7 5 7H7V5ZM9 7H14C15.6569 7 17 8.34315 17 10V15H19C19.5523 15 20 14.5523 20 14V5C20 4.44772 19.5523 4 19 4H10C9.44772 4 9 4.44772 9 5V7ZM5 9C4.44772 9 4 9.44772 4 10V19C4 19.5523 4.44772 20 5 20H14C14.5523 20 15 19.5523 15 19V10C15 9.44772 14.5523 9 14 9H5Z" fill="currentColor"></path></svg>Copy code</button></span></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="!whitespace-pre hljs language-bash">jupyter notebook Crypto_Clustering.ipynb
   </code></div></div></pre>

---

## Key Insights

* Dimensionality reduction with PCA simplifies clustering without losing critical information.
* The Elbow Method effectively identifies the optimal number of clusters (`k=4`).
* PCA improves clustering results by removing noise and irrelevant features.
