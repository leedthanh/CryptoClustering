# CryptoClustering

USE Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.


# Prepare the Data

Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

# Find the Best Value for k Using the Original Scaled DataFrame

Use the elbow method to find the best value for k which is 3
![elbow curve](https://github.com/leedthanh/CryptoClustering/assets/135544908/b437469e-20fd-4f9c-931d-ec11af480f71)


# Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Initialize the K-means model with the best value for k.
Fit the K-means model using the original scaled DataFrame.
Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
Set the x-axis as "PC1" and the y-axis as "PC2".
Color the graph points with the labels found using K-means.
Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
![scatter plot k3](https://github.com/leedthanh/CryptoClustering/assets/135544908/92b68df7-dbfe-46f8-933c-68fa479e2699)

# Optimize Clusters with Principal Component Analysis
Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
Retrieve the explained variance to determine how much information can be attributed to each principal component

# Find the Best Value for k Using the PCA Data
Use the elbow method on the PCA data to find the best value for k.
after getting the line chart the best value for K using PCA data is 4
![elbow curve pca](https://github.com/leedthanh/CryptoClustering/assets/135544908/95fac186-00fd-4143-b7a8-8f00ba27aec2)

# Cluster Cryptocurrencies with K-means Using the PCA Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
![scatter plot pca_](https://github.com/leedthanh/CryptoClustering/assets/135544908/6e6e54df-c0b9-4c02-97e1-b0604fb693ba)

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

![clusters withouth and with PCA](https://github.com/leedthanh/CryptoClustering/assets/135544908/aa558ce2-ec50-4cfb-ae1e-da412109b3d5)


![elbow cruve without and with pca_](https://github.com/leedthanh/CryptoClustering/assets/135544908/b9fc1ba5-417e-4835-9991-00ad0e3a7f41)


