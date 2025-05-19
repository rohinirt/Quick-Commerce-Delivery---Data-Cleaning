# Quick Commerce Delivery - Data Cleaning & Preprocessing

## Project Description

This project focuses on cleaning and preprocessing a real-world **Quick Commerce Delivery dataset** to prepare it for further analysis. The dataset contains **10,000 rows** and several features related to weather, traffic, delivery time, and geolocation data. The raw data had issues like missing values, incorrect formats, and inconsistent column naming, all of which were addressed to create a clean, analysis-ready dataset.

## Objective

The primary objective of this project is to **clean and preprocess the dataset** for effective exploratory data analysis (EDA) and modeling. No modeling is performed in this stage, but the dataset is optimized for downstream tasks.

## Dataset Overview

- **Domain**: Quick Commerce / Logistics
- **Size**: 10,000 rows
- **Key Features**:
  - `Order_Date`
  - `Traffic_Level`
  - `weather_description`
  - `temperature`, `humidity`, `precipitation`
  - `Restaurant_latitude`, `Restaurant_longitude`
  - `Delivery_location_latitude`, `Delivery_location_longitude`
  - `Delivery Time (Mins)`
  - `Distance (km)`

## Methodology

### 1) Understand the Data
Reviewed structure, column types, and basic statistics.
df.info()
df.describe()
df.columns

### 2) Rename Columns
Converted inconsistent or lengthy column names to cleaner formats using df.rename().

### 3) Correct Data Types
Converted object types to appropriate formats:
numerical features - numeric
Categorical features → category

### 4️) Handle Missing Values
Identified missing values using:
Filled nulls using appropriate techniques:

Mode for categorical features (e.g., Traffic_Level)

Mean/Median for numerical values (e.g., temperature, humidity)

Applied the Haversine formula to calculate missing distances using geolocation.
    ...
This ensures accurate geospatial distance between restaurants and delivery points.

## Tools & Libraries Used
Python

Pandas

NumPy

Jupyter Notebook

## Future Enhancements
Perform exploratory data analysis (EDA)

Train regression models to predict delivery time

Visualize delivery trends and delays using a dashboard
