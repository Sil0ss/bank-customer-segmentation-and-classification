# Bank Customer Segmentation and Classification

## Project Overview

This project aims to analyze customer transaction behavior in a banking environment using Machine Learning techniques.

The project is divided into two stages:

1. **Customer Segmentation (Unsupervised Learning)**
   - Identify groups of customers with similar behavioral characteristics using K-Means Clustering.

2. **Customer Classification (Supervised Learning)**
   - Build a predictive model capable of assigning new customers into the identified clusters.

This project demonstrates an end-to-end machine learning workflow, starting from data preprocessing, clustering, cluster interpretation, and classification model development.

---

# Business Objective

Banks need to understand customer behavior to:

- Improve customer targeting
- Design personalized marketing campaigns
- Optimize customer retention strategies
- Identify high-value customer groups
- Support data-driven business decisions

By segmenting customers and predicting their segments automatically, financial institutions can improve customer relationship management.

---

# Dataset Information

The dataset contains customer transaction and demographic information.

## Features

| Feature | Description |
|----------|------------|
| TransactionAmount | Amount of money involved in the transaction |
| TransactionType | Type of transaction (Debit/Credit) |
| Location | Customer transaction location |
| Channel | Transaction channel |
| CustomerAge | Customer age |
| CustomerOccupation | Customer occupation |
| TransactionDuration | Duration of transaction |
| LoginAttempts | Number of login attempts |
| AccountBalance | Customer account balance |

---

# Exploratory Data Analysis (EDA)

The following analyses were performed:

- Dataset inspection
- Missing value analysis
- Duplicate checking
- Statistical summary
- Feature distribution analysis
- Numerical vs categorical feature identification

---

# Data Preprocessing

Several preprocessing steps were applied before modeling:

## Data Cleaning

- Missing value detection
- Duplicate record removal

## Feature Encoding

Categorical variables were transformed using:

- Label Encoding

Examples:

| Original | Encoded |
|-----------|----------|
| Debit | 0 |
| Credit | 1 |

---

## Feature Scaling

Numerical variables were standardized using:

- StandardScaler

This step ensures all features contribute equally during clustering.

---

# Customer Segmentation

## Algorithm

### K-Means Clustering

K-Means was used to identify customer groups based on behavioral similarities.

---

## Determining Optimal Number of Clusters

The optimal cluster number was identified using:

### Elbow Method

The Within-Cluster Sum of Squares (WCSS) was evaluated across multiple cluster values.

Result:

- Optimal K = 2

---

## Cluster Visualization

Principal Component Analysis (PCA) was used to reduce dimensions and visualize customer groups.

### PCA Benefits

- Dimensionality reduction
- Cluster visualization
- Easier interpretation

---

# Cluster Interpretation

After inverse transformation, the clusters were interpreted as follows:

## Cluster 0
### Persona:
**Senior Customers with Conservative Financial Behavior**

Characteristics:

- Higher average age
- Higher account balance
- Longer transaction duration
- Lower transaction amount

Behavior:

- Financially stable customers
- Tend to maintain larger balances
- More conservative spending behavior

---

## Cluster 1
### Persona:
**Younger Customers with Consumptive Behavior**

Characteristics:

- Lower average age
- Lower account balance
- Shorter transaction duration
- Higher transaction amount

Behavior:

- More active transaction behavior
- Faster spending patterns
- Lower savings retention

---

# Classification Model

After obtaining customer segments, cluster labels were used as the target variable.

## Target Variable

```python
Target = Cluster
```

---

## Train-Test Split

Dataset was divided into:

- Training Data
- Testing Data

Using:

```python
train_test_split()
```

---

## Classification Algorithm

### Decision Tree Classifier

Reasons:

- Easy to interpret
- Handles numerical and categorical data
- Suitable for beginner machine learning projects

---

## Model Evaluation

Evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

# Additional Experiments

The project also explores:

## Random Forest Classifier

Benefits:

- Better generalization
- Reduced overfitting
- Higher predictive performance

---

## Hyperparameter Tuning

Performed to improve model performance using parameter optimization techniques.

---

# Project Structure

```
bank-customer-segmentation-and-classification/
│
├── data/
│   ├── data_clustering.csv
│   └── data_clustering_inverse.csv
│
├── notebooks/
│   ├── 01_customer_segmentation_kmeans.ipynb
│   └── 02_customer_classification_decision_tree.ipynb
│
├── models/
│   ├── model_clustering.h5
│   ├── PCA_model_clustering.h5
│   ├── decision_tree_model.h5
│   ├── explore_RandomForestClassifier_classification.h5
│   └── tuning_classification.h5
│
├── README.md
└── requirements.txt
```

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Yellowbrick
- Joblib

---

# Machine Learning Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Label Encoding
- Feature Scaling
- K-Means Clustering
- Elbow Method
- PCA
- Cluster Interpretation
- Decision Tree Classification
- Random Forest Classification
- Hyperparameter Tuning
- Model Evaluation
- Model Persistence

---

# Future Improvements

Potential enhancements:

- More advanced clustering algorithms
  - DBSCAN
  - Hierarchical Clustering
  - Gaussian Mixture Models

- Additional classification models
  - XGBoost
  - LightGBM
  - CatBoost

- Deployment using Streamlit

- Real-time prediction dashboard

---

# Author

**Fadhil Muhammad Rifqi**

Aspiring Data Analyst | Data Science Enthusiast | Machine Learning Learner
