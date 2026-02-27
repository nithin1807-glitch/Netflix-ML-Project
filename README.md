# 🎬 Netflix Movies and TV Shows Clustering - Unsupervised Machine Learning

## 📝 Project Overview
Netflix is the world's leading streaming entertainment service with millions of subscribers globally. As their content library expands rapidly, manually categorizing and recommending content becomes increasingly inefficient. 

The objective of this Capstone Project is to analyze Netflix's vast catalog and apply **Unsupervised Machine Learning (Clustering)** to group similar movies and TV shows. By leveraging **Natural Language Processing (NLP)** on content descriptions and metadata, this project automates the segmentation of the platform's library, enabling more robust recommendation engines and strategic content planning.

## 🎯 Business Objective
* Explore historical trends in content production (Movies vs. TV Shows).
* Understand regional content availability and genre popularity.
* Create distinct, actionable content clusters to improve UI lane generation, targeted marketing, and personalized user recommendations.

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Natural Language Processing (NLP):** NLTK (Tokenization, Lemmatization, POS tagging, Stopwords)
* **Machine Learning:** Scikit-Learn (TF-IDF, TruncatedSVD, K-Means Clustering)
* **Deployment Readiness:** Joblib (Model serialization)

## ⚙️ Project Pipeline
1. **Exploratory Data Analysis (EDA):** Visualized content distributions, release year trends, rating proportions, and geographical data. Conducted hypothesis testing (Chi-Square, T-Tests) to statistically validate business trends.
2. **Data Wrangling & Feature Engineering:** Handled missing values through logical imputation. Engineered new features like `content_age` to capture content freshness.
3. **Text Preprocessing (NLP):** Cleaned textual data (descriptions, genres, cast) by expanding contractions, removing punctuation, handling stop words, and applying Lemmatization.
4. **Vectorization & Dimensionality Reduction:** Converted the cleaned text corpus into a numerical matrix using **TF-IDF** (generating 5,000 features). Applied **TruncatedSVD** to reduce the sparse matrix down to 100 dense principal components, eliminating noise and improving computational efficiency.
5. **Clustering:** Deployed the **K-Means** algorithm. Utilized the **Elbow Method** to dynamically determine the optimal number of clusters ($K=5$).
6. **Evaluation:** Validated the mathematical density and separation of the clusters using the **Silhouette Score** and the **Davies-Bouldin Score**.

## 📊 Key Business Insights & Cluster Strategies
The algorithm successfully segmented the Netflix library into 5 highly actionable business lanes:

* **Cluster 0 (Mature Dramas & Docs):** Content rated TV-MA, highly focused on Documentaries and International Dramas. *Strategy:* Target this lane toward adult users who prefer serious, critically acclaimed, or educational content.
* **Cluster 1 (Teen/Family Mix):** TV-14 rated Comedies and Children's movies. *Strategy:* Ideal for promoting "Family Movie Night" categories and general audience recommendations.
* **Cluster 2 (Quick Entertainment):** The largest segment, heavily featuring Stand-Up Comedy and Kids' TV. *Strategy:* Represents highly bingeable, shorter-attention-span content. Push this to mobile users or casual viewers.
* **Cluster 3 (Niche Mix):** A smaller crossover segment of Stand-Up and Kids' TV. *Strategy:* Useful for households with diverse viewing profiles.
* **Cluster 4 (General Audience Dramas):** TV-14 International Dramas and Comedies. *Strategy:* Serve as a strong default recommendation block for new users testing the platform.

## 🚀 Deployment 
To ensure production readiness, the complete preprocessing pipeline (`TF-IDF Vectorizer`, `TruncatedSVD`) and the final `K-Means Model` have been serialized using `Joblib`. A sanity check script is included to demonstrate how the live server can ingest a new, unseen movie description and instantly assign it to the correct business cluster.

## 📂 Repository Contents
* `Copy_of_Sample_ML_Submission_Template.ipynb`: The complete, commented, and executable Jupyter/Colab notebook containing the end-to-end pipeline.
* `Video_Presentation.mp4`: A 7-minute executive summary and technical walkthrough of the project and its business impact.
* `netflix_best_model.pkl`: The serialized models ready for deployment.
