An investigation into unsupervised machine Learning for predicting customer segment: Autoencoder method


🎯 Project Overview
This project explores an advanced unsupervised machine learning approach for Customer Segmentation using Autoencoders and K-means Clustering. The goal is to uncover distinct, actionable customer groups from a firm's purchase behavior data, leading to more targeted marketing strategies and a deeper understanding of the customer base.

This notebook demonstrates the methodology, implementation, and comparison of autoencoder-based clustering against traditional techniques, highlighting the advantages of using deep learning for feature representation and dimensionality reduction prior to clustering.

🛠️ Methodology & Workflow

The core of the project involves training an autoencoder to learn a compact, meaningful representation of the customer data, which is then used for clustering.

The workflow followed is:

Data Loading & Initial EDA: Load the marketing_campaign.csv dataset and perform initial checks for missing values and data types.

Data Preprocessing: Handle missing values, encode categorical features (like Education and Marital_Status), scale numerical features, and engineer new features (e.g., Age, Spent, Family Size).

Dimensionality Reduction: Apply Principal Component Analysis (PCA) for visualization and as a baseline comparison to the autoencoder's learned features.

Autoencoder Training: Build and train a deep Autoencoder model (and a Variational Autoencoder - VAE) to compress the high-dimensional feature space into a low-dimensional latent space.

Clustering: Apply K-means Clustering (after determining the optimal number of clusters using the Elbow Method) to the encoded data representations.

Evaluation & Comparison: Evaluate the clustering performance using metrics like Silhouette Score and Calinski-Harabasz Index. Compare the results from Autoencoder/VAE clustering with traditional methods (PCA + K-means, DBSCAN, Hierarchical Clustering).

✨ Key Findings

The project identified four distinct customer segments, with the Autoencoder PCA approach yielding the best performance metrics (Silhouette Score: 0.463 and Calinski-Harabasz Index: 2401.5).

The identified clusters are profiled as follows:

Cluster 0 (Budget Buyers): Low Spending and Low Income. Majority are parents, with up to 5 family members.

Cluster 1 (Mid-Range Families): Average Spending and Average Income. Definitely parents, with up to 4 family members.

Cluster 2 (Affluent Singles): High Spending and High Income. Definitely not parents, with up to 2 family members.

Cluster 3 (High Value/Average Income): High Spending and Average Income. Definitely not parents, with up to 3 family members.

These profiles provide clear targets for personalized marketing and product development efforts.
