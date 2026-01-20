# Azure Databricks - Data Engineering Project

This repository contains my **first end-to-end Data Engineering project**, built using **Microsoft Azure Cloud** and **Azure Databricks** with **PySpark**.

The project focuses on designing and implementing **ETL pipelines** following the **Medallion Architecture (Bronze, Silver, Gold)**, a modern and widely adopted pattern for building scalable and reliable data platforms.



## 🚀 Project Overview

The main objective of this project is to demonstrate how raw data can be ingested, transformed, and curated into analytics-ready datasets using cloud-native tools and best practices.

The solution covers:
- Data ingestion from raw sources
- Data transformation and cleansing
- Data modeling for analytics consumption
- Distributed data processing with PySpark



## 🏗️ Architecture

The project is structured using the **Medallion Architecture**:

### 🟤 Bronze Layer
- Raw data ingestion
- Minimal transformation
- Preserves source data as-is

### ⚪ Silver Layer
- Data cleansing and normalization
- Data enrichment
- Application of business rules

### 🟡 Gold Layer
- Curated, analytics-ready datasets
- Optimized for reporting and BI use cases



## 🛠️ Technologies Used

- Microsoft Azure
- Azure Databricks
- Apache Spark (PySpark)
- Delta Lake
- Medallion Architecture



## 🎯 Key Learnings

Through this project, I gained hands-on experience with:
- Cloud-based data platforms
- Distributed data processing using Spark
- Building scalable ETL pipelines
- Applying modern Data Engineering design patterns
- Managing data across multiple data layers



## 📌 Notes

This is a **learning project**, created to apply theoretical concepts in a practical environment using industry-standard tools.

Future improvements may include:
- Pipeline orchestration
- Data quality checks
- Performance optimization
- Monitoring and logging
