# Fashion Outlier Detection using Unsupervised Learning Models

This project is done as part of my advanced machine learning course. This project applies unsupervised machine learning techniques to detect outliers in fashion product images using a subset of the Fashion-MNIST dataset. These outliers could represent mislabeled, low-quality, or unusual items, which can help in quality control, inventory checks, or product categorization for fashion retailers.

## Objectives
To identify fashion items that deviate significantly from normal product patterns using three key methods:
  - Principal Component Analysis (PCA)
  - K-Means Clustering
  - t-SNE (t-distributed Stochastic Neighbor Embedding)

The goal is not only to find anomalies, but also to compare how well each method performs, and evaluate how these insights might support business decisions.

## Dataset
- Original Dataset - https://www.kaggle.com/datasets/zalando-research/fashionmnist
- Fashion-MNIST is a curated dataset of Zalando’s fashion article images.
- 1210 grayscale images (28x28 pixels)
- 10 classes (T-shirt, Trouser, Pullover, etc.)

## Data Analysis Approach
1. PCA (Principal Component Analysis)
- Used for dimensionality reduction and reconstruction
- PCA effectively clustered majority of points
- Detected outliers primarily in classes 8 & 9 (Bag, Ankle Boot)

2. K-Means Clustering
- Clusters data in PCA-reduced space
- Detected 61 outliers
- Outliers scattered across multiple clusters
- Visualized using cluster scatter plots and product image previews

3. t-SNE (t-Distributed Stochastic Neighbor Embedding)
- High-dimensional visualization technique (non-linear)
- Provided rich visual separation of image classes
- Effective for pattern spotting, but computationally expensive

## Model Performance
| Model   | Mean Squared Reconstruction Error | Silhouette Score |
|---------|-----------------------------------|------------------|
| PCA     | 0.046                             | N/A              |
| K-Means | N/A                               | 0.430            |
| t-SNE   | N/A                               | N/A              |

- **PCA**  
  PCA is highly effective for dimensionality reduction and detecting outliers based on reconstruction error. With an MSRE of 0.046, it preserves most of the original data structure.

- **K-Means Clustering**  
  K-Means is scalable and interpretable, making it a practical tool for separating product types. The Silhouette Score of 0.43 suggests moderate cluster separation.

- **t-SNE**  
  t-SNE provides strong visual insights into data relationships. However, it's more useful for exploration than production due to high computational requirements and lack of clustering metrics.

## Insights 
Each method provides a different lens for anomaly detection—PCA for compression loss, K-Means for cluster deviation, and t-SNE for neighborhood dissimilarity. Combining insights from multiple methods leads to more robust anomaly detection. Some key insights:

- Early detection of visual anomalies can prevent customer dissatisfaction from mislabeled or defective products.
- Dimensionality reduction (PCA) helps compress image data with minimal loss, enabling faster ML pipelines.
- Clustering techniques like K-Means support product tagging, grouping, and recommendation filtering.

## Conclusion

This study demonstrated that combining different unsupervised outlier detection techniques (PCA, K-means, and t-SNE) can effectively identify and analyze anomalies in image data. The findings suggest that applying dimensionality reduction techniques and clustering methods can significantly improve the detection of outliers in image classification tasks, which is crucial for improving model accuracy and robustness in real-world applications.
