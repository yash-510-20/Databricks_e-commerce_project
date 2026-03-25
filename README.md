# databricks_project_managed_tab
#In this project i have used Managed Tables to make this project where i have used Order data set consist 5 different files and process it and using medallion architecture presented into gold layer
#  Databricks Sales ETL Pipeline (Bronze → Silver → Gold)

##  Project Overview

This project implements an end-to-end **data engineering pipeline** using PySpark on Databricks.
It follows the **Medallion Architecture** (Bronze, Silver, Gold) to transform raw data into business-ready insights.

---

##  Architecture

```
Raw Data → Bronze Layer → Silver Layer → Gold Layer → Analytics
```

###  Bronze Layer

* Ingest raw data from source
* Minimal transformation
* Store as-is for traceability

###  Silver Layer

* Data cleaning & validation
* Handle nulls, duplicates
* SCD-2 logic
* Add derived columns (e.g., `order_date`, `revenue`)

###  Gold Layer

* Business-level aggregations
* Optimized for reporting & dashboards

---

##  Key Features

*  End-to-end ETL pipeline using PySpark
*  Modular notebook structure
*  Job orchestration using Databricks Workflows
*  Business-ready aggregations
*  Scalable and production-friendly design

---

##  Dataset Schema (fact_sales)

### Identifiers

* order_id
* order_item_id
* customer_id
* product_id

### Time Attributes

* order_purchase_timestamp
* order_date

### Measures

* price
* freight_value
* revenue

### Dimensions

* customer_state
* product_category_name

---

##  Gold Layer Outputs

*  Sales by State
*  Top Products by Revenue
*  Daily Sales Trends
*  Monthly Sales Trends

---

##  Tech Stack

* PySpark
* Databricks
* Delta Lake
* SQL

---

##  How to Run

1. Upload project to Databricks workspace
2. Import notebooks
3. Create job using `config/job_config.json`
4. Run pipeline:

   * Bronze → Silver → Gold

---

##  Workflow

```
Bronze → Silver → Gold
   ↓        ↓        ↓
 Raw   Cleaned   Aggregated
 Data    Data       Data
```

---

##  Future Improvements

* Add streaming pipeline
* Implement CI/CD
* Integrate with dashboard tools (Power BI / Tableau)

---

##  Author

Yash More
(Data Engineer)

---

## ⭐ If you like this project

Give it a star on GitHub!
