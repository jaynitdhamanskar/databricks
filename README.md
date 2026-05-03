# 🏗️ End-to-End Data Lakehouse Project (Databricks)

## 📌 Overview

This project showcases a **production-style data lakehouse architecture** built using Databricks, implementing the **Medallion Architecture (Bronze → Silver → Gold)** to transform raw CRM and ERP data into **analytics-ready datasets**.

The pipeline simulates a real-world business scenario by integrating multiple data sources, applying transformations, and delivering **fact and dimension tables** for downstream analytics and BI reporting.

---

## 🚀 Key Highlights

* End-to-end **data engineering pipeline**
* Multi-source integration (**CRM + ERP systems**)
* **Medallion Architecture (Bronze, Silver, Gold)**
* Dimensional modeling (**Star Schema**)
* Fact & Dimension table creation
* Notebook-based orchestration
* Scalable and modular design

---

## 🧱 Architecture


<p align="center">
  <img src="https://github.com/jaynitdhamanskar/databricks/blob/main/assest/sketching.png" alt="Architecture Diagram" width="800"/>
</p>

---

## 📂 Project Structure

```
📁 project-root
│
├── init_lakehouse.ipynb                # Lakehouse setup & initialization
│
├── silver/
│   ├── CRM
│   │   ├── silver_crm_cust_info.ipynb
│   │   ├── silver_crm_prd_info.ipynb
│   │   └── silver_crm_sales_details.ipynb
│   │
│   ├── ERP
│   │   ├── silver_erp_cust_az12.ipynb
│   │   ├── silver_erp_loc_a101.ipynb
│   │   └── silver_erp_px_cat_g1v2.ipynb
│   │
│   └── silver_orchestration_.ipynb     # Silver layer pipeline orchestration
│
├── gold/
│   ├── Dimensions
│   │   ├── gold_dim_customers.ipynb
│   │   └── gold_dim_products.ipynb
│   │
│   ├── Facts
│   │   └── gold_fact_sales.ipynb
│   │
│   └── gold_orchestration_.ipynb       # Gold layer orchestration
│
└── README.md
```

---

## ⚙️ Pipeline Workflow

### 🔹 1. Initialization (Lakehouse Setup)

* Create schemas and databases
* Configure storage and environment
* Prepare workspace for pipeline execution

📄 `init_lakehouse.ipynb`

---

### 🔹 2. Silver Layer (Data Processing)

Transforms raw data into clean, structured datasets.

**Key Operations:**

* Data cleansing (null handling, deduplication)
* Standardization of formats
* Data enrichment & joins across systems
* Schema alignment

**Data Sources:**

* CRM → Customer, Product, Sales
* ERP → Customer (AZ12), Location (A101), Product Categories

📄 Orchestration: `silver_orchestration_.ipynb`

---

### 🔹 3. Gold Layer (Business Modeling)

Builds analytics-ready datasets using dimensional modeling.

**Dimensions:**

* Customers
* Products

**Fact Tables:**

* Sales (transactions, revenue metrics)

**Key Features:**

* Star schema design
* Aggregations for reporting
* Business-friendly structure

📄 Orchestration: `gold_orchestration_.ipynb`

---

## 🧰 Tech Stack

| Category                | Technology                         |
|------------------------|----------------------------------|
| Platform               | Databricks                       |
| Processing Engine      | Apache Spark (PySpark & SQL)     |
| Storage Layer          | Delta Lake                       |
| Transformation         | SQL Transformations              |
| Orchestration          | Notebook-based orchestration     |

---


## 👨‍💻 Author

**Jaynit Dhamanskar**
