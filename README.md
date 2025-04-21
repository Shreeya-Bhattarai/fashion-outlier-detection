# Outlier Detection on Fashion-MNIST using PCA, K-Means & t-SNE

## Objective
This project was done as part of my advanced machine learning course. The goal of this project is to apply unsupervised machine learning techniques — PCA, K-Means Clustering, and t-SNE — to detect outliers in a modified Fashion-MNIST dataset. The aim is to understand how each model identifies unusual patterns and compare their performance in a high-dimensional image dataset.

## Dataset
- Original Dataset - https://www.kaggle.com/datasets/zalando-research/fashionmnist
- Fashion-MNIST (a sample from the original with added outliers)
- 1210 grayscale images (28x28 pixels)
- 10 classes (T-shirt, Trouser, Pullover, etc.)

## Key Findings:
  - PCA was the most effective for dimensionality reduction and identifying outliers based on reconstruction error.
  - K-means clustering identified clusters and outliers but showed limitations in the silhouette score, which indicated some overlap between clusters.
  - t-SNE provided valuable 2D visualization, but it was computationally intensive, making it less ideal for large-scale datasets.

## Conclusion:
This study demonstrated that combining different unsupervised outlier detection techniques (PCA, K-means, and t-SNE) can effectively identify and analyze anomalies in image data. The findings suggest that applying dimensionality reduction techniques and clustering methods can significantly improve the detection of outliers in image classification tasks, which is crucial for improving model accuracy and robustness in real-world applications.
