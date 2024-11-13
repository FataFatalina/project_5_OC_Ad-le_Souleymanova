# Customer Segmentation for an E-commerce Platform

## Project Context
Olist is an e-commerce sales platform that generates a significant amount of data. This project focuses on **customer segmentation** based on similar profiles to:
- Understand different types of users.
- Create stable customer segments.
- Propose a **maintenance strategy** to keep segments stable over time.

## Project Objectives
- Perform customer segmentation to identify distinct user profiles.
- Use clustering techniques and silhouette analysis to assess segmentation quality.
- Develop a time-based analysis to evaluate the stability of these segments.

## Project Plan
1. **Data Manipulation**
2. **Exploratory Data Analysis (EDA)**
3. **Data Preprocessing**
4. **Clustering & Partitioning**
5. **Silhouette Score Analysis**
6. **Business Analysis of Segments**
7. **Temporal Stability Analysis of Segmentation**

## Dataset
- The dataset is open and available on **Kaggle**.
- It includes various data types: **text** and **numeric** values.
  
### Data Breakdown:
- **Order History**
- **Purchased Products**
- **Customer Satisfaction Ratings**
- **Customer Locations**
  
All data sources are combined into a single dataframe for analysis.

## Project Steps

### I) Data Manipulation
- **Feature Engineering**: 
  - Group data by unique customer ID.
  - Aggregate using functions like `min`, `max`, `mode`, `mean`, and `count`.
- **Data Cleaning**:
  - Remove redundant columns.
  - Handle missing values by imputing modal values.
  - Encode categorical columns using one-hot encoding.
- **Dimensionality Reduction**: 
  - Apply variance-based reduction to remove features with low variance.

### II) Exploratory Data Analysis (EDA)
Conducted a thorough analysis to understand the distribution, relationships, and patterns within the data.

### III) Dimensionality Reduction
- **PCA (Principal Component Analysis)**: 
  - Transforms the data by projecting it onto a coordinate system based on data variance.
  - High-variance features are selected for analysis.
  
- **ISOMAP**: 
  - A non-linear dimensionality reduction technique using K-Nearest Neighbors (KNN).
  - Computes the shortest distance between nodes to represent the data in lower dimensions while preserving distances between similar points.

### IV) Clustering with KMeans
Utilized **KMeans** clustering to segment customers based on their behaviors and profiles.

### V) Silhouette Score Analysis
- The silhouette score measures:
  - **Cluster cohesion** (intra-cluster distance).
  - **Cluster separation** (distance to the nearest external cluster).
  - Values range from 0 (worst) to 1 (best).

### VI) Business Analysis of Segments
- **Radar/Kiviat Diagrams**: Used to visualize and interpret each segment's business characteristics.

### VII) Temporal Stability Analysis of Segmentation
1. Create a **baseline model** using the first 12 months of purchase data.
2. Expand the dataset by adding one month of new customer data at a time.
3. Train a new model on each expanded dataset.
4. Evaluate stability using **ARI (Adjusted Rand Index)** scores by comparing the baseline model with the model trained on each subsequent period.

   - **Observation**: The clusters start changing after 1.5 months, indicating the point at which a new segmentation may be required.

5. **Silhouette Score Comparison**: Compared clustering quality with **KMeans** and **DBSCAN** for six clusters (`k=6`).

## Tools & Libraries
- **Python**: Version X.X
- **pandas**, **scikit-learn**, **KMeans**, **DBSCAN**, **Matplotlib**, **Seaborn**
- **Jupyter Notebook** for analysis and visualization

---

## Conclusion
This project successfully segments e-commerce customers based on behavioral data, providing actionable insights for targeted marketing and customer relationship management. Temporal stability analysis offers a basis for long-term segment maintenance, ensuring that segments remain relevant over time.
