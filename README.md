## Project Overview

This project analyzes global earthquake data from the last 10 years using an end-to-end data pipeline.
The raw data is processed using Apache Spark to clean, transform, and aggregate large-scale seismic records.
The processed datasets are then visualized in interactive dashboards built with Power BI to explore global patterns, temporal trends, and earthquake characteristics.

## Dataset

The dataset contains approximately 80,000 earthquake records collected over the last 10 years.
Each record includes information such as:
- Timestamp
- Geographic location (latitude and longitude)
- Magnitude and magnitude type
- Depth
- Region description

The data was obtained from publicly available seismic sources (USGS).

## Project Architecture

Raw CSV Data
      ↓
Spark ETL (cleaning, transformation, aggregation)
      ↓
Processed datasets (BI-ready)
      ↓
Power BI Interactive Dashboards

## ETL Process

The ETL pipeline was implemented using PySpark and includes the following steps:
- Data ingestion from raw CSV files
- Data cleaning (null values, data types, filtering invalid records)
- Feature engineering (year extraction, depth and magnitude categorization)
- Aggregation of earthquake events by year and magnitude type
- Export of processed datasets for BI consumption

## Data Modeling

The final data model follows a simple star-schema approach:
- A central fact table containing cleaned earthquake events
- Supporting aggregated tables for yearly trends and magnitude analysis

This structure ensures efficient filtering and visualization in Power BI.

## Power BI Dashboard

The Power BI dashboard provides:
- A global map showing earthquake distribution by location and magnitude
- Time-series analysis of earthquake frequency per year
- Magnitude distribution analysis
- Interactive filters by year and magnitude type

## Technologies Used

- Python
- Apache Spark (PySpark)
- Power BI
- Pandas
- Git & GitHub