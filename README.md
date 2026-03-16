# YouTube Data Engineering Pipeline using AWS

## 📌 Project Overview
This project demonstrates an end-to-end serverless Data Engineering pipeline on AWS to process and analyze YouTube trending video data.

The pipeline ingests raw CSV and JSON files, processes them using AWS services, converts them into optimized Parquet format, and enables SQL-based analytics using Amazon Athena.

The project simulates a modern cloud data lake architecture commonly used in production data platforms.

## 🏗️ Architecture
- Data Source: YouTube Dataset (CSV/JSON)
- Storage: Amazon S3 (Raw & Cleansed layers)
- Processing: AWS Lambda & AWS Glue
- Format Conversion: JSON/CSV → Parquet
- Metadata Catalog: AWS Glue Crawler
- Query Engine: Amazon Athena

## 🔄 Data Flow
1. Raw YouTube data uploaded to S3.
2. AWS Lambda processes JSON files and converts them into structured format.
3. AWS Glue job transforms and stores data in Parquet format.
4. AWS Glue Crawler catalogs Parquet files into Glue Data Catalog.
5. Amazon Athena queries the data using SQL.

🔄 Data Pipeline Workflow
  Step 1 — Data Ingestion
      
      Raw YouTube trending datasets (CSV + JSON) are uploaded to Amazon S3 Raw Layer.
      
  Step 2 — Lambda Processing
      
      AWS Lambda function processes JSON reference files and extracts nested fields.
      
      Main operations:
      
      Read JSON from S3
      
      Flatten nested structures
      
      Convert to tabular format
      
      Write structured data back to S3
      
  Step 3 — ETL Transformation
      
      AWS Glue ETL job performs:
      
      Data cleaning
      
      Schema normalization
      
      Format conversion
      
      CSV / JSON  →  Parquet
      
  Step 4 — Schema Discovery
      
      AWS Glue Crawler automatically detects the schema and updates the Glue Data Catalog.
      
      Tables created:
      
      raw_statistics
      raw_statistics_reference_data
      cleaned_parquet
      
  Step 5 — Analytics using Athena
      
      Amazon Athena queries the Parquet dataset directly from S3 using SQL.
      
      This enables serverless analytics without managing infrastructure.

## 💡 Key Features
- Optimized storage using Parquet format.
- Schema inference using Glue Crawler.
- Partitioned data by region.
- Serverless architecture using AWS.
- Cost-efficient analytics using Athena.

## 🛠️ Tech Stack
- Python
- AWS S3
- AWS Lambda
- AWS Glue
- AWS Athena
- Parquet
- Pandas
- AWS Wrangler

## 📊 Sample Use Cases
- Analyze trending videos by region.
- Identify most viewed videos.
- Compare likes and comments across categories.

## 🚀 Future Enhancements
- Automate pipeline using EventBridge.
- Add Airflow orchestration.
- Build dashboards using QuickSight.

## 🔗 Dataset
Data stored in S3 (not included in repo due to size).

---

⭐ If you like this project, feel free to star the repo!

