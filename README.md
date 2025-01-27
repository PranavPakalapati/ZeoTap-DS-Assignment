# ZeoTap-DS-Assignment


**Overview**
This project aims to perform customer clustering analysis on transactional data from an e-commerce platform. Using K-Means clustering, the project groups customers based on features such as quantity, total value, and price of items they have purchased. The output includes detailed cluster characteristics, a visual representation of the clusters, and a PDF report summarizing the clustering results.

The steps followed in this analysis include data loading, preprocessing, feature aggregation, clustering, evaluation, and reporting.

**Requirements**
To run this project, you need the following Python libraries:

pandas: For data manipulation and aggregation
matplotlib: For plotting customer clusters
scikit-learn: For performing K-Means clustering and evaluating clustering performance
fpdf: For generating the PDF report
To install the required libraries, run:

bash
Copy
Edit
pip install pandas matplotlib scikit-learn fpdf
Data Sources
The analysis uses three datasets:

Customers: Contains customer details.
Products: Contains product information, including the ProductID.
Transactions: Contains transactional details, including CustomerID, ProductID, Quantity, and TotalValue.
The datasets are loaded directly from the following Google Drive links:

Customers Dataset
Products Dataset
Transactions Dataset
Steps Involved
1. Data Preprocessing
The three datasets (customers, products, and transactions) are merged based on customer and product IDs.
A check is performed to ensure that the necessary columns such as CustomerID, Quantity, TotalValue, and Price are available.
The data is aggregated at the customer level to compute the average Quantity, TotalValue, and Price (if available) for each customer.
2. Clustering
K-Means clustering is applied to group customers into n_clusters clusters. The clustering is performed based on scaled features (Quantity, TotalValue, and Price).
The Davies-Bouldin Index (DBI) is computed to evaluate the quality of the clustering. The DBI is a measure of clustering quality, where lower values indicate better clustering.
3. Visualization
A scatter plot is generated to visualize the customer clusters, using the first two features (e.g., Quantity and TotalValue) for plotting.
The plot is saved as an image and included in the PDF report.
4. PDF Report
A PDF report is generated with the following sections:
Clustering Metrics: The number of clusters and Davies-Bouldin Index.
Cluster Visualization: A plot showing the clusters.
Cluster Summary: For each cluster, the number of customers, average quantity, and average total value are summarized.
Output Files
Clustering Report PDF: A PDF file named Pranav_Pakalapati_Clustering_Report.pdf is generated, which includes:

The number of clusters.
Davies-Bouldin Index (clustering quality metric).
A visual representation of the clusters.
A summary of each cluster with key statistics (number of customers, average quantity, and average total value).
Cluster Visualization: A plot of customer clusters saved as customer_clusters.png.

Final Results
Davies-Bouldin Index: Measures the quality of the clustering. The lower the value, the better the clustering.
Example output: Davies-Bouldin Index: 0.9135
Clustering Summary: For each cluster, the following values are presented:
Cluster 0:
Number of Customers: 120
Average Quantity: 3.2
Average Total Value: 250.5
Cluster 1:
Number of Customers: 150
Average Quantity: 2.8
Average Total Value: 220.3
(Similarly for other clusters...)
Future Improvements
Optimal Number of Clusters: Use techniques like the Elbow Method or Silhouette Score to determine the optimal number of clusters.
Incorporate More Features: Additional customer features such as demographic data (age, region) could be integrated for better clustering.
Clustering Algorithms: Explore other clustering algorithms like DBSCAN or Hierarchical Clustering to compare the results.
License
This project is licensed under the MIT License.
