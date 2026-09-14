# Unemployment Analysis with Python

## Overview

This project performs exploratory data analysis (EDA) on unemployment data from India.

The analysis focuses on identifying regional and temporal patterns in unemployment
and examining changes during the COVID-19 period.

## Objective

The main objectives of this project are to:

- Understand the structure and quality of the unemployment dataset
- Analyze average unemployment rates across regions
- Study month-wise unemployment trends
- Compare unemployment trends across selected regions
- Examine relationships between unemployment, estimated employment, and labour participation
- Compare unemployment before and during the COVID-19 period
- Identify regions with the largest increases in unemployment

## Dataset

The project uses the **Unemployment in India** dataset.

The dataset contains information about:

- Region
- Date
- Frequency
- Estimated Unemployment Rate (%)
- Estimated Employed
- Estimated Labour Participation Rate (%)
- Area

The dataset was loaded directly into the Jupyter Notebook using pandas.

> Note: The dataset provides an `Estimated Employed` measure rather than a literal
> employment-rate column. Therefore, the available employment measure was used
> in the correlation analysis.

## Data Cleaning

The following preprocessing steps were performed:

1. Loaded the dataset using pandas.
2. Inspected the dataset shape and column names.
3. Removed leading/trailing spaces from column names.
4. Checked for missing values.
5. Removed rows containing missing values.
6. Converted the `Date` column to datetime format.
7. Verified the cleaned dataset using descriptive statistics and `df.info()`.

The dataset contained **768 rows initially** and **740 rows after removing missing values**.

## Exploratory Data Analysis

### 1. Region-wise Average Unemployment

The average unemployment rate was calculated for each region.

The regions with the highest average unemployment rates included:

- Tripura
- Haryana
- Jharkhand
- Bihar
- Himachal Pradesh

Tripura recorded the highest average unemployment rate in the dataset at approximately **28.35%**.

### 2. Month-wise Unemployment Trend

A time-series analysis was performed by calculating the average unemployment
rate for each month.

The unemployment rate was relatively stable during much of 2019 and early 2020,
followed by a sharp increase during April and May 2020.

The average unemployment rate reached approximately:

- **23.64% in April 2020**
- **24.88% in May 2020**

It then declined to approximately **11.90% in June 2020**.

### 3. Three-Region Time-Series Comparison

Unemployment trends were compared for:

- Tripura
- Haryana
- Jharkhand

The analysis shows that unemployment patterns differed considerably between
regions, with noticeable increases around the COVID-19 period.

### 4. Correlation Analysis

A correlation matrix was created using:

- Estimated Unemployment Rate (%)
- Estimated Employed
- Estimated Labour Participation Rate (%)

The correlation between unemployment rate and estimated employment was
approximately **-0.22**, indicating a weak negative linear relationship.

The correlations involving labour participation were close to zero.

### 5. Pre-COVID vs COVID-19 Period

The dataset was divided into two periods:

- **Pre-COVID:** Before March 2020
- **COVID-19 Period:** March 2020 onward

The average unemployment rate changed from:

| Period | Average Unemployment Rate |
|---|---:|
| Pre-COVID | 9.51% |
| COVID-19 Period | 17.77% |

This represents an increase of approximately **8.26 percentage points**.

### 6. Regional COVID-19 Impact

The change in average unemployment between the two periods was calculated for
each region.

The largest increases included:

| Region | Increase |
|---|---:|
| Puducherry | 37.36 percentage points |
| Tamil Nadu | 22.57 percentage points |
| Jharkhand | 22.07 percentage points |
| Bihar | 17.80 percentage points |
| Karnataka | 12.05 percentage points |

The results show that the increase in unemployment was not uniform across regions.

## Key Findings

- There was substantial variation in unemployment rates between regions.
- Tripura recorded the highest average unemployment rate among the regions analyzed.
- Unemployment increased sharply during April and May 2020.
- The average unemployment rate increased from **9.51% before COVID-19 to 17.77% during the COVID-19 period**.
- Puducherry experienced the largest increase among the regions analyzed.
- The relationship between unemployment and estimated employment was weakly negative.
- Labour participation showed very weak linear relationships with the other indicators.

## Visualizations

The project includes the following visualizations:

1. Top 10 regions by average unemployment rate
2. Month-wise unemployment trend
3. Three-region unemployment time-series
4. Correlation heatmap
5. Pre-COVID vs COVID-19 comparison
6. Regional COVID-19 unemployment impact

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

```text
DataScience-Task2-UnemploymentAnalysis/
│
├── Unemployment_Analysis.ipynb
├── Unemployment in India.csv
├── README.md
│
└── screenshots/
    ├── 01_Dataset_Overview.png
    ├── 02_Data_Quality_Statistics.png
    ├── 03_Top_10_Regions_Unemployment.png
    ├── 04_Monthly_Unemployment_Trend.png
    ├── 05_Three_Region_Time_Series.png
    ├── 06_Correlation_Heatmap.png
    ├── 07_Pre_COVID_vs_COVID.png
    └── 08_Regional_COVID_Impact.png