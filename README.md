# Wearables Health Data Engineering Project
<p align="center">
  <img src="icooons.webp" width="800">
</p>

An end-to-end **Data Engineering pipeline** for processing and analyzing wearable health data generated from smart devices such as smartwatches and fitness trackers.

This project demonstrates how raw health data can be ingested, transformed, modeled, and visualized using modern data engineering tools and best practices.

---

## 📌 Project Overview

Wearable devices generate large volumes of daily health data.  
This project simulates a real-world scenario where such data is processed through a scalable batch data pipeline and prepared for analytics and reporting.

The dataset represents:
- **6 months** of daily records  
- **300 users**  
- Synthetic but **physiologically realistic** wearable health data  

---

## 📊 Dataset Details

The dataset includes daily health metrics such as:
- Steps count  
- Calories burned  
- Heart rate  
- Sleep duration  
- Activity level  

Data is generated to closely resemble data collected from modern wearable devices.

---

## 🛠 Tech Stack

| Layer | Technology |
|-----|-----------|
| Data Source | CSV Files |
| Metadata Management | AWS Glue Crawler & Data Catalog |
| Data Processing | PySpark |
| Data Modeling | Star Schema |
| Visualization | Power BI |

---

## 🏗 Architecture

```
Raw Wearable Data (CSV)
        ↓
AWS Glue Crawler
        ↓
AWS Data Catalog
        ↓
PySpark (Data Cleaning & Transformations)
        ↓
Data Warehouse (Star Schema)
        ↓
Power BI Dashboards
```

---

## 🔄 Data Pipeline Workflow

### 1. Data Ingestion
Raw wearable data is stored as CSV files containing daily health records for each user.

---

### 2. Schema Detection (AWS Glue Crawler)
AWS Glue Crawler is used to automatically:
- Detect column names
- Infer data types
- Understand table structure
- Store metadata in AWS Data Catalog  

This enables schema discovery without manual intervention.

---

### 3. Data Transformation (PySpark)
PySpark handles large-scale data transformations, including:
- Null value detection and counting
- Data type validation
- Filtering invalid records
- Preparing clean datasets for analytics

---

### 4. Data Modeling (Star Schema)
The transformed data is modeled into a **Star Schema** to support analytical queries.

#### Dimension Tables
- **Dim_Date**: date-related attributes  
- **Dim_User**: user-level attributes  

#### Fact Table
- **Fact_Daily_Health**: daily health metrics linked to dimensions via foreign keys  

This structure improves query performance and BI usability.

---

### 5. Data Warehouse Layer
The star schema tables form the data warehouse layer, acting as the single source of truth for reporting and analytics.

---

### 6. Data Visualization (Power BI)
Power BI dashboards are built on top of the warehouse to analyze:
- Daily and monthly activity trends
- Health metric distributions
- User behavior over time  

Dashboards are interactive and designed for analytical insights.

---

## 📈 Key Outcomes

- Built a complete batch ETL pipeline
- Applied scalable data transformations using PySpark
- Designed a professional dimensional data model
- Enabled business-friendly analytics using Power BI

---

## 🚀 Future Enhancements

- Add real-time streaming with Kafka
- Use Airflow for pipeline orchestration
- Load data into cloud warehouses (Redshift / Snowflake)
- Implement data quality checks
- Extend dashboards with advanced analytics

---

👨‍💻 Author
Mahmoud [saad]
📧 Email: [mahmoud010196@gmail.com]
💼 LinkedIn: https://www.linkedin.com/in/mahmoud-saad-8540b63a0/
🐙 GitHub: https://github.com/mah8saad
