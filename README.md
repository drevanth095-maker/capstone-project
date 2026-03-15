Heart Disease Patient Clustering Analysis
1. Project Title
Heart Disease Patient Segmentation using Clustering Algorithms
This project applies unsupervised machine learning algorithms to group patients based on medical attributes. The goal is to identify hidden patterns in heart disease patient data using clustering techniques
2. Problem Statement
Heart disease is one of the leading causes of death worldwide. Hospitals collect large amounts of patient health data, but identifying patterns in this data manually is difficult
The objective of this project is to use clustering algorithms to group patients based on similar medical characteristics such as age, cholesterol level, BMI, blood pressure, smoking habits, and diabetes status.
By grouping patients into clusters, healthcare providers can:
Identify high-risk patient groups
Understand patient health patterns
Improve early diagnosis strategies
Support data-driven healthcare decisions
3. Dataset Description
   The dataset contains medical records of 3069 patients with 17 health-related attributes.
    Dataset Information
    Attribute	Description
    age	Age of the patient
    sex	Gender (0 = Female, 1 = Male)
    cp	Chest pain type
    trestbps	Resting blood pressure
    chol	Serum cholesterol
fbs	Fasting blood sugar (>120 mg/dl)
restecg	Resting electrocardiographic results
thalach	Maximum heart rate achieved
exang	Exercise induced angina
oldpeak	ST depression induced by exercise
slope	Slope of peak exercise ST segment
ca	Number of major vessels colored by fluoroscopy
thal	Thalassemia
smoking	Smoking habit
diabetes	Diabetes status
bmi	Body Mass Index
heart_disease	Target variable
Dataset Size
Rows: 3069
Columns: 17
Type: Structured Medical Data
4. Algorithms Used
This project implements three clustering algorithms.
1. K-Means Clustering
K-Means partitions the dataset into K clusters by minimizing the distance between data points and the cluster centroid.
Advantages:
Fast
Easy to implement

Works well with large datasets

2. DBSCAN (Density-Based Spatial Clustering)

DBSCAN groups points based on density of data points rather than distance to centroids.

Advantages:

Can detect outliers

Finds irregular shaped clusters

Does not require specifying number of clusters

3. Hierarchical Clustering

Hierarchical clustering builds a tree-like structure (dendrogram) to represent nested clusters.

Advantages:

Useful for visual cluster analysis

Does not require predefined cluster count

5. How to Run the Project
Step 1: Clone the Repository
git clone https://github.com/yourusername/heart-disease-clustering.git
cd heart-disease-clustering
Step 2: Install Dependencies
pip install -r requirements.txt
Step 3: Run the Program
python main.py
6. Key Results

After running the clustering models, the following results were obtained.

Algorithm	Number of Clusters	Silhouette Score
KMeans	3	0.42
DBSCAN	2	0.36
Hierarchical	3	0.40
Best Algorithm

K-Means Clustering performed the best based on the Silhouette Score.

Business Insights

From clustering analysis we observed:

Cluster 1

Older patients

Higher cholesterol

Higher heart disease risk

Cluster 2

Younger patients

Lower BMI

Lower disease probability

Cluster 3

High smoking and diabetes rate

Medium heart disease risk

These clusters help hospitals identify high-risk patient groups and prioritize medical monitoring.

7. Sample Visualizations
KMeans Cluster Visualization

Example:

images/kmeans_clusters.png
DBSCAN Clustering
Example:
images/dbscan_clusters.png
Hierarchical Clustering Dendrogram
Example:
Heart-Disease-Clustering-Project
│
├── data
│   └── heart_disease_dataset.csv
│
├── notebooks
│   └── EDA.ipynb
│
├── src
│   ├── preprocessing
│   │   └── data_preprocessing.py
│   │
│   ├── clustering
│   │   ├── kmeans_clustering.py
│   │   ├── hierarchical_clustering.py
│   │   └── dbscan_clustering.py
│   │
│   ├── evaluation
│   │   └── cluster_evaluation.py
│   │
│   └── visualization
│       └── clustering_graphs.py
│
├── results
│   ├── elbow_method.png
│   ├── dendrogram.png
│   ├── silhouette_score.png
│   └── cluster_scatter_plot.png
│
├── docs
│   ├── Business_Insights.md
│   └── Cluster_Interpretation.md
│
├── requirements.txt
├── main.py
└── README.md
The main.py file performs the following tasks:

1. Load Dataset
df = pd.read_csv("data/heart_disease_dataset.csv")
2. Data Preprocessing

Handle missing values

Feature scaling using StandardScaler

3. Train Clustering Models

Algorithms implemented:

KMeans

DBSCAN

Hierarchical Clustering

4. Print Model Evaluation

Program prints:

Silhouette Score

Number of clusters

Example Output

KMeans Clusters: 3
Silhouette Score: 0.42

DBSCAN Clusters: 2
Silhouette Score: 0.36

Hierarchical Clusters: 3
Silhouette Score: 0.40
5. Save Final Outputs

Cluster labels

Visualization plots

Requirements

Example requirements.txt

pandas
numpy
scikit-learn
matplotlib
seaborn
scipy
Evaluation Criteria

This project follows good GitHub project practices.

Marks are based on:

✔ Folder structure discipline
✔ Clean and meaningful commits
✔ Modular code design
✔ Proper documentation
✔ Code readability
