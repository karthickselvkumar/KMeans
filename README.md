# From-Scratch Implementation and Evaluation of K-Means Clustering

## Project Overview

This project presents a complete implementation of the **K-Means clustering algorithm** developed entirely from scratch using **NumPy**, without relying on scikit-learn’s clustering utilities. The goal is to understand the internal working principles of K-Means, including:

- Centroid initialization
- Distance computation
- Iterative updates
- Convergence criteria
- Evaluation using the **Elbow Method**

A synthetic multi-modal dataset is generated to validate the correctness and performance of the implementation.

---

## Objectives

- Generate a synthetic dataset with multiple well-separated clusters
- Implement the K-Means clustering algorithm using **NumPy only**
- Compute **Within-Cluster Sum of Squares (WCSS)** to evaluate clustering quality
- Apply the **Elbow Method** to determine the optimal number of clusters
- Analyze convergence behavior and final cluster structure

---

## Dataset Generation

- Generated using `sklearn.datasets.make_blobs`
- Number of samples: ~500
- Number of clusters: 4
- Clusters are well-separated to ensure stable convergence

> **Note:** scikit-learn is used only for dataset generation, as permitted.

---

## K-Means Algorithm Implementation

### 1. Initialization
Centroids are initialized randomly by selecting data points from the dataset.

### 2. Distance Calculation
Euclidean distance is used to assign each data point to the nearest centroid.

### 3. Centroid Update
Centroids are recalculated as the mean of all points assigned to each cluster.

### 4. Convergence Criterion
The algorithm terminates when centroid positions change below a predefined tolerance or when a maximum number of iterations is reached.

---

## Elbow Method (WCSS Evaluation)

- Tested K values range from 1 to 10
- For each K, the K-Means algorithm is executed
- **Within-Cluster Sum of Squares (WCSS)** is calculated and recorded
- The optimal number of clusters is determined by identifying the elbow point in the WCSS curve

---

## Final Clustering Execution

- K-Means is executed using the optimal K value
- Final centroid coordinates are computed after convergence
- Each data point is assigned a final cluster label

---

## Output and Results

### Textual Output
- WCSS values for all tested K values
- Final centroid coordinates
- Cluster assignment summary

### Visualization
- **Elbow curve** showing WCSS versus number of clusters
- **Scatter plot** of final clusters with centroids

---

## Analysis and Observations

- Random initialization influences convergence speed and final centroids
- Well-separated clusters result in stable convergence
- The Elbow Method effectively identifies the optimal number of clusters
- Vectorized **NumPy** operations improve computational efficiency

---

## Technologies Used

- Python
- NumPy
- Matplotlib
- scikit-learn (dataset generation only)
- Jupyter Notebook

---

## Project Structure

├── kmeans(1).ipynb
└── README.md
## Conclusion

This project demonstrates a low-level, practical understanding of unsupervised learning by implementing K-Means clustering without using pre-built clustering libraries. The results validate the correctness of the implementation and highlight the importance of **initialization** and **evaluation strategies**.

---

## Author

**Karthik Selvakumar**
