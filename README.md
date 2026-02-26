🎬 Netflix Movies & TV Shows Clustering Project
📌 Project Overview

This project performs unsupervised machine learning on the Netflix Movies & TV Shows dataset to discover hidden content patterns and group similar titles together.

The objective is to cluster Netflix content based on textual similarity using Natural Language Processing (NLP) techniques and KMeans clustering.

🎯 Business Objective

Automatically group similar content

Understand content similarity patterns

Support recommendation system foundation

Assist strategic content categorization

This project demonstrates how Netflix-like platforms can use clustering to analyze large-scale content libraries.

📊 Dataset Information

Dataset: Netflix Movies and TV Shows
Features used:

Title

Director

Cast

Country

Listed_in (Genre)

Description

Textual features were combined and processed for clustering.

🛠️ Technologies & Libraries Used

Python

Pandas

NumPy

Matplotlib

Scikit-learn

XGBoost (initial experimentation)

Joblib

🔎 Project Workflow
1️⃣ Data Preprocessing

Removed missing values

Feature engineering

Combined important text columns

Text cleaning

2️⃣ Feature Engineering (NLP Pipeline)

TF-IDF Vectorization
Converts text into numerical feature vectors.

Truncated SVD
Reduces high-dimensional TF-IDF features into lower dimensions for efficient clustering.

3️⃣ ML Model Implementation
✅ KMeans Clustering

KMeans algorithm was used to group similar Netflix titles by minimizing within-cluster variance (WCSS).

Why KMeans?

Works well with high-dimensional text features

Efficient for large datasets

Suitable for unsupervised learning tasks

📈 Model Evaluation

Since clustering is unsupervised, traditional metrics like Accuracy, Precision, Recall, and F1-score are not applicable.

The following evaluation methods were used:

🔹 Elbow Method

Used to determine optimal number of clusters by analyzing WCSS.

🔹 Silhouette Score

Silhouette Score achieved:

0.3748

This indicates moderate cluster separation and reasonable grouping quality.

💾 Model Saving for Deployment

The complete clustering pipeline was saved using Joblib:

netflix_tfidf_vectorizer.pkl

netflix_svd_model.pkl

netflix_kmeans_model.pkl

These components together form the deployment-ready clustering pipeline.

To predict cluster for new content:

Text → TF-IDF → SVD → KMeans → Cluster ID

🚀 How to Run the Project

Clone the repository

Install required libraries

Open NETFLIX_PROJECT.ipynb

Run all cells

Load saved models for prediction

📌 Key Insights

Content similarity is heavily influenced by genre and description text.

Dimensionality reduction significantly improves clustering efficiency.

Clustering can be extended for recommendation systems.

🔮 Future Improvements

Improve cluster quality using advanced embedding models (Word2Vec, BERT)

Perform cluster labeling and interpretation

Build a recommendation engine on top of clusters

Deploy using Flask / Streamlit

🎓 Conclusion

This project demonstrates a complete end-to-end machine learning pipeline:

Data Cleaning → NLP Processing → Feature Engineering → Clustering → Evaluation → Deployment Preparation

It showcases practical implementation of unsupervised learning in real-world content analysis scenarios.

⭐ Author

Nithin
Machine Learning Enthusiast
