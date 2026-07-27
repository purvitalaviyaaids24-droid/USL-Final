# Customer Segmentation – Summary Report

## Business Problem and Dataset

The objective of this project is to segment customers based on their
purchasing behavior so that the business can create targeted marketing
strategies. The Online Retail dataset contains transaction-level
information including Invoice, Quantity, InvoiceDate, Price, Customer ID
and Country. For this analysis, United Kingdom customers were selected.

## RFM Feature Engineering

Customer-level RFM features were created. Recency represents the number
of days since the customer's most recent purchase using 31 December 2011
as the reference date. Frequency represents the total number of unique
invoices placed by each customer. Monetary represents the total spending
of each customer.

The data was preprocessed by removing missing Customer IDs, non-positive
quantities and non-positive prices. TotalPrice was calculated as Quantity
multiplied by Price. Outliers were capped using the IQR method. Frequency
and Monetary were log transformed because they were strongly right-skewed.
Finally, StandardScaler was applied to all three clustering features so
that features with larger numerical values would not dominate clustering.

## Algorithm Comparison

Three unsupervised learning algorithms were evaluated: K-Means,
Agglomerative Hierarchical Clustering and DBSCAN. The models were compared
using Silhouette Score, Davies-Bouldin Index and Calinski-Harabasz Index.
The best-performing algorithm was [ALGORITHM NAME] based on the overall
internal metrics.

K-Means stability was also checked using five different random states.
The mean Silhouette Score was [VALUE] and the standard deviation was
[VALUE], indicating [stable/variable] clustering results.

## Customer Segments

The final segmentation identified [NUMBER] main customer groups.

**Champions:** These customers have recent purchases, high purchase
frequency and high monetary value. They are the most valuable customers.

**Loyal Customers:** These customers purchase regularly and show strong
customer engagement.

**At-Risk Customers:** These customers have not purchased recently but
may have previously generated significant revenue.

**Hibernating Customers:** These customers have high recency and relatively
low frequency and monetary value, indicating low engagement.

## Future Improvements

The analysis could be improved by including additional features such as
product preferences, customer demographics, purchase channel, campaign
response, geographic information and website/app behavior. Semi-supervised
refinement or real-time customer scoring could also be introduced to make
the segmentation more useful for ongoing marketing campaigns.