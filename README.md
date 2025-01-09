# Clustering

# EastWest Airlines Data Clustering and Analysis

## Project Overview

This project performs clustering analysis on the EastWest Airlines customer data using multiple clustering techniques. The dataset contains customer information, including flight details, miles traveled, bonus miles, and account balance. The main goal of this project is to apply clustering algorithms to categorize customers based on their behaviors and usage of the airline's services. The following clustering methods are employed:

- K-Means Clustering
- Agglomerative (Hierarchical) Clustering
- DBSCAN (Density-Based Spatial Clustering)

Additionally, Principal Component Analysis (PCA) is used for dimensionality reduction and visualizing the clustering results.

## Data Description

The dataset used in this project is `EastWestAirlines_data.csv`, which contains the following columns:

- **Balance**: The balance of the customer's account.
- **Qual_miles**: The number of qualifying miles flown by the customer.
- **Bonus_miles**: The number of bonus miles earned by the customer.
- **Bonus_trans**: The number of bonus transactions made by the customer.
- **Flight_miles_12mo**: The number of flight miles traveled by the customer in the last 12 months.
- **Flight_trans_12**: The number of flight transactions in the last 12 months.
- **Days_since_enroll**: The number of days since the customer enrolled with EastWest Airlines.
- **Award?**: Whether the customer has won an award (binary: 1 for Yes, 0 for No).

### Basic Statistics:

- Summary statistics of the dataset (after removing duplicates) are provided for numerical features.
- The dataset is checked for missing values and duplicate entries before analysis.

## Clustering Techniques Used

### 1. K-Means Clustering
K-Means is a centroid-based algorithm that partitions the dataset into a specified number of clusters (K). The "elbow method" is used to determine the optimal value of K, and the model is evaluated using the **Silhouette Score**.

### 2. Agglomerative (Hierarchical) Clustering
Agglomerative clustering is a bottom-up approach where each data point starts as its own cluster, and clusters are merged based on proximity. A dendrogram is used to visualize the merging process and determine the number of clusters.

### 3. DBSCAN (Density-Based Spatial Clustering)
DBSCAN is a density-based algorithm that groups together points that are close to each other based on distance metrics, separating low-density points as outliers. This method is particularly useful for datasets with noise or irregular shapes.

### Dimensionality Reduction with PCA
To visualize the clustering results in two dimensions, **PCA** (Principal Component Analysis) is used to reduce the dataset to two principal components, which are then plotted for each clustering method.

## Data Preprocessing

- **Missing Data Handling**: The dataset is first checked for missing values.
- **Duplicate Removal**: Any duplicate entries are removed.
- **Feature Scaling**: The data is standardized using **StandardScaler** to ensure uniform scaling of the features, which is crucial for clustering methods like K-Means and DBSCAN.

## Visualization

- **Correlation Heatmap**: A heatmap is generated to visualize the correlation between numerical features.
- **Pair Plot**: A pair plot is created for selected features to visualize the relationships between them.
- **Box Plots**: Box plots are generated for numerical features grouped by the "Award?" column.
- **Scatter Plots**: Scatter plots are used to visualize relationships between various features, such as balance vs. bonus miles and flight miles vs. days since enrollment.

## Results

### K-Means Clustering
- The **Silhouette Score** for K-Means clustering is computed to evaluate the quality of the clusters formed.
- K-Means labels are added to the dataset for further analysis.

### Agglomerative Clustering
- The **Silhouette Score** for Agglomerative Clustering is also computed.
- Agglomerative clustering labels are added to the dataset.

### DBSCAN
- DBSCAN clustering is performed, and the **Silhouette Score** is computed for clusters.
- Points identified as noise are labeled with `-1` in the DBSCAN results.

### PCA Visualization
PCA is used to project the high-dimensional data into 2D space. The clustering results (K-Means, Agglomerative, DBSCAN) are visualized on scatter plots to see how well the algorithms have separated the data points.

## Installation

To run this project, you need to install the following Python libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy
