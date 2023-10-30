# CryptoClustering

USE Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.


# Prepare the Data

Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

# Find the Best Value for k Using the Original Scaled DataFrame

Use the elbow method to find the best value for k which is 3

# Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Initialize the K-means model with the best value for k.
Fit the K-means model using the original scaled DataFrame.
Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
Set the x-axis as "PC1" and the y-axis as "PC2".
Color the graph points with the labels found using K-means.
Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

# Optimize Clusters with Principal Component Analysis
Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
Retrieve the explained variance to determine how much information can be attributed to each principal component

# Find the Best Value for k Using the PCA Data
Use the elbow method on the PCA data to find the best value for k.
after getting the line chart the best value for K using PCA data is 4

# Cluster Cryptocurrencies with K-means Using the PCA Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

Initialize the K-means model with the best value for k.
Fit the K-means model using the PCA data.
Predict the clusters to group the cryptocurrencies using the PCA data.
Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
Create a scatter plot using hvPlot as follows:
Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
Color the graph points with the labels found using K-means.
Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
The impact of using fewer features to cluster the data using K-Means? is that the scaled dataset has overlap.  
However after PCA the dataset has no overlap and clearly show 3 clusters in the dataset.  



