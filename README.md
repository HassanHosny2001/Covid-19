# COVID-19 Workflow

##Overview:
- This repository presents a streamlined COVID-19 data analysis workflow using data from Kaggle, and it utilizes Cloudera, HDFS, Hive, Oozie, and Power BI.

## Data Ingestion:
- Import COVID-19 datasets from Kaggle, a reliable data source.
- Clean and prepare the data for analysis.

## Data Loading:
- Load the dataset to HDFS.

## Hive Database Setup:
- Create a database in Hive.
- Create the following schemas in Hive:
* 1st Hive staging table for pointing to the dataset location to select data from.
* 2nd Hive ORC table partitioned by Country to improve query performance.
* 3rd Final Hive table to generate the report and output file for visualization.

## Oozie Workflow Setup:
- Automate data processing tasks with an Oozie workflow in Cloudera HUE.
- Schedule regular updates for up-to-date analysis.

## Data Visualization:
- Gain valuable insights from COVID-19 data using Power BI.
- Create interactive visualizations for better understanding.
