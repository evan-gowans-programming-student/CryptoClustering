# CryptoClustering

Overview

This project applies K-Means clustering and Principal Component Analysis (PCA) to cryptocurrency market data to group similar cryptocurrencies based on their price change characteristics.

Files

Crypto_Clustering.ipynb - Jupyter Notebook containing the full analysis

crypto_market_data.csv - Dataset containing cryptocurrency market data

Instructions

Data Preparation

Load crypto_market_data.csv into a DataFrame.

Get summary statistics and visualize the data.

Normalize the data using StandardScaler().

Create a new DataFrame with the scaled data, setting "coin_id" as the index.

Finding the Best Value for k

Use the elbow method to find the best k-value:

Compute inertia for k-values from 1 to 11.

Plot the elbow curve to determine the optimal k.

Answer: What is the best value for k?

Clustering Cryptocurrencies Using K-Means

Initialize and fit the K-Means model with the best k-value.

Predict clusters using the scaled DataFrame.

Create a scatter plot:

x-axis: price_change_percentage_24h

y-axis: price_change_percentage_7d

Color points based on cluster labels

Include coin_id in hover details

Optimizing Clusters with PCA

Reduce features to 3 principal components using PCA.

Retrieve explained variance to determine data representation.

Create a new DataFrame with PCA-transformed data.

Finding the Best k Using PCA DataFrame

Repeat the elbow method using PCA-transformed data.

Compare k-value found in PCA vs. original scaled data.

Clustering Cryptocurrencies Using PCA DataFrame

Fit K-Means using PCA-transformed data.

Predict clusters and create a scatter plot:

x-axis: PC1, y-axis: PC2

Color points based on cluster labels

Include coin_id in hover details

Answer: What is the impact of using fewer features?

Visualization and Comparison

Compare elbow curves from original and PCA data.

Compare cluster results from both methods.

Answer: How does feature reduction impact clustering?

Requirements

Key Features:

Elbow method: Determines optimal k

K-Means clustering: Groups cryptocurrencies

PCA: Reduces feature dimensions

hvPlot visualizations: Interactive scatter plots

Comparative analysis: Evaluates clustering results

Coding Standards:

Import libraries at the beginning

Use clear variable names (snake_case format)

Follow DRY (Don't Repeat Yourself) principles

Write efficient, maintainable code
