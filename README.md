# CS-472-572-Final-Project

Public repository for our Spring 2026 CS 472/572 final project: "Human Activity Recognition via Unsupervised Clustering Methods."

## Project Overview

Human Activity Recognition (HAR) has become increasingly important in mobile health, elderly care, and personalized fitness because smartphones and wearable devices continuously collect accelerometer and gyroscope data. Since this type of data is high-dimensional and often contains non-linear relationships, unsupervised clustering can be difficult using only traditional linear methods.

This project compares the following clustering models on the UCI HAR dataset:
- K-Means
- Hierarchical Agglomerative Clustering
- Spectral Clustering
- DBSCAN
- Gaussian Mixture Models (GMM)

## Extensions
This project includes two extensions beyond the PCA baseline:
- Autoencoder (AE)
- Convolutional Variational Autoencoder (CVAE)

### Dataset:
-Original dataset source:
https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones
-For this project, we use the updated data files stored in the repository's dataset/ folder.

The dataset was collected from 30 subjects wearing a Samsung Galaxy S II smartphone on their waist
- Records: 10,299
- Features: 561
- Activities: 6
  - LAYING
  - SITTING
  - STANDING
  - WALKING
  - WALKING DOWNSTAIRS
  - WALKING UPSTAIRS

The original train and test data were combined for this unsupervised clustering study, while the labels were kept for Adjusted Rand Index (ARI).

## Google Colab Run Instructions

1. Open Project.ipynb in Google Colab.
2. Go to Runtime > Change runtime type.
3. Set Hardware accelerator to GPU.
4. Upload train.csv and test.csv before running the notebook.
5. Run the notebook from top to bottom.


## The following unsupervised clustering methods were tested:
### 1. K-Means
Baseline centroid-based clustering with n_clusters=6.

### 2. Hierarchical Agglomerative Clustering
Tested with four linkage types:
- Single
- Complete
- Average
- Ward

### 3. Spectral Clustering
Tested with:
- assign_labels = kmeans
- assign_labels = discretize

### 4. DBSCAN
Tested as a density-based clustering method with tuned parameters:
- eps = 11
- min_samples = 4

### 5. Gaussian Mixture Models(GMM)
Tested with four covariance types:
- Spherical
- Diagonal
- Tied
- Full

## Evaluation Metrics
- Silhouette Score
- Adjusted Rand Index (ARI)


