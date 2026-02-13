# YouTube Data Engineering Pipeline using AWS

## 📌 Project Overview
This project builds an end-to-end data engineering pipeline using AWS services to process YouTube trending video data.

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

