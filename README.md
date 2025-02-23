# Wine-Quality-Feature-Selection-and-Model-Optimization

## Overview

This project focuses on **feature selection techniques** to enhance machine learning model performance on the **White Wine Quality dataset** from the **UCI Machine Learning Repository**. The dataset contains 11 chemical properties of white wine, and our goal is to identify the most relevant features that influence wine quality ratings.

## Dataset

- **Name**: White Wine Quality
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
- **Description**: The dataset consists of 11 input features (e.g., acidity, sugar, pH, etc.) and 1 target variable (wine quality, rated from 0 to 10).

## Tasks Performed

### 1. Data Preprocessing

- Checked for missing values.
- Analyzed the distribution of the target variable.
- Normalized the dataset (if necessary).
- Split the dataset into **training (80%)** and **testing (20%)** sets.

### 2. Feature Selection Techniques

#### **Filter Methods**

- **Low Variance Filter**: Removed features with very low variance.
- **Pearson’s Correlation**:
  - Computed correlation coefficients.
  - Visualized correlations using a heatmap.
  - Removed features with low correlation with wine quality.
  - Used **Variance Inflation Factor (VIF)** to detect multicollinearity.
- **Mutual Information**:
  - Computed mutual information scores.
  - Selected the top 5 most informative features.

#### **Wrapper Methods**

- **Forward Feature Selection**: Iteratively added features until model performance stopped improving.
- **Backward Feature Elimination**: Started with all features and iteratively removed the least important ones.

#### **Embedded Methods**

- **Lasso Regression (L1 Regularization)**: Selected features based on non-zero coefficients in Lasso regression.

### 3. Performance Comparison

- Compared the number of features selected by each method.
- Evaluated model performance using:
  - **Accuracy**
  - **Precision**
  - **Recall**
  - **F1-score**
- Identified the most effective feature selection technique.

## Results

- The best feature selection method was **Forward Selection**, as it provided the highest model accuracy while minimizing feature redundancy.
- The final model achieved an accuracy of **52.14%**.

## How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/humayun-raza-030/wine-quality-feature-selection.git
   ```
