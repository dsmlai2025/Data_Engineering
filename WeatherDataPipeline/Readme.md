# Weather Data Pipeline with Python and PostgreSQL

## Project Overview
<img width="400" height="300" alt="image" src="https://github.com/dsmlai2025/Data_Engineering/blob/main/WeatherDataPipeline/RideShareWeather.jpg" />

Ridefy would like to develop an ETL pipeline to integrate weather information into its route optimization, fleet management, demand forecasting, and dynamic pricing systems. 
This project aims to enhance decision-making by incorporating real-time and historical weather data, enabling Ridefy to improve operational efficiency 
and adapt dynamically to weather-driven variables.

## Project Description

The ETL pipeline extracts weather data from external APIs, performs necessary transformations including data cleansing, formatting, and enrichment, 
and loads the processed data into a PostgreSQL database. The pipeline supports near real-time updates and bulk historical data ingestion, ensuring comprehensive 
and high-quality weather information is available for downstream analytics and machine learning models. 
By integrating weather data, Ridefy aims to optimize vehicle routing under varying conditions, improve fleet utilization, 
forecast demand with higher accuracy, and enable dynamic pricing strategies responsive to weather impacts.

## Tools Used
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![APIs](https://img.shields.io/badge/APIs-005571?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-333333?style=for-the-badge&logo=pandas)

## Steps
1. Data Extraction
   * Obtain API keys from OpenWeatherAPI.
   * Configure the desired city and the forecasted time period for data extraction.
   * Use Python (with requests) to fetch weather data.

2. Data Transformation
  * Inspect the datasets for missing or inconsistent values.
  * Remove or impute any missing data as appropriate.
  * Convert weather temperature from Kelvin to Celsius if necessary.
  * Optional - Derive additional features, such as "Feels like temperature" and AQI categories (e.g., Good, Moderate, Unhealthy).

3. Data Loading
   * Define the PostgreSQL schema using the provided schema.sql file (tables for weather).
   * Use SQLAlchemy (or another database connector) to connect to the PostgreSQL database.
   * Insert the transformed weather into the appropriate tables.
   * Validate successful data transfer by querying the database after loading.

## Project Summary
This project is an end-to-end ETL pipeline designed to extract weather and air quality data from public APIs, transform it into a clean and analyzable structure, 
and load it into a PostgreSQL database for further use. 
It showcases essential data engineering skills, including API integration, data transformation with Python and pandas, and automated loading into a relational database. 
The pipeline features robust error handling, logging, and can be orchestrated using workflow tools for automation. 
The repository provides a clear template for integrating diverse weather and air quality datasets, building a foundation for analytics and visualization applications.
