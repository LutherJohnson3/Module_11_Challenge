**Prepare the Data** 

1. Used the *StandardScaler()* module from *scikit-learn* to normalize the data from the CSV file.
2. Created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
    * The first five rows of the scaled DataFrame should appear as follows:

**Find the Best Value for k Using the Original Scaled DataFrame**

Use the elbow method to find the best value for *k* by completing the following steps:

1. Created a list with the number of k values from 1 to 11.
2. Created an empty list to store the inertia values.
3. Created a *for* loop to compute the inertia with each possible value of k.
4. Created a dictionary with the data to plot the elbow curve.
5. Plotted a line chart with all the inertia values computed with the different values of *k* to visually identify the optimal value for *k*.

**Cluster Cryptocurrencies with K-Means Using the Original Scaled Data**

Use the following steps to cluster the cryptocurrencies for the best value for *k* on the original scaled data:

1. Initialized the K-means model with the best value for k.
2. Created an instance of K-means, define the number of clusters based on the best value of k, and then fit the model using the original scaled DataFrame.
3. Predicted the clusters to group the cryptocurrencies using the original scaled DataFrame.
4. Created a copy of the original data and add a new column with the predicted clusters.
5. Created a scatterplot using pandas’ *plot* as follows:
    * Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".

**Optimize Clusters with Principal Component Analysis**

1. Using the original scaled DataFrame, performed a PCA and reduce the features to three principal components.
2. Retrieved the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
    * What is the total explained variance of the three principal components?
3. Created a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

**Find the Best Value for k Using the PCA Data**

Use the elbow method on the PCA data to find the best value for k using the following steps:

1. Created a list with the number of k-values from 1 to 11.
2. Created an empty list to store the inertia values.
3. Created a *for* loop to compute the inertia with each possible value of *k*.
4. Created a dictionary with the data to plot the elbow curve.
5. Plotted a line chart with all the inertia values computed with the different values of *k* to visually identify the optimal value for *k*.

**Cluster Cryptocurrencies with K-Means Using the PCA Data**

Use the following steps to cluster the cryptocurrencies for the best value for *k* on the PCA data:

1. Initialize the K-means model with the best value for *k*.
2. Create an instance of K-means, define the number of clusters based on the best value of *k*, and then fit the model using the PCA data.
3. Predict the clusters to group the cryptocurrencies using the PCA data.
4. Created a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
5. Created a scatterplot using pandas’ *plot* as follows:
    *Set the x-axis as "PC1" and the y-axis as "PC2".


