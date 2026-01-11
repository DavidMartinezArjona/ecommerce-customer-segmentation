🛒 Customer Segmentation and Churn Prediction in E-commerce
📌 Project Overview

This project presents an end-to-end data science pipeline applied to an e-commerce use case, covering:

Data cleaning and preprocessing of raw transactional data

Feature engineering at customer level

Customer segmentation using unsupervised learning (clustering)

Churn prediction using supervised machine learning models

Interpretation of results from a business perspective

The goal is to demonstrate how customer behavior can be modeled, segmented, and leveraged to predict churn, following best practices in data science and avoiding common pitfalls such as data leakage.

🎯 Business Problem

Customer churn is a critical challenge in e-commerce. Understanding which customers are likely to stop purchasing and how different behavioral segments behave enables:

Targeted retention strategies

Personalized marketing campaigns

More efficient allocation of marketing resources

This project addresses these challenges by combining customer segmentation with predictive modeling.

📊 Dataset

Source: Online Retail Dataset (UCI / Kaggle)

Description: Real transactional data from a UK-based online retailer

Period: December 2010 – December 2011

Granularity: Transaction-level data

Key challenges in the dataset:

Missing customer identifiers

Cancellations and product returns

Negative quantities and invalid prices

Strongly skewed monetary distributions

ecommerce-customer-segmentation/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_eda_and_cleaning.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_clustering.ipynb
│   └── 04_churn_prediction.ipynb
│
├── README.md
└── requirements.txt

🔄 Methodology
1. Data Cleaning & EDA

Removal of invalid records and duplicates

Explicit handling of missing CustomerID values

Identification of cancellations and returns as behavioral signals

Exploratory analysis of temporal and monetary patterns

📓 Notebook: 01_eda_and_cleaning.ipynb

2. Feature Engineering

Aggregation from transactions to customer-level features

Construction of classical RFM variables:

Recency

Frequency

Monetary value

Additional behavioral features:

Average basket size

Variability of spending

Return ratio

Average time between purchases

Log transformations and robust scaling to handle skewness and outliers

📓 Notebook: 02_feature_engineering.ipynb

3. Customer Segmentation (Clustering)

Unsupervised clustering using K-Means (baseline)

Objective selection of number of clusters using:

Elbow method

Silhouette score

Cluster interpretation based on customer behavior

Visualization of segments using PCA (for interpretability only)

📓 Notebook: 03_clustering.ipynb

4. Churn Prediction

Definition of churn using a future prediction window, avoiding data leakage

Supervised models:

Logistic Regression (baseline, interpretable)

Random Forest (non-linear model)

Evaluation using ROC-AUC and classification metrics

Comparison of models with and without cluster features

Feature importance analysis to interpret drivers of churn

📓 Notebook: 04_churn_prediction.ipynb

🧠 Key Results

Customer segmentation reveals clearly differentiated behavioral profiles

Churn is strongly influenced by:

Recency of last purchase

Purchase frequency

Customer segment membership

Including cluster information improves predictive performance

Even simple, interpretable models provide strong results when features are well designed

🛠️ Tech Stack

Language: Python

Data manipulation: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-learn

Methods:

Clustering (K-Means, GMM)

Classification (Logistic Regression, Random Forest)

🚀 How to Run the Project

Clone the repository

Install dependencies:

pip install -r requirements.txt


Run notebooks in order:

01_eda_and_cleaning.ipynb

02_feature_engineering.ipynb

03_clustering.ipynb

04_churn_prediction.ipynb

📌 Notes

The project strictly separates feature construction and target definition in time to prevent data leakage.

All modeling choices are justified from both a technical and business perspective.

The pipeline is designed to be easily extensible to production settings or additional models.

📬 Contact

If you have questions, suggestions, or would like to discuss this project, feel free to reach out.