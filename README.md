## Unsupervised Learning for Tailored Banking Solutions(Customer Segmentation)

## Project Overview

This project focuses on the analysis and segmentation of banking customers to improve customer relationship management (CRM) and offer more personalized banking services. By leveraging machine learning techniques such as PCA (Principal Component Analysis) and KMeans clustering, the project analyzes customer behaviors, such as their spending patterns, credit usage, and payment history, to group them into different segments. This enables banks to better understand their customers and tailor services to their specific needs.

## Objective.

The goal of this project is to:
- **Analyze customer data** to identify key features that influence customer behavior.
- **Reduce dimensionality** using PCA to better visualize the data and identify meaningful patterns.
- **Segment customers** into distinct groups using KMeans clustering for personalized banking strategies.

## Steps Involved

### 1. Data Preprocessing
The dataset was first cleaned and preprocessed, handling missing values and scaling numerical features to prepare for analysis. The **scaling** process ensures that features with different units (e.g., income, balance, purchase history) are standardized to prevent any feature from dominating the model.

### 2. Dimensionality Reduction (PCA)
PCA was used to reduce the dimensionality of the dataset, allowing us to focus on the most significant features. By transforming the data into principal components, we can visualize the data in fewer dimensions while retaining the variance and structure.

### 3. KMeans Clustering
KMeans clustering was applied to segment customers based on their behaviors. The number of clusters (k) was determined using the **Elbow Method** and further validated using metrics like the **Davies-Bouldin Index** and **Silhouette Score**.

#### Cluster Analysis:
- **Cluster 0**: Moderate credit usage, balanced payment behavior, and moderate reliance on cash advances.
- **Cluster 1**: Low spending, minimal purchases, and heavy reliance on cash advances.
- **Cluster 2**: High credit limits, large purchases, and frequent installment payments. Likely affluent customers.
- **Cluster 3**: High reliance on cash advances, low regular purchases. Possibly in financial distress.
- **Cluster 4**: Balanced spending, frequent installment purchases, and moderate cash advances. Likely responsible credit users.
- **Cluster 5**: Varied behavior, possible minimal credit activity or distinct usage patterns.

### 4. Scenario-Based Analysis

**Cluster Evaluation Metrics for Differents K values**

To determine the optimal number of clusters for KMeans, we evaluated the clustering performance using two metrics:

- **Davies-Bouldin Index**: Lower values indicate better-defined clusters.
- **Silhouette Score**: Higher values indicate better cluster separation.

| **No Clusters (k)** | **Davies-Bouldin Index** (Lower is Better) | **Silhouette Score** (Higher is Better) |
|-------------------|--------------------------------------------|------------------------------------------|
| **2**            | 0.9771                                     | 0.4129                                   |
| **3**            | 0.8461                                     | **0.4274** (Best)                        |
| **4**            | 0.8653                                     | 0.4166                                   |
| **5**            | 0.9350                                     | 0.3748                                   |
| **6**            | **0.8160** (Best)                          | 0.3972                                   |
| **7**            | 0.7979 (Second Best)                       | 0.3925                                   |


Based on the clustering results, we derived actionable insights by prioritizing different customer segmentation strategies:

- **Scenario 1: Prioritizing Cohesion**  
  Best Choice: k=3  
  Example: Personalized Wealth Management for affluent customers using a tailored approach.

- **Scenario 2: Prioritizing Separation**  
  Best Choice: k=7  
  Example: Differentiated Banking Services for various customer segments such as young professionals, retirees, and high net-worth individuals.

- **Scenario 3: A Balance Between Cohesion and Separation**  
  Best Choice: k=6  
  Example: Comprehensive segmentation strategy for a bank offering a range of products and services.

- **Scenario 4: Aiming for Simplicity**  
  Best Choice: k=2  
  Example: Simple segmentation strategy for core banking services targeting basic and premium service users.

## Technologies Used

- **Python**
- **pandas** and **NumPy** for data manipulation and analysis
- **scikit-learn** for machine learning (PCA and KMeans)
- **matplotlib** and **seaborn** for data visualization

## Results

- **Best Cluster Count (k=3)**: Offers the highest Silhouette Score, making it the best choice for customer segmentation based on internal cohesion.
- **Lowest Davies-Bouldin Index (k=7)**: Best for customer separation with distinct financial behaviors.

## Potential Applications

- **Personalized Banking**: Tailoring financial products and services to individual customer segments.
- **Targeted Marketing**: Creating marketing campaigns for specific customer clusters.
- **Risk Management**: Identifying high-risk customers for debt management and financial advice.


You can find the project repository on GitHub:  
(https://github.com/Mazenasag/Banking-Solutions-Customer-Segmentation-.git)
