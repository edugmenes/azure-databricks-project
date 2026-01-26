# End-to-End Azure Data Engineering

This repository contains my **first Data Engineering project**, built using **Microsoft Azure Cloud** and **Azure Databricks**.

The project focuses on designing and implementing **ETL pipelines** using **PySpark** following the **Medallion Architecture (Bronze, Silver, Gold)**, a modern and widely adopted pattern for building scalable and reliable data platforms.



## 🚀 Project Overview

The main objective of this project is to demonstrate how raw data can be ingested, transformed, and curated into analytics-ready datasets using cloud-native tools and best practices.

The solution covers:
- Data ingestion from raw sources
- Data transformation and cleansing
- Data modeling for analytics consumption
- Distributed data processing with PySpark



## 🏗️ Architecture
![Architecture Diagram](/public/images/Captura%20de%20tela%202026-01-20%20123843.png)

### Azure Event Hubs
Purpose: Real-time data ingestion

Role in project:
- Captures streaming events (clicks, logs, IoT, transactions)
- Highly scalable and fault tolerant

✨ Without Event Hubs: You’d miss live data or overload systems

### Azure Data Factory (ADF)
Purpose: Orchestration & batch ingestion

Role in project:
- Schedules pipelines
- Moves data from source → data lake
- Triggers Databricks jobs

✨ Think of it as the control center

### Azure Databricks (Apache Spark)
Purpose: Data processing & transformation

Role in project:
- Processes huge volumes of data efficiently
- Implements Bronze → Silver → Gold logic
- Handles both batch and streaming data

✨ This is the engine of the architecture

### Azure Data Lake Storage Gen2 (ADLS)
Purpose: Central storage layer

Role in project:
- Stores all data (Bronze, Silver, Gold)
- Cheap, scalable, secure
- Optimized for analytics

✨ This is your single source of truth

### Delta Lake
Purpose: Reliability & governance on top of ADLS

Role in project:
- ACID transactions
- Schema enforcement
- Time travel (data versioning)
- Efficient reads/writes

✨ Delta Lake turns “files” into real analytical tables



## 🧮 Data Model
The project is structured using a **Medallion Architecture** 

    <storage-account>/<container>/
    │
    └── projet1/
        ├── resources/                  # Source and target data
        │   ├── source/                 # CSV files received from the source
        │   └── target/                 # Exports files for customers
        │
        ├── 01-bronze/                  # Raw data
        │   ├── customers/
        │   │   └── customers.parquet
        │   ├── sales/
        │   │   └── sales.parquet
        │   ...
        │    
        ├── 02-silver/                  # Clean data
        │   ├── customers/
        │   │   └── customers.parquet
        │   ├── sales/
        │   │   └── sales.parquet
        │   ...
        │
        ├── 03-gold/                    # Aggregated data
        │   ├── sales_per_category/
        │   ├── sales_per_city/
        │   ...
        │
        ├── metadata/                   # Metadata and logs
        │   ├── bronze/
        │   ├── silver/
        │   ├── gold/
        │   ├── ddl/                    # CREATE TABLE scripts
        │   ├── logs/                   # ETL execution logs
        │   └── checkpoints/            # Autoloader checkpoints / streaming
        │
        └── tmp/                        # Temporary staging

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
