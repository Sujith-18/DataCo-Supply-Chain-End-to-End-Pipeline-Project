# DataCo Supply Chain Data Engineering Pipeline

## 📌 Project Overview

This project implements an end-to-end data engineering pipeline using Microsoft Azure services to process the DataCo Supply Chain dataset, which contains customer orders, sales, and shipment information.

The pipeline follows the **Medallion Architecture** to transform raw data into clean, structured, analytics-ready datasets for reporting and visualization.

## 🏗️ Architecture


DataCo Supply Chain Dataset
           |
           v
    Azure Data Factory
           |
           v
       Bronze Layer
   (Raw Source Data)
           |
           v
    Azure Databricks
         PySpark
           |
  Data Cleaning & Validation
           |
           v
       Silver Layer
  (Transformed Data)
           |
           v
 Azure Synapse Analytics
      Serverless SQL
           |
      SQL Views
           |
   Star Schema Modeling
           |
           v
        Gold Layer
  Fact & Dimension Tables
           |
           v
 Reporting & Visualization


## 🛠️ Technologies Used

- **Azure Data Factory:** Data ingestion and pipeline orchestration.
- **Azure Data Lake Storage Gen2:** Storage for Bronze, Silver, and Gold layers.
- **Azure Databricks:** Data processing and transformation.
- **PySpark:** Data cleaning, duplicate handling, and validation.
- **Azure Synapse Analytics:** SQL-based data exploration and modeling.
- **SQL:** Views, fact tables, dimension tables, and star schema modeling.
- **Microsoft Entra ID:** Application authentication and storage access.

## 🔄 Implementation

### 1. Bronze Layer — Data Ingestion
- Loaded the DataCo dataset from a local device into Azure Data Lake Storage using Azure Data Factory.
- Stored the raw source data in the Bronze layer.

### 2. Silver Layer — Data Transformation
- Read Bronze-layer data in Azure Databricks.
- Handled null values and duplicates.
- Standardized data formatting and performed data validation.
- Stored the cleaned and transformed data in the Silver layer.

### 3. Gold Layer — Data Modeling
- Queried Silver-layer data using Azure Synapse Analytics.
- Created SQL views to explore the datasets.
- Designed fact and dimension tables based on the relationships between datasets.
- Loaded the modeled data into the Gold layer for reporting and visualization.

## ⭐ Key Features

- End-to-end cloud data pipeline implementation.
- Medallion Architecture with Bronze, Silver, and Gold layers.
- PySpark-based data cleaning and validation.
- SQL-based data modeling using fact and dimension tables.
- Analytics-ready supply chain data for downstream reporting.

## 🎯 Outcome

Built an end-to-end supply chain data engineering pipeline that transforms raw order, sales, and shipment data into structured datasets suitable for analytical queries and business intelligence reporting.

