# 🏠 Home Sales Analysis with SparkSQL

## Overview

This project analyzes a home sales dataset using **Apache Spark** and **SparkSQL**.  
You will perform various data transformation and querying tasks including:

- Loading data from an AWS S3 bucket
- Creating temporary SQL views
- Using SparkSQL to compute grouped metrics
- Measuring runtime performance
- Caching and un-caching tables
- Saving and reading Parquet files with partitioning

<br/>

## Technologies Used

- Python 3.x  
- Apache Spark 3.5.x  
- Google Colab  
- SparkSQL  
- Parquet Format  

---

## Dataset

The dataset is provided in CSV format and contains information about home sales, such as:

- `date`: Sale date  
- `date_built`: Construction year  
- `price`: Sale price  
- `bedrooms`, `bathrooms`, `floors`  
- `sqft_living`: Square footage  
- `view`: View rating (0–4)

---

## Tasks Completed

### ✅ Data Loading & View Creation

- Loaded CSV from AWS S3 using `SparkFiles`
- Created a temporary SQL view called `home_sales`

### ✅ SparkSQL Queries

- Average price of 4-bedroom homes per year (sold date)
- Average price of 3 bed / 3 bath homes by year built
- Average price for homes with specific filters (≥2000 sqft, 2 floors)
- Average price by `view` rating (only ≥ $350,000), with runtime measurement

### ✅ Performance Optimization

- Cached `home_sales` temporary table
- Compared runtime between cached vs. uncached queries
- Saved dataset as **Parquet**, partitioned by `date_built`
- Loaded Parquet data and recreated temporary view
- Re-ran performance query on Parquet data

### ✅ Resource Cleanup

- Uncached the `home_sales` view and verified removal

---

## How to Run

1. Open the notebook `Home_Sales.ipynb` in Google Colab
2. Install Spark and Java using the first code cell
3. Run each section step by step, following markdown headers
4. Observe runtimes and query results in output cells

---

## Author

Batuhan Aysan  
University of Toronto Data Analytics Bootcamp  
June 2025 – Module 22: SparkSQL

---

## License

This project is for educational purposes and not intended for production use.
