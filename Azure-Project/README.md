
# Azure Health Insurance Claims Pipeline

This project demonstrates an **end-to-end Azure Data Engineering solution** for processing and analyzing Health Insurance Claims data.  
It follows the **Medallion Architecture (Bronze → Silver → Gold)** to ensure data quality, governance, and business insights.

---

## 📂 Project Structure

```
Azure-Project/
│── 1. Set up/               # Environment setup scripts and configurations
│── 2. API extracts/         # Data ingestion from APIs (claims, patients, providers)
│── 3. Silver/               # Cleansed and transformed data
│── 4. Gold/                 # Curated data for analytics
│── EMR_DDL/                 # Table definitions for EMR datasets
│── datasets/                # Sample input datasets
│── Gold Queries/            # Analytical queries for reporting
│── Lookup_file_table_mapping.json  # Lookup and mapping logic
│── audit_table_ddl/         # Audit table structures for governance
│── Project Notes/           # Notes and documentation
```

---

## 🚀 Architecture

![Azure Health Insurance Claims Pipeline](azure_claims_pipeline_architecture.png)

This pipeline is built using the following Azure components:

- **Azure Data Factory (ADF)** → Orchestrates ingestion of raw claim, patient, and provider data.  
- **Azure Data Lake (Bronze)** → Stores raw ingested data in its original format.  
- **Azure Databricks (Silver Layer)** → Cleanses, transforms, and standardizes the data.  
- **Azure Synapse Analytics / SQL DB (Gold Layer)** → Stores curated datasets optimized for analytics.  
- **Power BI** → Provides dashboards and insights for claim analysis, fraud detection, and cost optimization.  

---

## ⚙️ Key Features

- Follows **Medallion Architecture** (Bronze → Silver → Gold).  
- Ingests **API extracts and flat files** into Azure Data Lake.  
- Cleansing, deduplication, and standardization with **PySpark in Databricks**.  
- Audit and monitoring with **audit tables & logging**.  
- Final analytical layer optimized for **Power BI dashboards**.  

---

## 📊 Use Cases

- **Claim Cost Analysis** – Track medical costs and reimbursements.  
- **Fraud Detection** – Identify duplicate or suspicious claims.  
- **Provider Performance** – Analyze provider efficiency and quality metrics.  
- **Member Insights** – Understand claim patterns and member risk profiles.  

---

## 🛠️ Tech Stack

- **Azure Data Factory** – Data ingestion & orchestration  
- **Azure Data Lake Storage (ADLS Gen2)** – Raw, cleansed, curated data layers  
- **Azure Databricks (PySpark, Delta Lake)** – Transformations  
- **Azure Synapse Analytics / SQL Database** – Analytical store  
- **Power BI** – Dashboards & visualization  

---

## 📌 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/areef322/Repos.git
   cd Azure-Project
   ```

2. Set up Azure resources (ADF, ADLS, Databricks, Synapse).  

3. Load raw data into **datasets/** or connect API extracts in **2. API extracts/**.  

4. Use **Databricks notebooks** (inside `3. Silver/`) for data cleansing and transformation.  

5. Load curated data into **Synapse / SQL** (inside `4. Gold/`).  

6. Connect **Power BI** to the Gold layer for dashboards.  

---

## ✅ Future Enhancements

- Add **CI/CD with GitHub Actions** for pipeline deployment.  
- Implement **Data Quality checks with Great Expectations**.  
- Enable **Real-time ingestion with Event Hub / Kafka**.  
- Add **Machine Learning models** for fraud detection.  

---

## 👨‍💻 Author

- **Areef**  
  📧 Contact: [areefm556@gmail.com]  
  🌐 GitHub: [areef322](https://github.com/areef322)

---
