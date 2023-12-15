# Cryptocurrencies

# Project consisted of performing unsupervised machine learning on a Crytocurrency dataset.

## 4 deliverables:

    * Deliverable 1: Preprocessing the data for principal component analysis (PCA).
    * Deliverable 2: Reducing feature data dimensions using PCA.
    * Deliverable 3: Clustering cryptocurrencies using K-means.
    * Deliverable 4: Visualizing crytocurrencies results.

### Deliverable 1:

*   Read in crypto_data.csv and build DataFrame named "crypto_df"
*   Keep only rows where the "IsTrading" column is "True" in DataFrame.
*   Keep only rows that have values in the "Algorithm" column in DataFrame.
*   Drop the "IsTrading" column from DataFrame. 
*   Check for "null values (NaN) in rows in DataFrame.
*   Drop rows containing NaN values in DataFrame.
*   Keep only rows where the values for "TotalCoinsMined" are greater than 0 in DataFrame.
*   Make a new DataFrame called "cryptonames_df" for the "CoinName" column.
*   Drop "CoinName" column name from "cryto_df" DataFrame.
*   Run get_dummies() to create variables from text features in DataFrame.
*   Standardize the feature data values using StandardScaler() & apply scaler.


### Deliverable 2:

*  Run PCA on scaled data to reduce dimensions scaled (X) DataFrame to produce three principal components.
*  Output the principal component values PC1, PC2, & PC3 into "pcs_df" DataFrame.

### Deliverable 3:

*  Create an instance of the K-means algorithm.
*  Build an elbow curve by applying KMeans() method to "pcd_df" to determine the number of clusters needed for analysis.
*  Elbow curve shows that 4 clusters are required.
*  Run KMeans() method to train data & predict class for each cryptocurrency.
*  Create "clustered_df" by contatenating "crypto_df" and "pcs_df" DataFrames.
*  Add the "CoinName" column that holds the crytocurrency names to the "clustered_df" DataFrame.
*  Add the "Class" column to the "clustered_df" DataFrame using "model.labels_"
*  Print "clustered_df"

### Deliverable 4:

*  Create 3D scatter plot of clusters by applying scatter_3D() function to "clustered_df" DataFrame.
*  Create table using hvplot.table() function and "clustered_df" input. Note that class values in challenge 18 goby are not consistent with other outputs. askBCS confirmed that my code is correct and my output is consistent.
*  Run MinMaxScaler() method to scale "TotalCoinSupply" and "TotalCoinsMined" columns.
*  Create DataFrame "plot_df" using scaled "TotalCoinSupply" and "TotalCoinsMined" column values.
*  Add "CoinName" column from "clustered_df" DataFrame to "plot_df" DataFrame.
*  Add "Class" column from "clustered_df" DataFrame to "plot_df" DataFrame.
*  Output "plot_df" table.
*  Output 2D scatter plot of "plot_df" using hvplot.scatter() function.

## NOTE: I think that the class values in the GoBy for Mod 18 Challenge are WRONG for the hvplot.table()!!

