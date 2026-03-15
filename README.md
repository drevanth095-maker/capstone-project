Customer Segmentation Using Clustering Algorithms
1. Project Title

Customer Segmentation using Machine Learning Clustering Algorithms (KMeans, Hierarchical, DBSCAN)

2. Problem Statement

Businesses need to understand their customers to provide better services, targeted marketing, and improved customer retention.

However, customers often have different purchasing behaviors, demographics, and spending patterns, making it difficult to treat them as a single group.

This project aims to segment customers into meaningful groups using clustering algorithms so businesses can identify patterns such as:

High value customers

Budget customers

Frequent shoppers

At-risk customers

Clustering helps businesses make data-driven marketing and strategic decisions.

3. Dataset Description

The dataset used in this project is:

File: heart_disease_dataset.csv

The dataset contains information about patients including medical and lifestyle attributes which can be used to analyze patterns and group individuals.

Age

Gender

Blood Pressure                                                                              blood pressure level
 
bmi                                                                                          body mass index

These features help identify patterns related to heart disease risk groups.

4. Algorithms Used

This project compares three clustering algorithms.

1. KMeans Clustering

KMeans groups data points into K clusters based on distance from centroids.

Steps:

Choose number of clusters (K)

Initialize centroids

Assign points to nearest centroid

Update centroid positions

Repeat until convergence

Used for:

Fast clustering

Large datasets

2. Hierarchical Clustering

Hierarchical clustering builds a tree-like structure (dendrogram).

Types:

Agglomerative (bottom-up)

Divisive (top-down)

This project uses:

Ward Method

Ward method minimizes variance within clusters.

3. DBSCAN (Density-Based Clustering)

DBSCAN groups data points based on density.

Advantages:

Detects arbitrary shaped clusters

Handles noise/outliers

Does not require predefined cluster number

Parameters:

eps
min_samples
5. Project Structure
Customer-Segmentation-Clustering

├── Advanced

├── Clustering_methods

├── Data-preprocessing

├── Dimensional_reduction

├── EDA

├── Results
└── clustering graphs

├── src
└── clustering

├── Business Insights

├── Cluster Interpretation

├── README.md

└── heart_disease_dataset.csv

This structure ensures:

Modular code

Organized experimentation

Easy project maintenance

6. How to Run the Project
Step 1: Clone the Repository
git clone https://github.com/yourusername/customer-segmentation-clustering.git

Step 2: Install Dependencies
pip install -r requirements.txt

Step 3: Run the Project
python main.py

The script will:

Load the dataset

Perform preprocessing

Apply clustering algorithms

Generate cluster results

Save visualization outputs

7. Data Preprocessing

The dataset undergoes several preprocessing steps:

Handling Missing Values

Missing data is handled using:

Mean imputation

Data cleaning

Feature Scaling

StandardScaler is used:

StandardScaler()

This ensures features are normalized before clustering.

8. Exploratory Data Analysis (EDA)

EDA helps understand dataset patterns.

Visualizations include:

Feature distribution plots

Correlation heatmap

Outlier detection

Pair plots

These insights guide feature selection for clustering.

9. Cluster Evaluation Methods

To determine the optimal clustering performance, the following methods are used:

1. Elbow Method

Used to determine the optimal number of clusters.

The point where WCSS decreases slowly is considered the best K value.

2. Silhouette Score

Measures cluster quality.

Range:

-1 to 1

Higher score means better cluster separation.

3. Davies-Bouldin Index

Measures cluster similarity.

Lower value indicates better clustering performance.

10. Key Results
Number of Clusters Found
Algorithm	Clusters
KMeans	3
Hierarchical	3
DBSCAN	Varies depending on density
Best Algorithm

Based on evaluation metrics:

KMeans provided the most stable clusters with better silhouette score.

11. Sample Visualizations
Elbow Method Graph

Shows optimal cluster number.

Hierarchical Dendrogram

Displays cluster merging structure.

Cluster Scatter Plot

Shows cluster distribution between features such as:

Age

Cholesterol

12. Printed Results

Example console output:

Silhouette Score: 0.63
Number of clusters: 3
13. Saved Outputs

The project automatically saves:

Clustering graphs

Evaluation metrics

Cluster assignments

Inside:

Results/
14. Business Insights

Clustering reveals different customer segments.

Cluster 1 – Low Risk Group

Younger individuals

Lower cholesterol levels

Cluster 2 – Moderate Risk

Average age

Moderate health risk

Cluster 3 – High Risk Group

High cholesterol

Higher probability of heart disease

These insights help healthcare professionals:

Identify high-risk patients

Recommend preventive measures

Improve healthcare decision making

15. Cluster Interpretation

Each cluster represents a specific behavioral pattern in the dataset.

Example segmentation:

Cluster	Description
Cluster 1	Healthy individuals
Cluster 2	Moderate health risk
Cluster 3	High heart disease risk
16. Evaluation Criteria

This project follows good GitHub repository practices.

Folder Structure Discipline

Organized directories for:

preprocessing

clustering

results

Clean Commits

Each update corresponds to a clear functionality improvement.

Code Modularity

Algorithms are separated into different modules.

Documentation Quality

Comprehensive README explaining:

Problem

Methods

Results

Readability

Code follows:

clear variable naming

comments

structured workflow

17. Technologies Used

Python

Pandas

NumPy

Scikit-Learn

Matplotlib

Seaborn

SciPy

18. Author

Venkat

Machine Learning & Data Science Project
