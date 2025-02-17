# AWS-YoutubeAnalytics-DataPipeline

## Project Overview

This project analyzes YouTube video statistics to uncover insights into video popularity trends across different regions using scalable data engineering practices on AWS.

## Goals

- **Data Ingestion**: Implement a robust system to ingest data from YouTube APIs and other sources.
- **ETL System**: Transform raw data into a structured format suitable for analysis.
- **Data Lake**: Utilize AWS S3 for centralized storage to handle data from various sources efficiently.
- **Scalability**: Ensure the system can scale dynamically with increasing data volumes.
- **Cloud Utilization**: Leverage AWS services to handle large-scale data processing.
- **Data Visualization**: Develop a QuickSight dashboard to visualize key metrics and trends.

## Data Flow Description

1. **Data Collection**: Data is ingested from the YouTube API and stored in raw format in Amazon S3.
2. **Data Processing**:
   - AWS Glue is used to catalog raw data and manage ETL jobs.
   - AWS Lambda functions are triggered to process and transform data as needed.
3. **Data Storage**: Processed data is stored back in S3, ensuring it is ready for analysis.
4. **Analysis and Reporting**:
   - Use AWS Athena for ad-hoc query performance.
   - Amazon QuickSight integrates with S3 and Athena to provide interactive dashboards.

## Architecture

<img src="architecture.jpeg">

## Services Used

- **Amazon S3**: Object storage service with scalability and data availability.
- **AWS IAM**: Manages access securely across AWS services.
- **AWS Lambda**: Runs code in response to events without provisioning servers.
- **AWS Glue**: Prepares and combines data for analysis without server management.
- **AWS Athena**: SQL-based queries executed directly against data in S3.
- **Amazon QuickSight**: BI service for data visualization.

## Dataset
This Kaggle [Dataset](https://www.kaggle.com/datasets/datasnaek/youtube-new) contains statistics (CSV files) on daily popular YouTube videos over the course of many months. There are up to 200 trending videos published every day for many locations. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region.

## ETL Pipelines executed

<img src="ETL_1.jpg">
<img src="ETL_2.jpg">

## Sample Dashboards 

<img src="Visual_1.png">
<img src="Visual_2.png">
