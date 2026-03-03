🛒 Customer Segmentation & Churn Prediction (E-Commerce)
📌 Overview

End-to-end Data Science project using real e-commerce transactional data.

The project covers:

Data cleaning and preprocessing

Customer-level feature engineering

Customer segmentation (unsupervised learning)

Churn prediction (supervised learning)

Business interpretation of results

The goal is to model customer behavior and identify churn risk using robust feature design and proper validation techniques.

🎯 Business Objective

In e-commerce, retaining customers is more cost-effective than acquiring new ones.

This project answers:

Can we identify distinct customer segments?

Can we predict which customers are likely to churn?

Results can support:

Targeted retention strategies

Personalized marketing campaigns

Efficient resource allocation

📊 Dataset

Source: Online Retail Dataset (UCI / Kaggle)

Period: 2010–2011

Type: Transaction-level data

Main challenges addressed:

Missing customer IDs

Returns and cancellations

Skewed monetary distributions

🔄 Methodology
1️⃣ Data Cleaning & EDA

01_eda_and_cleaning.ipynb

Removal of invalid transactions

Handling missing values

Creation of total transaction value

2️⃣ Feature Engineering

02_feature_engineering.ipynb

Customer-level aggregation including:

Recency

Frequency

Monetary value

Basket metrics

Return ratio

Log transformation and scaling applied to handle skewness.

3️⃣ Customer Segmentation

03_clustering.ipynb

K-Means clustering

Elbow & Silhouette methods

PCA visualization

Business interpretation of segments

4️⃣ Churn Prediction

04_churn_prediction.ipynb

Time-based churn definition (no data leakage)

Logistic Regression

Random Forest

ROC-AUC evaluation

Feature importance analysis

🧠 Key Insights

Clear behavioral segments emerge from transactional data

Recency and frequency strongly influence churn

Including cluster membership improves prediction

Well-designed features outperform complex models

🛠️ Tech Stack

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

🚀 How to Run
pip install -r requirements.txt

Run notebooks in order from 01 to 04.

📌 Notes

Data leakage is explicitly avoided.

Modeling decisions are driven by both technical and business considerations.
