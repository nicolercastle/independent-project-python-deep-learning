Deep learning project comparing logistic regression, MLP, and CNN models for multiclass classification using Python.

# Python Deep Learning Independent Project

This repository contains the full code pipeline for an independent deep learning project completed during finals week. The goal was to use deep learning to analyze a real-world data set.  I compared logistic regression, multilayer perceptron (MLP), and convolutional neural network (CNN) models for multiclass classification using a real-world wine quality dataset.

## License and Usage
Note: All rights reserved.  This code is shared for educational and portfolio purposes only. Please do not reuse or redistribute without permission.

## Overview

- Built and compared three classification models: logistic regression, MLP, and CNN
- Applied PCA for dimensionality reduction and SMOTE for class balancing
- Evaluated performance using accuracy and validation loss
- Designed and trained deep learning architectures using TensorFlow/Keras
- Visualized performance metrics and model comparisons
- Delivered a reproducible pipeline and professional report

## Tools Used

- Python (`NumPy`, `pandas`, `scikit-learn`, `TensorFlow`/`Keras`, `matplotlib`, `imbalanced-learn`)
- Deep learning model architecture design and evaluation
- Data preprocessing, scaling, and encoding
- Dimensionality reduction (PCA) and class balancing (SMOTE)
- Performance metric visualization

## Dataset Source
Cortez, P., et al. (2009). Wine Quality [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C56S3T.
  
## Project Highlights

- Completed independently in under one week
- Received a final grade of 100%
- Emphasized reproducibility, interpretability, and thoughtful model comparison

## How to View

- The notebook includes all code, visualizations, and commentary
- Models are trained and evaluated in sequence, with performance metrics displayed throughout

## Results Summary

This project explored wine quality prediction using multiple deep learning architectures. While CNNs offered hierarchical feature extraction, PCA-based MLP models proved more stable and interpretable. Random Forest outperformed all deep learning models, highlighting the importance of feature structure in tabular datasets. The final PCA-based MLP (without learning rate scheduler) achieved 55.69% validation accuracy, and the CNN peaked at 56.77%, both significantly outperforming baseline models.

## Model Architectures

- **Logistic Regression**
  - Baseline model using linear classification
  - Achieved modest performance, limited by inability to capture non-linear feature interactions

- **Multilayer Perceptron (MLP)**
  - Four hidden layers: 128 → 64 → 32 → 16 neurons
  - ReLU activations and softmax output for multiclass classification
  - Initially trained on raw features, then retrained using PCA components
  - PCA-based MLP showed improved stability and performance over raw input MLP

- **Convolutional Neural Network (CNN)**
  - Two 1D convolutional layers with kernel size 2
  - MaxPooling1D layers to prevent feature collapse
  - Flattened output passed to dense layers for final classification
  - Designed to extract hierarchical feature relationships from structured tabular data

## Key Results

- **Random Forest (non-deep learning benchmark)**
  - Achieved highest validation accuracy: 68.00%
  - Demonstrated strong handling of feature importance and structured relationships

- **Logistic Regression**
  - Validation accuracy: 52.62%
  - Outperformed majority class baseline (42.31%) but limited by linear assumptions

- **MLP (raw features)**
  - Validation accuracy: 41.38%
  - Struggled with class imbalance and feature extraction

- **MLP (PCA-based)**
  - Validation accuracy: 55.69%
  - PCA improved learning stability and reduced feature redundancy

- **CNN**
  - Peak validation accuracy: 56.77%
  - Comparable to PCA-based MLP, but slightly less stable across iterations

- **SMOTE (oversampling)**
  - Validation accuracy dropped to 47.08%
  - Synthetic samples introduced noise, reducing generalization

**Final Recommendation**: PCA-based MLP was the most stable deep learning model. While CNN showed promise, PCA offered more consistent improvements for structured tabular data.



