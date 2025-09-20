## Building a Retail Data Pipeline

### Project Overview
In this project, you'll build a complete ETL pipeline with Walmart's retail data. 
You'll retrieve data from various sources, including SQL databases and Parquet files, apply transformation techniques to prepare and clean the data, and finally load it into an easily accessible format.
This project is excellent for building foundational yet advanced data engineering knowledge because it covers essential skills like data extraction 
from multiple formats, data transformation for meaningful analysis, and data loading for efficient storage and access. 
It helps reinforce concepts like handling diverse data sources, optimizing data flows, and maintaining scalable pipelines.

### Background
Walmart is the biggest retail store in the United States. Just like others, they have been expanding their e-commerce part of the business. 
By the end of 2022, e-commerce represented a roaring $80 billion in sales, which is 13% of total sales of Walmart. One of the main factors that affects their sales is public holidays, like the Super Bowl, Labour Day, Thanksgiving, and Christmas.
In this project, you have been tasked with creating a data pipeline for the analysis of supply and demand around the holidays, along with conducting a preliminary analysis of the data. 
You will be working with two data sources: grocery sales and complementary data. You have been provided with the grocery_sales table in PostgreSQL database with the following features:

*grocery_sales*


| index |  unique ID of the row |
|----| -----|
| Store_ID |  the store number |
| Date | the week of sales |
| Weekly_Sales | sales for the given store |

Also, you have the extra_data.parquet file that contains complementary data:

*extra_data.parquet*

|col | Descr |
|---|---|
| IsHoliday | Whether the week contains a public holiday - 1 if yes, 0 if no. |
| Temperature | Temperature on the day of sale|
| Fuel_Price | Cost of fuel in the region|
| CPI" | Prevailing consumer price index|
| Unemployment" | The prevailing unemployment rate|
| MarkDown1", "MarkDown2", "MarkDown3", "MarkDown4" | number of promotional markdowns|
| Dept | Department Number in each store|
| Size | size of the store | 
| Type |  type of the store (depends on Size column) | 

**Task**

You will need to merge those files and perform some data manipulations. 
The transformed DataFrame can then be stored as the clean_data variable containing the following columns:

| Store_ID |
|----|
| Month |
| Dept |
| IsHoliday |
| Weekly_Sales |
| CPI |
| ""Unemployment"" |

After merging and cleaning the data, you will have to analyze monthly sales of Walmart and store the results of your analysis as the agg_data variable that should look like:
Finally, you should save the clean_data and agg_data as the csv files.
