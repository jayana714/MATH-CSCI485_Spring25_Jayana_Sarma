# **PCA and t-SNE for Dimensionality Reduction on Wine Quality Dataset**

## **Introduction to PCA and t-SNE**
Dimensionality reduction techniques, such as **Principal Component Analysis (PCA)** and **t-Distributed Stochastic Neighbor Embedding (t-SNE)**, are essential for visualizing high-dimensional data in lower dimensions. These techniques help to simplify complex data while preserving its underlying structure. PCA is a linear technique that focuses on maximizing variance, whereas t-SNE is a non-linear technique that preserves local structures.

## **Overview**
This project applies Principal Component Analysis (PCA) and t-SNE to the Wine Quality dataset to reduce its dimensionality and visualize the data in 2D. The goal is to compare how these techniques handle the high-dimensional dataset in terms of clustering and interpretability.

## **Requirements**
To run this project, you will need to install the following dependencies:
- `scikit-learn` (for PCA, t-SNE, and dataset handling)
- `matplotlib` (for visualizations)
- `seaborn` (for enhanced plotting)
- `pandas` (for data manipulation)

## **Wine Quality Dataset**
The dataset consists of chemical properties of wine samples and their quality ratings, as follows:
- **Fixed Acidity**: Citric acid (g/dm³)
- **Volatile Acidity**: Acetic acid (g/dm³)
- **Citric Acid**: Citric acid (g/dm³)
- **Residual Sugar**: Residual sugar (g/dm³)
- **Chlorides**: Chlorides (g/dm³)
- **Free Sulfur Dioxide**: Free sulfur dioxide (mg/dm³)
- **Total Sulfur Dioxide**: Total sulfur dioxide (mg/dm³)
- **Density**: Density (g/cm³)
- **pH**: pH level
- **Sulphates**: Sulphates (g/dm³)
- **Alcohol**: Alcohol percentage (%)
- **Quality**: Quality rating (scale from 0 to 10)

## **Project Steps**

1. **Data Preprocessing**:
   - Load and merge the red and white wine datasets.
   - Normalize the dataset, excluding the target variable 'quality'.
   - Handle any missing data if necessary.

2. **Applying PCA**:
   - Perform PCA to reduce the dataset to 2D while retaining the maximum variance.
   - Visualize the results with scatter plots, using colors to differentiate wine types (red or white).
   - Compare the results of PCA with t-SNE to assess the interpretability and clustering performance.

3. **Applying t-SNE**:
   - Apply t-SNE for non-linear dimensionality reduction to project the data into 2D.
   - Visualize the results and compare them with PCA-based visualizations.
   
4. **Comparison and Analysis**:
   - Compare the cluster separation and interpretability of PCA and t-SNE.
   - Discuss the advantages and limitations of each method in terms of preserving the structure of the data.


