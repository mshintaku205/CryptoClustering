# CryptoClustering
Module 19 Challenge


## Project Description
Use Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Prepare the Data
- Use StandardScaler() module from scikit-learn to normalize the data from the CSV file resource
- Create a DataFrame with the scaled data


## Features
**Find the Best Value for k Using the Scaled DataFrame**<br>
- Code the elbow method algorithm to find the best value for k<br>
- Visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.

**Cluster Cryptocurrencies with K-means Using the Scaled DataFrame**<br>
- Initialize the K-means model with best value for k
- Fit the K-means model by using the scaled DataFrame
- Predict the clusters for grouping the cryptocurrencies by using the scaled DataFrame
- Review the resulting array of cluster values
- Create a copy of the scaled DataFrame, and then add a new column of the predicted clusters
- Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Color the graph points with the labels that was found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents. 

**Optimize Clusters with Principal Component Analysis**<br>
- Create a PCA model instance, and set n_components=3
- Use the PCA model to reduce the features to three principal components.
- Get the explained variance to determine how much information can be attributed to each principal component
- Create a new DataFrame from the scaled PCA data. Be sure to set the coin_id index from the original scaled DataFrame as the index for the new DataFrame. Review the first five rows of the DataFrame.

**Find the Best Value for k Using the PCA DataFrame**<br>
- Code the elbow method algorithm, and use the scaled PCA DataFrame to find the best value for k
- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k

**Cluster Cryptocurrencies with K-means Using the PCA DataFrame**<br>
- Initialize the K-means model with the best value for k
- Fit the K-means model by using the PCA data
- Predict the clusters for grouping the cryptocurrencies by using the PCA data
- Using hvPlot, create a scatter plot. Color the graph points with the labels that was found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents.
