# Databricks Retail Sales Pipeline

A beginner-friendly Data Engineering project built with **Databricks**, **PySpark**, **Delta Lake**, and **Spark SQL**. This project demonstrates how raw retail data can be transformed into analytics-ready datasets using the **Medallion Architecture (Bronze → Silver → Gold)**.

## Project Overview

This project walks through a simple end-to-end data pipeline in Databricks. Starting with three CSV files, the data is ingested using PySpark, stored as Delta tables, transformed into business-ready datasets, and queried using Spark SQL.

The project also explores Databricks features such as SQL visualizations, Databricks Jobs, and Unity Catalog through the accompanying article.

## Tech Stack

- Databricks
- Apache Spark
- PySpark
- Delta Lake
- Spark SQL

## Dataset

The project uses three sample retail datasets:

- **customers.csv** – Customer information
- **orders.csv** – Order transactions
- **products.csv** – Product catalog

## Pipeline

### Bronze Layer
- Read CSV files into PySpark DataFrames
- Store raw data as Delta tables

### Silver Layer
- Clean and prepare the data
- Remove duplicates
- Handle missing values

### Gold Layer
- Join datasets
- Calculate revenue
- Create analytics-ready tables

## SQL Analytics

The Gold table is queried using Spark SQL to generate business insights.

Example:

```sql
SELECT
    product_name,
    SUM(revenue) AS total_revenue
FROM gold_sales
GROUP BY product_name
ORDER BY total_revenue DESC;
```

## What's Included

- Databricks notebook
- Sample retail datasets
- PySpark transformations
- Delta Lake tables
- Spark SQL queries

## Databricks Features Demonstrated

Along with the notebook, this project explores several Databricks capabilities, including:

- Delta Lake
- Medallion Architecture
- Spark SQL
- SQL Dashboard
- Databricks Jobs
- Unity Catalog

> SQL visualizations, Databricks Jobs, and Unity Catalog are configured within the Databricks workspace and are demonstrated in the accompanying article rather than included as code in this repository.

## Getting Started

1. Upload the CSV files to a Databricks Volume.
2. Import the notebook into your Databricks workspace.
3. Run the notebook from top to bottom.
4. Execute the Spark SQL query on the Gold table.
5. Create a SQL visualization and configure a Databricks Job.

## Learnings

Through this project, I learned how to:

- Build a simple data pipeline using PySpark
- Work with Delta Lake tables
- Organize data using the Medallion Architecture
- Query data with Spark SQL
- Understand Databricks Jobs and Unity Catalog

## Article

A detailed walkthrough of this project link:
https://dev.to/shresthapandey/my-first-end-to-end-data-pipeline-in-databricks-4ajm
