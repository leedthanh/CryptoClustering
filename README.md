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



