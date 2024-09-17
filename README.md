# CryptoClustering

## Summary
This exercise demonstrates the use of K-Means clustering for grouping cryptocurrencies based on market data, and compares the clustering performance with and without Principal Component Analysis (PCA) optimization.

### 1. Data Preprocessing
- The cryptocurrency market data was loaded into a Pandas DataFrame, and StandardScaler was applied to normalize the data.
- Basic statistical summaries and visualizations were performed to understand the distribution of the data.

### 2. K-Means Clustering (Original Data)
- The `KMeans` algorithm was applied to the scaled data using a range of cluster values (k=1 to 11).
- An Elbow Curve was plotted to visually determine the optimal value for *k*, which was found to be **4**.
- A K-Means model was then fitted to the scaled data using *k=4*, and cluster predictions were generated for each cryptocurrency.
- A scatter plot was created to visualize the clusters based on price changes over 24 hours and 7 days.

### 3. PCA Dimensionality Reduction
- Principal Component Analysis (PCA) was applied to reduce the data to three principal components (PC1, PC2, PC3).
- An Elbow Curve was plotted again using the PCA-reduced data to determine the optimal number of clusters, which also yielded *k=4*.
- A K-Means model was fitted to the PCA-reduced data, and cluster predictions were made.

### 4. Comparison of Results
- A composite plot was created to compare the Elbow curves for the original and PCA-reduced data, showing that the PCA data resulted in lower inertia values at each cluster count, indicating more compact clustering.
- Another composite plot was created to compare the scatter plots of clusters from the original data and PCA-reduced data. The PCA-reduced clusters were more compact, while the original clusters showed greater spread and differentiation.

### 5. Conclusion
- PCA optimization allows for more efficient clustering by reducing data dimensionality, but this may result in the loss of some nuanced differences in the data. The choice between using PCA or the original data depends on the trade-off between clustering efficiency and data granularity.

## Code Source
- Learning Assistant
- GitHub location: https://github.com/jeffjunohkim/CryptoClustering.git
