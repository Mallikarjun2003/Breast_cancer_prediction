# Breast Cancer Prediction using Logistic Regression

## Introduction

This repository contains code for predicting breast cancer using logistic regression. The dataset used for this task contains various features computed for each cell nucleus from breast cancer biopsies.

Breast cancer is a type of cancer that develops in the breast tissue. It occurs when breast cells grow uncontrollably and form a malignant tumor. There are different types of breast cancer, including Ductal Carcinoma In Situ (DCIS), Invasive Ductal Carcinoma (IDC), and Invasive Lobular Carcinoma (ILC).

## Dataset Description

The dataset includes the following information:

1. ID number
2. Diagnosis (M = malignant, B = benign)
3-32) Ten real-valued features computed for each cell nucleus:

    - a) radius (mean of distances from center to points on the perimeter)
    - b) texture (standard deviation of gray-scale values)
    - c) perimeter
    - d) area
    - e) smoothness (local variation in radius lengths)
    - f) compactness (perimeter^2 / area - 1.0)
    - g) concavity (severity of concave portions of the contour)
    - h) concave points (number of concave portions of the contour)
    - i) symmetry
    - j) fractal dimension ("coastline approximation" - 1)

The mean, standard error, and "worst" or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is Radius SE, field 23 is Worst Radius.

The dataset has been sourced from Kaggle. You can find the dataset [here](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data).

## Explanation of Metrics

- **Radius**: Mean of distances from the center to points on the perimeter. Larger values indicate larger tumor size.
- **Texture**: Standard deviation of gray-scale values. Higher values indicate greater variation in texture.
- **Perimeter**: Perimeter of the tumor. Larger perimeters indicate larger tumor size.
- **Area**: Area of the tumor. Larger areas indicate larger tumor size.
- **Smoothness**: Local variation in radius lengths. Smoother tumors have lower values.
- **Compactness**: Measure of compactness (perimeter^2 / area - 1.0). Higher values indicate more irregular shapes.
- **Concavity**: Severity of concave portions of the contour. Higher values indicate more concave shapes.
- **Concave Points**: Number of concave portions of the contour. Higher values indicate more concave shapes.
- **Symmetry**: Symmetry of the tumor. Values closer to 1 indicate more symmetric tumors.
- **Fractal Dimension**: "Coastline approximation" - 1. Higher values indicate more complex shapes.

## Interpretation of Results

The logistic regression model achieved an accuracy of 98% on the test set. The confusion matrix and classification report provide insights into the performance of the model.

## Usage

To use the trained model for making predictions on new data:

1. Preprocess the new data by scaling it using the same `StandardScaler` instance used during training.
2. Use the `predict` method of the trained logistic regression model to obtain predictions.

This README file provides an overview of breast cancer, an explanation of each metric used in the dataset, interpretation of the results, and information on how to use the trained model for making predictions. Adjust the content as needed to suit your specific requirements.
