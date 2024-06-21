# Cryptocurrency Clustering Analysis

This project performs clustering analysis on a cryptocurrency dataset using K-Means clustering, both with and without Principal Component Analysis (PCA) for dimensionality reduction. The aim is to identify the impact of using fewer features on the clustering results.

## Dataset

The dataset used for this analysis is `crypto_market_data.csv`, which contains various features related to different cryptocurrencies. Ensure this file is placed in a `Resources` folder in the same directory as your script.

## Steps in the Analysis

1. **Import Libraries and Load Data**
   - Import the required libraries and load the cryptocurrency dataset into a Pandas DataFrame.

2. **Generate Summary Statistics and Initial Plot**
   - Generate summary statistics for the dataset to understand the distribution of data.
   - Plot the data to visualize trends and patterns.

3. **Prepare the Data**
   - Standardize the data using `StandardScaler` to ensure all features contribute equally to the clustering process.
   - Create a DataFrame with the scaled data and set the appropriate index.

4. **Find the Best Value for k Using the Original Data**
   - Create a list of k-values (from 1 to 11) to test different numbers of clusters.
   - Use a for loop to compute the inertia for each k-value and store the results.
   - Plot the Elbow curve to visually identify the optimal number of clusters.

5. **Cluster Cryptocurrencies with K-Means Using the Original Data**
   - Initialize and fit a K-Means model using the optimal k-value.
   - Predict the cluster labels for each cryptocurrency.
   - Add the predicted cluster labels to the DataFrame and create a scatter plot to visualize the clusters.

6. **Optimize Clusters with Principal Component Analysis (PCA)**
   - Perform PCA to reduce the dataset to three principal components.
   - Retrieve the explained variance to determine how much information can be attributed to each principal component.
   - Create a new DataFrame with the PCA data and find the best value for k using the PCA data.
   - Plot the Elbow curve for the PCA data.

7. **Cluster Cryptocurrencies with K-Means Using the PCA Data**
   - Initialize and fit a K-Means model using the optimal k-value for the PCA data.
   - Predict the cluster labels and add them to the PCA DataFrame.
   - Create a scatter plot to visualize the clusters using the PCA data.

8. **Visualize and Compare the Results**
   - Create composite plots to contrast the Elbow curves and the clusters obtained with and without PCA optimization.
   - Analyze the impact of using fewer features on the clustering results.

## Conclusion

By comparing the clustering results with and without PCA, you can determine the impact of dimensionality reduction on the clustering process. PCA simplifies the data, makes the clustering process faster, and can sometimes yield more distinct clusters, all while retaining most of the important information from the original dataset.
