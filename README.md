# CMPE-255-Short-Story

# Machine Learning for Customer Segmentation Using K-Means Clustering

**Author:** Olivia Hunter  
**Project Type:** Individual Short Story Assignment

## 1. Project Overview

This project explores how K-Means clustering can help businesses group customers based on annual income and spending behavior. Using the Mall Customer Segmentation dataset, I applied unsupervised machine learning to identify patterns among customers.

The experiment compares different numbers of clusters to understand how the choice of K affects cluster quality and customer segmentation.

## 2. Research Question

How can K-Means clustering help businesses group customers based on behavior and spending?

## 3. Objectives

- Understand how K-Means clustering works.
- Group customers using annual income and spending score.
- Compare K values of 2, 3, 4, and 5.
- Evaluate clustering using inertia and silhouette scores.
- Visualize and interpret the resulting customer groups.
- Explore the limitations of K-Means for customer segmentation.

## 4. Dataset

**Dataset:** Mall Customer Segmentation  
**Source:** [Kaggle — Customer Segmentation Tutorial in Python](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

The original dataset contained 200 customer records. After checking the selected features for missing or invalid values, all 200 records were retained.

### Selected Features

- **Annual Income (k$):** Customer annual income in thousands of dollars.
- **Spending Score (1–100):** Customer spending score.

These features were selected to explore whether customers with similar income levels exhibit different spending behaviors.

## 5. Methodology

The experiment followed these steps:

1. Loaded and inspected the dataset.
2. Selected annual income and spending score.
3. Checked for missing or invalid values in the selected features.
4. Standardized the features using `StandardScaler`.
5. Trained K-Means models with K = 2, 3, 4, and 5.
6. Used `random_state=42` and `n_init=10`.
7. Compared inertia and silhouette scores.
8. Visualized the clusters and examined their mean income and spending scores.

## 6. Experimental Results

### Evaluation Metrics

| K | Inertia | Silhouette Score |
|---:|---:|---:|
| 2 | 269.6910 | 0.3213 |
| 3 | 157.7040 | 0.4666 |
| 4 | 108.9213 | 0.4939 |
| 5 | 65.5684 | 0.5547 |

The inertia decreased as the number of clusters increased. The elbow graph suggested that K = 3 was a reasonable simpler candidate, although the elbow was not completely clear. K = 5 achieved the highest silhouette score among the tested values.

The elbow and silhouette methods did not identify the same preferred number of clusters.

### Cluster Profiles for K = 5

| Cluster | Customer Count | Mean Annual Income (k$) | Mean Spending Score |
|---:|---:|---:|---:|
| 0 | 81 | 55.30 | 49.52 |
| 1 | 39 | 86.54 | 82.13 |
| 2 | 22 | 25.73 | 79.36 |
| 3 | 35 | 88.20 | 17.11 |
| 4 | 23 | 26.30 | 20.91 |

The clusters showed different combinations of income and spending. For example, Cluster 3 had high mean income but low spending, while Cluster 2 had lower mean income but high spending. This suggests that income alone does not explain customer spending behavior.

### Visualizations

The experiment produces the following figures:

- Elbow Method Graph
- Silhouette Score Graph
- Customer Cluster Visualizations for K = 2, 3, 4, and 5

## 7. Limitations

This experiment uses only two features and does not have ground-truth customer segment labels. Adding other features, such as age or purchase history, could produce different clusters. Results may also be affected by centroid initialization and outliers. Alternative methods, such as K-Medoids or hierarchical clustering, could provide different groupings.

The clusters should be interpreted as exploratory patterns rather than definitive customer categories.

## 8. Future Work

Future experiments could:

- Test additional values of K.
- Compare K-Means with other clustering algorithms.
- Include more customer features.
- Examine how outliers affect the clusters.
- Investigate whether the identified groups are useful for specific business decisions.

## 9. Files

- **Notebook:** https://colab.research.google.com/drive/1bGRp2SA5z-E9lYqvjH8OgVl9wYvYdTJD#scrollTo=1b253f41
- **Short Story PDF:** `report/kmeans_short_story.pdf`
- **Figures:** `figures/`
- **Presentation Slides:** `slides/`
- **Youtube Link:** https://youtu.be/lI7I9OMcIO4

## 10. Deliverables

| Deliverable | Link/Location | Completion |
|---|---|---|
| **Medium Article** | [Read Article](https://medium.com/@olhunter03/machine-learning-for-customer-segmentation-exploring-k-means-clustering-f210fdbf5de1) | ✅ Complete |
| **Slide Presentation PDF** | In "Slides Folder" | ✅ Complete |
| **10–15 Minute Video** | https://youtu.be/lI7I9OMcIO4 | ✅ Complete |
| **SlideShare Presentation** | Pending | ⏳ Pending |

## 11. References

1. Ikotun, A. M., Ezugwu, A. E., Abualigah, L., Abuhaija, B., & Heming, J. (2023). *K-means clustering algorithms: A comprehensive review, variants analysis, and advances in the era of big data*. *Information Sciences, 622*, 178–210. https://doi.org/10.1016/j.ins.2022.11.139

2. Liu, Y., & Huang, S. (2025, January 7). *A survey on K-means clustering algorithms: Theoretical analysis and performance comparison* [PDF]. https://knightnemo.github.io/assets/files/clustering.pdf

3. Kaggle. (n.d.). *Customer segmentation tutorial in Python* [Dataset]. https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-pythonkm
