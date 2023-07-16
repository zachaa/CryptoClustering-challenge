# Challenge 19 - Unsupervised Learning

This challenge demonstrates the usage of unsupervised learning with k-means clustering.

Using the provided data on [Crypto Currencies](Resources/crypto_market_data.csv), containing 7 features, I explored clustering the data. The analysis, plots, and code can be found in [`Crypto_Clustering.ipynb`](Crypto_Clustering.ipynb)
- First, I normalized the data using `StandardScaler()` from `scikit-learn`. 
- Using this data, I then used the elbow method to find the best value for `k`.
    - From the elbow method line chart, I determined that the best value for `k` is 4.
- I then fit the data with a k-means model to cluster the different crypto currencies into 4 groups then plotted the groups in a scatter plot.
- I then used Principal Component Analysis (PCA) to reduce the features down to 3.
    - The explained variance of these three features was 89%.
- I repeated the process of using the elbow method and fitting the data with a k-means model.
    - Using PCA and the elbow method, the best value of `k` was again determined to be 4, leading to the conclusion that PCA with 3 features was appropriate for this data set.
- Finally, I compared the the elbow curves and the scatter plots before and after PCA. Images are shown below.
    - Overall, using PCA made the outliers more obvious, however, it does not make clusters 0 and 3 appear more distinct, at least with the two dimensions shown.

### Plots
![Elbow curve plots comparing the original data with the PCA data](Images/elbow_plot.png)

![Scatter plot of 24 hours and 7 days features, colored by k-means cluster.](Images/clusters_plot.png)

![Scatter plot of Principal Components 1 and 2, colored by k-means cluster.](Images/clusters_PCA_plot.png)