# Shipment Data Pipeline: Oracle to Power BI via AWS
Built an end-to-end shipment data pipeline that extracts data from Oracle via ORDS REST API, 
stores raw data in Amazon S3, performs ETL using AWS Glue, loads clean data into Amazon RDS MySQL, 
and visualizes shipment insights in Microsoft Power BI

## Architecture

## Project Workflow
1. Shipment data is stored in Oracle Database.
2. Amazon EventBridge triggers AWS Lambda on a schedule.
3. Lambda fetches data from Oracle via ORDS REST API and saves it into S3 as raw data.
4. AWS Glue Crawler scans the raw data and updates the Glue Data Catalog.
5. AWS Glue ETL cleans and transforms the data.
6. Clean data is written back to Amazon S3.
7. Another Lambda job loads the clean data into Amazon RDS for MySQL.
8. Power BI connects to RDS and displays shipment insights on dashboards.

## My Role
- Designed the overall data pipeline architecture
- Built the data source and input UI using Oracle APEX
- Created and managed the shipment data source in Oracle Database
- Built scheduled data ingestion using EventBridge and Lambda
- Set up S3 raw/clean data layers
- Configured Glue Crawler and Glue ETL for transformation
- Loaded transformed data back into Amazon S3 and triggered a Lambda function to load updated data into MySQL
- Integrated Power BI for reporting and visualization

## Tech Stack
Oracle Database / ORDS REST API
Amazon EventBridge
AWS Lambda
Amazon S3
AWS Glue Crawler
AWS Glue ETL
Amazon RDS MySQL
Microsoft Power BI

## Responsibilities
- Designed the end-to-end ELT workflow
- Scheduled data extraction using EventBridge
- Developed Lambda functions for fetching and loading data
- Organized raw and clean data storage in S3
- Configured Glue Crawler and Glue ETL jobs for schema inference and cleansing
- Loaded transformed data into RDS MySQL for BI reporting
- Connected Power BI to RDS to build dashboard views

## Key Features 
- Automated scheduled ingestion
- Raw and clean data separation
- Schema discovery with Glue Crawler
- ETL validation and cleansing
- BI-ready relational data model
