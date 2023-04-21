# Cryptocurrency Machine Learning Analysis

## Project Overview

### Purpose

The purpose of this project is to build an unsupervised machine learning model using cryptocurrency data to find a meaningful amount of clusters in which the cryptocurrencies could be grouped together, using `Python`, `scikit-learn`, `Pandas`, `Plotly`, and `HVPlot`.

### Code

The Jupyter Notebook which contains the entire analysis can be found **[here](./crypto_clustering.ipynb)**

### Data

The data used for this project can be found **[here](./resources/crypto_data.csv)** and is sourced from **[CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)**

## Process

### Raw Data to Model

The data went through the following workflow:

1. Filtering the data
2. Cleaning data
3. Object type columns were converted to binary columns of 0 or 1 using **Pandas** `get_dummies()` method
4. Every column was standardized with a **Standard Scaler** method
5. Every column was then condensed to 3 principal components using a **Principal Component Analysis (PCA)** method
6. An **Elbow Curve** method was used to find the most meaningful **K-Means** value
7. The **K-Means** value of 4 was selected from the **Elbow Curve**
8. A **K-Means** model was trained from the cleaned data and insights provided by the **Elbow Curve**
