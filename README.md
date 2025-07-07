# customer-segmentation_clustering-analysis
This customer segmentation project successfully applied KMeans clustering to a clean dataset of customers. Through feature scaling, Elbow and Silhouette methods, and visualizations, the analysis revealed five distinct customer groups. These clusters vary in age, income, and spending patterns, providing meaningful insights for targeted marketing, product planning, and resource allocation. Strategic actions like focusing on premium customers and engaging low spenders were derived based on behavioral traits of each cluster, aiding data-driven business decisions.

# Dataset Exploration
The dataset comprises 2000 customer records with four key features: Customer ID, Age, Annual Income, and Spending Score. Initial inspection confirms there are no missing values and no duplicate rows, making the dataset clean and ready for analysis. The numerical nature of features like income and score makes them ideal for clustering algorithms.

# Data Preprocessing
To ensure the clustering algorithm performs effectively, features were standardized using StandardScaler. This transforms the values to a uniform scale (mean 0, std 1), critical because KMeans is sensitive to magnitudes and distance-based calculations.

# Clustering Analysis
To identify the optimal number of clusters, both the Elbow Method and Silhouette Score were used:

The Elbow Method showed a noticeable “bend” at k=5, suggesting diminishing returns beyond this point.
The Silhouette Score, which measures how similar a point is to its own cluster compared to others, also peaked around 5 clusters, validating our choice.
The KMeans algorithm was then applied with k=5. Each customer was assigned a cluster label, and this was appended to the dataset as a new column.

# Visualizations
Multiple visual tools were used to understand the clustering results:

PCA 2D Plot: Principal Component Analysis reduced the 3D feature space into 2D, enabling visualization of clusters. The scatter plot showed clear separation between most clusters.
Pair Plots: These explored pairwise relationships between Age, Income, and Spending Score for each cluster.
Centroids Table: The original scale centroids revealed the behavioral tendencies of each cluster, such as high spenders with high income or younger customers with moderate spending scores.
# Recommendations Based on Clusters

Cluster 0 – Younger customers with moderate income but high spending scores.
- Best suited for loyalty rewards and exclusive deals to retain high engagement.
  
Cluster 1 – Older customers with low spending score and lower income.
- Not ideal for high-end product marketing, but suitable for budget-oriented promotions.
  
Cluster 2 – Middle-aged with high income and high spending score.
  - Primary target group for luxury or premium product campaigns.
    
Cluster 3 – Younger with low income and low spending scores.
- Potentially less valuable now, but can be targeted for engagement-based growth programs.
  
Cluster 4 – High income but very low spending score.
  - Indicates potential for re-engagement; explore reasons for low spending through surveys or personalized marketing.
