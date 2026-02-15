# 🛒 Olist E-Commerce Data Warehouse & Analytics Project

## 📌 Project Overview

This project demonstrates the design and implementation of an end-to-end data analytics solution using a layered data architecture approach. The goal is to transform raw e-commerce data into a clean, business-ready analytical model that supports reporting and insights.

The project covers the full data lifecycle:

* Raw data ingestion
* Data cleaning and transformation
* Data quality validation
* Dimensional modeling (Star Schema)
* Analytical querying

This project simulates a real-world business intelligence environment commonly used in modern organizations.

---

## 🎯 Objectives

* Build a structured data warehouse from raw CSV files
* Apply data cleaning and transformation logic
* Implement layered architecture (Bronze → Silver → Gold)
* Design a Star Schema for analytics
* Perform data quality validation checks
* Prepare data for BI tools such as Power BI

---

## 🏗️ Architecture

The project follows a multi-layered architecture:

```
Raw Data → Bronze Layer → Silver Layer → Gold Layer → Analytics
```

### Layers Description

**Bronze Layer — Raw Data**

* Stores ingested data without transformations
* Serves as historical source of truth

**Silver Layer — Cleaned Data**

* Data type conversions
* Null handling
* Business rule implementation
* Derived columns creation
* Data validation fixes

**Gold Layer — Analytical Model**

* Star schema design
* Fact and dimension views
* Business-ready dataset for reporting

---

## ⭐ Data Model (Gold Layer)

The analytical model consists of:

### Fact Table

* `fact_order_items`

### Dimension Tables

* `dim_customers`
* `dim_products`
* `dim_sellers`
* `dim_date`

The model enables analysis across customers, products, sellers, and time dimensions.

---

## ⚙️ ETL Process

Two stored procedures control the pipeline:

### 1️⃣ Bronze Load

`proc_load_bronze`

* Bulk insert from CSV files
* Minimal processing
* Raw ingestion

### 2️⃣ Silver Load

`proc_load_silver`

* Data cleaning
* Type conversions
* Business logic
* Derived metrics
* Data quality improvements

Gold layer is created using SQL views on top of the Silver layer.

---

## 📊 Key Metrics Created

* Total item value
* Payment value aggregation
* Delivery duration
* Approval duration
* Estimated vs actual delivery difference
* Late delivery flag
* Customer and seller geolocation enrichment
* Review score aggregation

---

## ✅ Data Quality Checks

Quality validation scripts were implemented for all layers:

### Bronze Layer

* Row count validation
* Null checks
* Duplicate detection
* Data completeness verification

### Silver Layer

* Data type validation
* Business rule enforcement
* Invalid value detection
* Transformation accuracy checks

### Gold Layer

* Referential integrity validation
* Measure consistency
* Date relationship validation
* Aggregation accuracy checks

---

## 📁 Project Structure

```
project-root/
│
├── datasets/
│   ├── raw_csv_files
│
├── scripts/
│   ├── bronze/
│   ├── silver/
│   ├── gold/
│
├── tests/
│   ├── bronze_quality_checks.sql
│   ├── silver_quality_checks.sql
│   ├── gold_quality_checks.sql
│
├── docs/
│   ├── medallion_architecture.png
│   ├── data_pipeline.png
│   ├── star_schema.png
│
└── README.md
```

---

## 🛠️ Technologies Used

* SQL Server
* T-SQL
* Data Warehousing Concepts
* Dimensional Modeling
* Draw.io (Diagrams)
* GitHub (Version Control)

---

## 📈 Potential Business Use Cases

* Sales performance analysis
* Delivery performance monitoring
* Customer behavior analysis
* Seller performance evaluation
* Product category insights
* Revenue trend analysis

---

## 🚀 Future Improvements

* Power BI dashboard integration
* Incremental data loading
* Data orchestration using pipelines
* Performance optimization with indexed tables
* Advanced KPI calculations

---

## 👨‍💻 Author

Meenakshi Singh
Data Analyst | SQL | Data Modeling | Business Intelligence

---

## 📜 Data Source

Olist Brazilian E-Commerce Public Dataset

---

## ⭐ Project Purpose

This project was created for portfolio demonstration and skill development in data analytics and data warehousing concepts.

