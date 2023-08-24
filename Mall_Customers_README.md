
# README for Mall Customers Behavior Model Project

---

## Introduction
This project aims to understand the behavior of mall customers by clustering them based on their purchasing characteristics. Clustering can provide insights into different customer segments, aiding in targeted marketing and business strategy optimization.

## Dataset
The dataset, named 'Mall_Customers.csv', comprises several features:
- `CustomerID`: Unique identifier for each customer.
- `Gender`: Gender of the customer.
- `Age`: Age of the customer.
- `Annual Income (k$)`: Customer's annual income in thousands of dollars.
- `Spending Score (1-100)`: Score assigned to the customer based on their spending behavior.

## Data Preprocessing
- The dataset was checked for missing values.
- Only numerical columns (`Age`, `Annual Income (k$)`, and `Spending Score (1-100)`) were considered for clustering.
- Data normalization was applied using `StandardScaler` to ensure all features contribute equally to the clustering process.

## Exploratory Data Analysis (EDA)
- Pair plots were generated to visualize the distributions and relationships between features.
- A correlation matrix was plotted to understand the inter-relationships between different features.

## Model Building & Evaluation
Multiple clustering approaches were explored:
- **KMeans Clustering**: Used the Elbow method to determine the optimal number of clusters. Both 5 and 6 clusters were considered, with silhouette scores of 0.3171 and 0.3336, respectively.
- **PCA with KMeans**: Applied Principal Component Analysis (PCA) for dimensionality reduction, followed by KMeans clustering. This approach yielded improved silhouette scores.
- **Agglomerative Clustering**: Hierarchical clustering was applied, resulting in silhouette scores of 0.2870 (5 clusters) and 0.3102 (6 clusters).
- **DBSCAN**: Density-Based Spatial Clustering of Applications with Noise was used, which gave a silhouette score of 0.0120.

## Conclusion
The dataset provided insights into different customer segments based on their age, income, and spending scores. While several clustering methods were explored, achieving a high silhouette score proved challenging with the current dataset and features. The highest silhouette score obtained was 0.4166 (not achieved in our attempts). Despite this, the clustering revealed distinct customer groups that can be targeted differently in marketing campaigns. Further exploration with more data, features, or advanced algorithms might provide clearer customer segments in future endeavors.

---

