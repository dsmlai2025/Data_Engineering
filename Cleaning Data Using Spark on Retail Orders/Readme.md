## E-commerce Orders Data Cleaning

### Project Overview: 
This guided project walks you through cleaning an e-commerce orders dataset using PySpark, helping you understand how to extract, transform, and load data in a scalable way with Apache Spark. 
This project focuses on cleaning and transforming raw e-commerce order data (orders_data.parquet) to prepare it for use by the Machine Learning team.

### Objective

Prepare clean, structured data by applying specific cleaning rules to support demand forecasting and other ML models.

*Data Cleaning Steps*
Filter by time: Remove orders placed between 00:00 and 04:59.

*Create time_of_day: Based on order_date:*
05:00–11:59 → morning
12:00–17:59 → afternoon
18:00–23:59 → evening

*Remove product "TV":* Exclude rows where product is "TV".

*Standardize text:* Convert product and category columns to lowercase.
Extract state: Create purchase_state column from purchase_address.

*Files*

DataCleaningWithSpark_WalmartOrders.ipynb – Transformation and cleaning logic

orders_data.parquet – Raw input data
