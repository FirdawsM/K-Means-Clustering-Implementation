# K-Means Clustering Implementation

## Overview
This project implements the K-Means clustering algorithm from scratch in Python, including enhancements like K-Means++ initialization, handling empty clusters, and the elbow method for optimal k.


## Getting Started

### Prerequisites
List the software and libraries required to run your project. Include installation instructions:
- Python 3.x
- NumPy
- Matplotlib
- scikit-learn

### Installation
Follow these steps to set up your environment and run the code:

1. **Clone the repository** or **download the code** to your local machine:
   ```
   git clone https://github.com/FirdawsM/K-Means-Clustering-Implementation.git

2. Navigate to the project directory.
3. Install the required packages.
 
 ```
    pip install -r requirements.txt
```

### Usage
from kmeans import KMeans  # Replace 'kmeans' with the actual module name if different
 from sklearn.datasets import make_blobs

# Generate synthetic data
  X, true_labels = make_blobs(n_samples=300, centers=4, random_state=42)

# Instantiate and fit the KMeans model
  kmeans = KMeans(k=4)
  cluster_assignments, centroids = kmeans.fit(X)

# Visualize the results
 import matplotlib.pyplot as plt

 plt.scatter(X[:, 0], X[:, 1], c=cluster_assignments, s=30, cmap='viridis')
 plt.scatter(centroids[:, 0], centroids[:, 1], s=300, c='red', marker='X', label='Centroids')
 plt.title("K-Means Clustering Results")
 plt.xlabel("Feature 1")
 plt.ylabel("Feature 2")
 plt.legend()
 plt.show()
