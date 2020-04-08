# Cryptocurrency Analysis

## Overview

Using unsupervised machine learning to cluster different cryptocurrencies by market value, in order to present to stakeholders. 

Market value was evaluated  by trading price, total coins mined, and the total coins supply.

The goals for this project are to:
* Prepare the data for dimensions reduction with PCA and clustering using K-means.
* Reduce data dimensions using PCA algorithms from sklearn.
* Predict clusters using cryptocurrencies data using the K-means algorithm form sklearn.
* Create a 3D scatter plot and data table to present the results.

## Data Pre-Processing
Load data from a csv into a Pandas DataFrame for transformations.

### Transformation Steps
* Remove all cryptocurrencies that aren’t trading. 
* Remove all cryptocurrencies that don’t have an algorithm defined. 
* Remove all cryptocurrencies with at least one null value. 
* Remove all cryptocurrencies without coins mined.
* Store the names of all cryptocurrencies in a DataFramed called coins_name, use the crypto_df.index as the index for the new DataFrame.
* Remove columns not essential to the analysis.
* Create dummies variables for all of the text features, and store the resulting data in a DataFrame named X.
* Standardize the X DataFrame by using StandardScaler from sklearn.
* Pass the standardized DataFrame into a Principal Component Analysis (PCA) statistical algorithm to reduce the dimensions that are fed into the final clustering model.    

## Analysis
Using the standardized data the has been passed through the PCA algorithm, create a K-means clustering algorithm to complete the market value analysis. 

### Models Used 
Used the K-means clustering algorithm from sklearn to cluster the cryptocurrencies. 
* Create an elbow curve to find the best K value.
* Run the K-means clustering algorithm.
* Create a new DataFrame, called clustered_df, from the results that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class.

### Visualizing Results
Create a 3D scatter plot using Plotly Express that plots the results, clustered_df, and includes information in a hover pop-up for each point.
Create a table of the results with the following columns: CoinName, Algorithm, ProofType, TotalCoinSupply, TotalCoinsMined, and Class.
