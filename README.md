# Customer Segmentation using Unsupervised Learning

Video Explanation and dataset are given here : https://drive.google.com/drive/folders/1-8gEjOXwyCoAA1O1W2_wlBjNc0jt9SBD?usp=sharing
## Project Overview

This project performs customer segmentation using RFM analysis and
unsupervised machine learning.

The dataset contains online retail transaction information such as
Invoice, Quantity, InvoiceDate, Price, Customer ID and Country.

## Objective

The main objective is to identify different customer groups based on:

- Recency
- Frequency
- Monetary

These segments can help businesses create targeted marketing strategies.

## Data Preprocessing

The dataset was cleaned by:

- Filtering customers from United Kingdom
- Removing missing Customer IDs
- Removing Quantity <= 0
- Removing Price <= 0
- Creating TotalPrice

## RFM Analysis

Three customer-level features were created:

- Recency – days since the last purchase
- Frequency – number of unique orders
- Monetary – total customer spending

Outliers were capped using the IQR method.

Frequency and Monetary were log transformed and all features were
standardized using StandardScaler.

## Clustering Algorithms

Three clustering algorithms were compared:

1. K-Means
2. Agglomerative Hierarchical Clustering
3. DBSCAN

The algorithms were compared using:

- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Index

## Customer Segments

The clusters were interpreted as business personas such as:

- Champions
- Loyal Customers
- At-Risk Customers
- Hibernating Customers

## Files

- CustomerSegmentation_UnsupervisedLearning.ipynb
- rfm_scaler.pkl
- customer_segmentation_model.pkl
- summary_report.md
- requirements.txt

## Tools Used

Python, Pandas, NumPy, Matplotlib, Seaborn,
Scikit-learn, SciPy and Joblib.

Author
Purvi Talaviya
