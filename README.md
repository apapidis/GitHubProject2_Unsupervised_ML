# Customer Segmentation with Machine Learning

**Team** :Avaritsioti Olympia, Alexandros Papidis, Georgia Samara,Theologos Zervos 
**Dataset** source:https://www.kaggle.com/datasets/akelvarghese/global-superstore-sales-dataset

### Global Superstore Sales Analysis

Customer segmentation project using **K-Means Clustering and Principal
Component Analysis (PCA)** to identify meaningful customer groups based
on purchasing behavior in a retail sales dataset.

This project demonstrates an **end-to-end data science workflow**,
including data cleaning, feature engineering, clustering analysis, and
business insight generation.

------------------------------------------------------------------------

# Project Objective

Retail businesses generate large volumes of transactional data, but
extracting actionable insights from this data can be challenging.

The objective of this project is to:

-   Discover hidden patterns in customer purchasing behavior
-   Identify distinct customer segments
-   Provide business insights that support marketing and sales
    strategies

By grouping similar customers together, companies can improve:

-   Personalized marketing campaigns
-   Inventory planning
-   Product recommendations
-   Revenue growth

------------------------------------------------------------------------

# Dataset

The dataset contains **sales transactions for the year 2024**.

### Key Features

  Feature      Description
  ------------ --------------------
  Region       Sales region
  Product      Product name
  Category     Product category
  Units_Sold   Quantity purchased
  Unit_Price   Price per unit
  Revenue      Total sales value
  Cost         Cost of goods sold
  Profit       Profit generated

Initial dataset size:

-   2000 transactions
-   10 variables

------------------------------------------------------------------------

# Data Cleaning & Preprocessing

Several preprocessing steps were performed to prepare the data for
machine learning.

### Data Cleaning

-   Removed Date column (dataset covers a single year)
-   Removed Salesperson column (too many unique values)
-   Standardized inconsistent values in Region and Product names
-   Removed missing values
-   Filtered transactions with negative or zero profit

### Encoding

Categorical variables were converted into numerical features using:

One-Hot Encoding

### Feature Scaling

All features were standardized using:

StandardScaler

This prevents variables with large numeric ranges from dominating the
clustering process.

------------------------------------------------------------------------

# Exploratory Data Analysis

Initial exploration focused on:

-   Distribution of revenue and profit
-   Product category patterns
-   Regional sales behavior
-   Outlier detection

------------------------------------------------------------------------

# Machine Learning Methodology

## K-Means Clustering

K-Means clustering was used to group transactions based on purchasing
behavior.

### Finding the Optimal Number of Clusters

Two evaluation techniques were used:

**Elbow Method**\
Evaluates cluster compactness using inertia.

**Silhouette Score**\
Measures how well each observation fits within its assigned cluster.

We choose k=4 based on above results and for more business insights

-----------------------------------------------------------------------

# Dimensionality Reduction

To visualize clusters in lower dimensions, **Principal Component
Analysis (PCA)** was applied.

Visualization techniques used:

-   2D PCA scatter plots
-   3D PCA cluster visualization

------------------------------------------------------------------------

# Customer Segments Identified

### Cluster 0 --- High-Value Tech Buyers

High spending customers purchasing premium electronics.

### Cluster 1 --- Office Equipment Buyers

Customers purchasing printers, monitors, and office tools.

### Cluster 2 --- Tech Enthusiasts

Customers buying multiple low-cost tech gadgets and accessories.

### Cluster 3 --- Budget Office Shoppers

Customers buying office supplies in moderate quantities.

<img width="656" height="567" alt="image" src="https://github.com/user-attachments/assets/bb749ecf-9d56-401a-9465-a6ac306dcb23" />

------------------------------------------------------------------------

# Key Insights

-   High-value tech buyers generate the highest revenue per transaction
-   Office equipment buyers represent a significant portion of sales
-   Budget shoppers make frequent smaller purchases
-   Product category strongly influences purchasing behavior

------------------------------------------------------------------------

# Business Impact

Customer segmentation supports:

### Personalized Marketing

Targeted campaigns based on purchasing behavior.

### Inventory Optimization

Stock products based on cluster demand patterns.

### Product Recommendations

Upsell and cross-sell based on cluster preferences.

------------------------------------------------------------------------

# Technology Stack

Python libraries used:

-   pandas
-   numpy
-   matplotlib
-   seaborn
-   scikit-learn
-   yellowbrick

Machine learning techniques:

-   K-Means Clustering
-   PCA
-   Silhouette Score
-   Elbow Method

------------------------------------------------------------------------

# Future Improvements

-   Add customer demographic data
-   Track cluster changes over time
-   Apply additional clustering algorithms (DBSCAN, Hierarchical
    Clustering)
-   Implement automated customer segmentation
