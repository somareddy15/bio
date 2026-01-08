# Cloud Data Transformation: On-Prem to Azure Migration

## 📌 Project Overview
This project demonstrates the migration of legacy on-premises ETL workflows to a modern cloud architecture using **Azure Data Factory** and **Databricks**. The goal was to improve scalability, reduce operational costs, and implement robust data governance.



## 🚀 Technologies Used
* **Orchestration:** Azure Data Factory (ADF)
* **Compute:** Azure Databricks (PySpark)
* **Storage:** Azure Data Lake Storage (ADLS Gen2)
* **Governance:** Unity Catalog & Azure Key Vault
* **Data Modeling:** Medallion Architecture (Bronze, Silver, Gold)

## 🏗️ Architecture
1. **Ingestion:** Data is pulled from legacy SQL sources via Self-hosted Integration Runtimes in ADF.
2. **Raw Zone (Bronze):** Data is landed in ADLS Gen2 in its native format.
3. **Refinement (Silver):** Databricks notebooks perform data cleansing, schema enforcement, and deduplication.
4. **Analytics (Gold):** Business-level aggregates are stored in Delta tables for Power BI consumption.

## 📈 Key Outcomes
* **Performance:** 40% reduction in data processing time compared to on-prem systems.
* **Cost:** Eliminated physical server maintenance costs by moving to a pay-as-you-go cloud model.
* **Reliability:** Implemented automated retry logic and monitoring via Azure Monitor.

## 📂 Repository Structure
* `/notebooks`: PySpark scripts for data transformation.
* `/pipelines`: JSON exports of ADF pipelines.
* `/scripts`: SQL scripts for DDL and DML operations.
