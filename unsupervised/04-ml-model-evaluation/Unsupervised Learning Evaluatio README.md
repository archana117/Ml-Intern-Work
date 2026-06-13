Unsupervised Learning Evaluation Using K-Means Clustering
Project Overview

This project performs customer-independent clustering using the K-Means algorithm and evaluates the clustering quality using various unsupervised learning metrics.

Dataset

Dataset Name: Wine Dataset

Source: Scikit-Learn Built-in Dataset

Dataset Description

The Wine Dataset contains chemical analysis data for wines derived from three different cultivars grown in Italy.

Total Samples: 178
Features: 13
Classes: 3 (used only for reference; not used during clustering)
Feature Examples
Alcohol
Ash
Magnesium
Color Intensity
Proline
Technologies Used
Python
Scikit-Learn
NumPy
Algorithm

K-Means Clustering

Evaluation Metrics
1. Silhouette Score

Measures how similar an object is to its own cluster compared to other clusters.

Range: -1 to 1
Higher value indicates better clustering.
2. Davies-Bouldin Index

Measures cluster separation and compactness.

Lower value indicates better clustering.
3. Calinski-Harabasz Score

Measures the ratio of between-cluster dispersion to within-cluster dispersion.

Higher value indicates better clustering.
4. Inertia

Measures the sum of squared distances of samples to their nearest cluster center.

Lower value indicates tighter clusters.
Workflow
Load Wine Dataset.
Standardize features.
Apply K-Means Clustering.
Generate cluster labels.
Evaluate clustering quality using unsupervised metrics.
Expected Outcome

The project demonstrates how clustering algorithms can group similar data points without labeled outputs and how clustering quality can be assessed using unsupervised evaluation metrics.
