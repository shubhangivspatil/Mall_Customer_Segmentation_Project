 **Mall_Customer_Segmentation_Project**

** Mall Customer Segmentation Project**

**Overview**
This project segments mall customers based on their annual income and spending score using KMeans clustering. 
The goal is to identify distinct customer groups to help tailor marketing strategies. 
The project involves data preprocessing, exploratory data analysis (EDA), clustering, and visualization of the results.

**Project Structure**

•	Mall_Customers.csv: Dataset containing customer information.
•	customer_segmentation.py: Main script for data preprocessing, clustering, and visualization.
•	README.md: This file, providing an overview of the project and instructions for setup and usage.

**Setup and Requirements**

**Prerequisites**

•	Python 3.7+
•	Required Python packages: pandas, numpy, matplotlib, seaborn, sklearn, plotly
Installation
To install the required packages, you can use the following command:
bash
Copy code
pip install pandas numpy matplotlib seaborn scikit-learn plotly

**Detailed Steps**

1. Data Loading and Preprocessing
•	Loading Data: The dataset is loaded and its structure is inspected for a preliminary understanding.
•	Handling Missing Values: The dataset is checked for any missing values.
•	Encoding Categorical Variables: The 'Genre' column is one-hot encoded to convert categorical data into numerical format.
•	Feature Selection: Key features Annual Income (k$) and Spending Score (1-100) are selected for clustering.
•	Normalization: Features are scaled using StandardScaler to ensure they have a mean of 0 and a standard deviation of 1.

2. Exploratory Data Analysis (EDA)
   
•	Histograms and Boxplots: Distributions of Annual Income and Spending Score are visualized.
•	Pairplot: Relationships between features are explored.
•	Correlation Heatmap: Correlations between all numerical features are analyzed.

3. Clustering with KMeans
•	Elbow Method: The optimal number of clusters is determined by plotting Within-Cluster Sum of Squares (WCSS) against the number of clusters.
•	KMeans Training: The KMeans algorithm is trained on the scaled features with the optimal number of clusters.
•	Cluster Prediction and Visualization: Clusters are predicted and visualized in a scatter plot.

4. Dimensionality Reduction with PCA
•	PCA Application: Principal Component Analysis (PCA) reduces the feature dimensions to 2 for better visualization.
•	PCA-based Clustering: KMeans clustering is repeated on the PCA-reduced features, and the results are visualized.

5. Cluster Analysis and Evaluation
•	Cluster Centers Analysis: Characteristics of each cluster are examined by analyzing the cluster centers.
•	Cluster Labels: Cluster labels are added to the original dataset.
•	Silhouette Score: The silhouette score is computed to evaluate the quality of clustering.

6. Saving the Results
•	Save to CSV: The dataset with cluster labels is saved as customer_segments.csv.

7. Additional Analyses
   
**Demographic Analysis by Clusters**

•	Age Distribution by Cluster: Analyzed using box plots.
•	Gender Distribution by Cluster: Analyzed using count plots.
Cluster Profiling
•	Cluster Profiles: Mean values of numerical features for each cluster are calculated to profile each cluster.

**Marketing Strategies**

•	Cluster 0: Offer loyalty rewards and exclusive deals to retain these high-spending customers.
•	Cluster 1: Introduce premium products or services that cater to their affluent lifestyle, possibly encouraging higher spending.
•	Cluster 2: Implement budget-friendly promotions and discounts to increase engagement and spending.

**Interactive Visualization**
•	Plotly Dash: Create interactive visualizations for exploring customer segments.

**Insights**

From the analysis and clustering:
•	Distinct Segments: Three distinct customer segments were identified:
o	Cluster 0: Customers with moderate income and high spending scores. These are likely to be enthusiastic and loyal shoppers.
o	Cluster 1: Customers with high income and moderate spending scores. These may represent affluent customers who spend cautiously.
o	Cluster 2: Customers with moderate to low income and low spending scores. These might be price-sensitive customers or those less engaged with mall shopping.
•	Marketing Strategies: The mall can tailor marketing strategies for each segment:
o	Cluster 0: Offer loyalty rewards and exclusive deals to retain these high-spending customers.
o	Cluster 1: Introduce premium products or services that cater to their affluent lifestyle, possibly encouraging higher spending.
o	Cluster 2: Implement budget-friendly promotions and discounts to increase engagement and spending.

**Future Work**
•	Incorporate Additional Features: Include other customer attributes such as age, gender, and shopping frequency to enhance segmentation.
•	Temporal Analysis: Analyze spending behavior over time to identify trends and seasonal patterns.
•	Advanced Clustering Techniques: Experiment with other clustering algorithms like DBSCAN or hierarchical clustering for potentially better results.
•	Customer Feedback: Integrate customer feedback and satisfaction scores to refine the segmentation and improve the customer experience.
•	Personalized Marketing: Develop a recommendation system based on the customer segments to provide personalized offers and promotions.



