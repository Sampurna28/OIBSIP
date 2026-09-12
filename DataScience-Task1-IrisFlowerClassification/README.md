# Iris Flower Classification

## Oasis Infobyte Data Science Internship — Task 1

## Project Overview

This project focuses on classifying iris flowers into three species:

- Setosa
- Versicolor
- Virginica

The classification is performed using machine learning models based on four physical measurements:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The Iris dataset is loaded directly from Scikit-learn using its built-in `load_iris()` dataset.

## Project Workflow

1. Load the Iris dataset
2. Create and inspect the dataset
3. Perform Exploratory Data Analysis (EDA)
4. Visualize feature distributions by species
5. Identify the most discriminative features
6. Split the data into training and testing sets
7. Train Logistic Regression and KNN classifiers
8. Evaluate both models
9. Compare model performance
10. Select the best-performing model
11. Predict the species of a new flower
12. Summarize the findings

## Exploratory Data Analysis

The dataset contains:

- 150 observations
- 4 numerical features
- 1 target variable
- No missing values
- 50 observations for each species

### Most Discriminative Features

Based on the visual analysis, **petal length** and **petal width** provide the clearest separation between the three iris species.

Sepal length also provides useful information, while sepal width shows comparatively more overlap.

## Machine Learning Models

Two classification algorithms were trained:

### 1. Logistic Regression

Test Accuracy: **96.67%**

### 2. K-Nearest Neighbors (KNN)

Test Accuracy: **100.00%**

## Model Comparison

| Model | Test Accuracy |
|---|---:|
| Logistic Regression | 96.67% |
| K-Nearest Neighbors (KNN) | 100.00% |

Based on the selected test set, **KNN was the best-performing model**.

## Predicted Species

A new flower was tested using the following measurements:

- Sepal Length: 5.1 cm
- Sepal Width: 3.5 cm
- Petal Length: 1.4 cm
- Petal Width: 0.2 cm

**Predicted Species: Setosa**

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

```text
DataScience-Task1-IrisFlowerClassification/
│
├── Iris_Flower_Classification.ipynb
├── README.md
└── screenshots/