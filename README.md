# Cryptocurrencies Analysis

Unsupervised machine learning of Cryptocurrency data

## Overview

The project involves analysis of data from over 1000 cryptocurrencies for investment purposes. As we do not know what output we are looking for to classify patterns in the crypto data, unsupervised learning is a sensible approach. The data set was pre-processed to make it suitable for Principal Component Analysis (PCA). After this, the dimensions of the data were reduced using PCA, the cryptocurrencies grouped using K-means clustering, and the result of the analysis visualized.

### Purpose

This analysis could be used to help an investment bank create a grouped classification system for cryptocurrencies currently trading on the market and use this to present a new investment portfolio for its customers. 

## Resources

Tools and software: Python 3.7.9, Jupyter Notebook 6.1.4, pandas, hvplot, adn sklearn libraries, Visual Studio Code 1.54.3

Dataset: ["Crypto Data"](https://github.com/jkenning/Cryptocurrencies/blob/main/Resources/crypto_data.csv)

Analysis: ["Crypto Clustering"](https://github.com/jkenning/Cryptocurrencies/blob/main/crypto_clustering.ipynb)

## Summary of Results

First, the data was filtered to those cryptocurrencies currently being traded and that have a working algorithm. Null data and unneccesary fields were dropped from the data set. Variables were then created for text features and the data was standardized. 

![](https://github.com/jkenning/Cryptocurrencies/blob/main/Images/pcs_df.png)

Figure. 1 - Using PCA, the transformed data was reduced to three principle components. 

![](https://github.com/jkenning/Cryptocurrencies/blob/main/Images/elbow_curve.png)

Figure. 2 - The best value for 'k' was found to be about 4 using an Elbow curve.

![](https://github.com/jkenning/Cryptocurrencies/blob/main/Images/clustered_df.png)

Figure. 3 - The data was clustered using 4 clusteres and made to fit the model and concatenated with the original DataFrame.

![](https://github.com/jkenning/Cryptocurrencies/blob/main/Images/3D_scatter_w_clusters.png)

Figure. 4 - A 3D scatter plot allows us to visualize each of the three principal components and the clusters on one graph.

![](https://github.com/jkenning/Cryptocurrencies/blob/main/Images/tradeable_crypto_hvplot.png)

Figure. 5 - Resulting table showing all 532 tradeable cryptocurrencies, produced using hvplot. 

![](https://github.com/jkenning/Cryptocurrencies/blob/main/Images/plot_df.png)

Figure. 6 - Currency data was scaled and added to the clustered DataFrame to produce a new DataFrame

![](https://github.com/jkenning/Cryptocurrencies/blob/main/Images/TotalCoinsMinedVsTotalCoinSupply_scatter.png)

Figure. 7 - The new DataFrame was used to plot Total Coins Mined vs. Total Coin Supply, using hvplot. 