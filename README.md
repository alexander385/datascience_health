# Supply Chain Machine Learning Analysis

## Overview
This project applies **Machine Learning (ML) techniques** to a dataset from a **solder paste inspection process** in supply chain management. The dataset includes quality inspection data, machine performance, and board-specific attributes. The goal is to **predict soldering quality issues** using classification models and analyze key influencing factors.

## Dataset Description
The dataset contains **891 observations** with the following variables:

| Variable | Description |
|----------|-------------|
| **ID** | Running number (unique identifier) |
| **QI** | Quality Inspection at the end (1 = nIO (not okay), 0 = iO (okay)) |
| **Machine** | Machine ID performing soldering |
| **PreCheck** | Initial quality check before soldering (1 = nIO, 0 = iO) |
| **NumberPins** | Number of pins per board |
| **BoardID** | Board identifier |
| **Price** | Final price in Euros |
| **BoardCategory** | Board classification (not further specified) |
| **MaterialOrigin** | Origin of solder paste (S = Singapore, C = China, Q = Qatar) |

## Machine Learning Models Used
The following classification models were applied to predict **QI (Quality Inspection result)**:

1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**

Additionally, **K-Means Clustering** was used to group boards based on price and number of pins.

## Preprocessing Steps
- Converted categorical variables into appropriate formats.
- Handled missing values using mean/mode imputation.
- Identified and treated outliers using **Interquartile Range (IQR)**.
- Scaled numerical features where necessary.

## Model Evaluation
Each ML model was evaluated using the following metrics:

- **Accuracy**: Measures overall correctness.
- **Precision**: Proportion of predicted positives that are actually positive.
- **Recall (Sensitivity)**: Proportion of actual positives that are correctly predicted.
- **F1 Score**: Harmonic mean of Precision and Recall.
- **Error Rate**: Proportion of incorrect predictions.

### **Comparison of Classification Methods**

| Model               | Accuracy | Precision | Recall | F1 Score | Error Rate |
|----------------------|----------|-----------|--------|----------|------------|
| **Logistic Regression** | 0.80 | 0.81 | 0.67 | 0.73 | 0.20 |
| **Decision Tree**       | 0.75 | 0.72 | 0.63 | 0.67 | 0.25 |
| **Random Forest**       | 0.76 | 0.75 | 0.63 | 0.69 | 0.24 |

## Visualizations
- **Confusion Matrices**: Heatmaps for each model's classification results.
- **Feature Importance (Random Forest)**: Visualizing key variables influencing predictions.
- **Decision Tree Structure**: Graphical representation of the decision-making process.
- **Box Plots & Histograms**: Outlier detection and feature distribution.

