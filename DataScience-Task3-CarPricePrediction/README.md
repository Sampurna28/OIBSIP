# Car Price Prediction with Machine Learning

## Overview

This project predicts the selling price of used cars using machine learning regression techniques.

The analysis uses vehicle characteristics such as brand, model, vehicle age, kilometers driven, fuel type, transmission, mileage, engine size, maximum power, and number of seats.

## Objective

The objective is to build regression models that can predict used-car selling prices and compare their performance using MAE, RMSE, and R² score.

## Dataset

The project uses the CarDekho used-car dataset.

The dataset contains information about used vehicles, including:

- Car name
- Brand
- Model
- Vehicle age
- Kilometers driven
- Seller type
- Fuel type
- Transmission type
- Mileage
- Engine
- Maximum power
- Seats
- Selling price

## Data Cleaning

The following preprocessing steps were performed:

- Inspected the dataset structure and data types.
- Checked for missing values.
- Checked for duplicate records.
- Standardized inconsistent brand names such as `ISUZU`.
- Removed records containing invalid zero-seat values.
- Removed the unnecessary `Unnamed: 0` column.

After cleaning, the dataset contained 15,409 records and 13 columns.

## Exploratory Data Analysis

The following analyses were performed:

1. Distribution of selling prices
2. Selling price by fuel type
3. Selling price versus vehicle age
4. Numerical feature correlation analysis
5. Feature importance analysis

### Key EDA Findings

- Selling prices are strongly right-skewed.
- Petrol and diesel vehicles have wider price distributions.
- Vehicle age generally has a negative relationship with selling price.
- `max_power` has the strongest numerical correlation with selling price.
- `engine` also has a substantial positive relationship with selling price.

## Feature Preparation

The target variable is:

`selling_price`

The following predictors were used:

- Brand
- Model
- Vehicle age
- Kilometers driven
- Seller type
- Fuel type
- Transmission type
- Mileage
- Engine
- Maximum power
- Seats

The `car_name` feature was excluded because brand and model already represent the vehicle identity while avoiding a very high-cardinality categorical feature.

Categorical variables were transformed using One-Hot Encoding.

The dataset was divided into:

- 80% training data
- 20% testing data

## Machine Learning Models

Two regression models were trained:

### 1. Linear Regression

Linear Regression was used as the baseline model.

### 2. Random Forest Regressor

Random Forest was used to capture nonlinear relationships between vehicle characteristics and selling price.

## Model Performance

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | ₹255,245.93 | ₹447,947.93 | 0.6732 |
| Random Forest Regressor | ₹93,220.77 | ₹181,674.61 | 0.9462 |

## Best Model

The **Random Forest Regressor** achieved the best performance.

It produced:

- MAE: **₹93,220.77**
- RMSE: **₹181,674.61**
- R² Score: **0.9462**

The model explains approximately 94.62% of the variation in selling prices in the test dataset.

## Feature Importance

The Random Forest feature-importance analysis identified `max_power` as the most influential feature, followed by:

1. Max power
2. Vehicle age
3. Kilometers driven
4. Mileage
5. Ferrari brand
6. Engine

This indicates that both vehicle specifications and categorical vehicle information contribute to predicting used-car prices.

## Actual vs Predicted Prices

The actual-versus-predicted plot shows that most predictions are reasonably close to the diagonal reference line, indicating strong agreement between actual and predicted selling prices.

Some larger deviations are visible for high-priced vehicles, where the model has more difficulty predicting the exact selling price.

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
DataScience-Task3-CarPricePrediction/
│
├── Car_Price_Prediction.ipynb
├── cardekho_dataset.csv
├── README.md
└── screenshots/
    ├── 01_Dataset_Overview.png
    ├── 02_Data_Cleaning.png
    ├── 03_Selling_Price_Distribution.png
    ├── 04_Price_by_Fuel_Type.png
    ├── 05_Price_vs_Vehicle_Age.png
    ├── 06_Correlation_Heatmap.png
    ├── 07_Model_Comparison.png
    ├── 08_Feature_Importance.png
    ├── 09_Actual_vs_Predicted.png
    └── 10_Final_Results.png