# CryptoClustering  

## Overview  
This project applies **unsupervised machine learning** techniques to cluster cryptocurrencies based on market performance data. Using **K-means clustering** and **Principal Component Analysis (PCA)**, we explore patterns in crypto market trends and optimize cluster groupings.  

---  

## Table of Contents  
1. [Technologies Used](#technologies-used)  
2. [Dataset](#dataset)  
3. [Project Steps](#project-steps)  
   - [1. Data Preparation](#1-data-preparation)  
   - [2. Finding the Best k (Elbow Method)](#2-finding-the-best-k-elbow-method)  
   - [3. K-Means Clustering](#3-k-means-clustering)  
   - [4. Dimensionality Reduction with PCA](#4-dimensionality-reduction-with-pca)  
   - [5. K-Means Clustering with PCA Data](#5-k-means-clustering-with-pca-data)  
   - [6. Visualization & Insights](#6-visualization--insights)  
4. [Results & Findings](#results--findings)  

---  

## Technologies Used  
- **Python**  
- **Pandas**  
- **Scikit-learn**  
- **hvPlot**  
- **Jupyter Notebook**  

---  

## Dataset  
The dataset used for clustering is **crypto_market_data.csv**, containing various cryptocurrency market statistics.  

---  

## Project Steps  

### 1. Data Preparation  
- Load the dataset into a **Pandas DataFrame**.  
- Generate **summary statistics**.  
- Visualize the data using **hvPlot**.  
- Normalize the data using `StandardScaler()`.  

### 2. Finding the Best k (Elbow Method)  
- Iterate through **k-values from 1 to 11**.  
- Compute **inertia** for each k.  
- Plot the **Elbow Curve** to determine the optimal k.  

### 3. K-Means Clustering  
- Use the **optimal k-value** found in the previous step.  
- Fit a **K-Means model** to the scaled data.  
- Predict clusters and visualize results using **hvPlot**.  

### 4. Dimensionality Reduction with PCA  
- Apply **PCA (`n_components=3`)** to reduce dimensionality.  
- Compute the **explained variance** of each principal component.  
- Re-run the **Elbow Method** on the PCA-transformed data.  

### 5. K-Means Clustering with PCA Data  
- Perform **clustering** using the **PCA-reduced dataset**.  
- Compare **cluster results** before and after PCA.  

### 6. Visualization & Insights  
- Compare the **Elbow Curves** before and after PCA.  
- Compare **Cluster Distributions** before and after PCA.  
- Analyze the **impact of using fewer features** in K-Means.  

---  

## Results & Findings  
- The **optimal k-value** was determined using the **Elbow Method**.  
- **PCA improved clustering efficiency** by reducing noise while preserving key market trends.  
- **Cluster visualization** helped identify patterns in **crypto market behavior**.  
