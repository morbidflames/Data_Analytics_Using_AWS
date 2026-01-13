# Data_Analytics_Using_AWS
End-to-end AWS data analytics pipeline using S3, Athena, Glue, and QuickSight.

## 📌 Project Overview

This project demonstrates a complete **end-to-end data analytics pipeline built on AWS**. The objective of the project was to understand how raw data can be stored, queried, cleaned, transformed, automated, and finally visualized using AWS analytics services.

---

## 🛠️ Technologies & Services Used

* **Amazon S3** – Data storage
* **Amazon Athena** – SQL queries on S3 data
* **AWS Glue** – ETL and schema automation
* **AWS Glue DataBrew** – Visual data cleaning and transformation
* **Amazon QuickSight** – Data visualization and dashboards

---

## 🏗️ Project Architecture

```
Raw CSV Data
     ↓
Amazon S3 (Storage)
     ↓
Amazon Athena (SQL Queries)
     ↓
AWS Glue / Glue DataBrew (Cleaning & ETL)
     ↓
Amazon QuickSight (Dashboards & Insights)
```

---

## 📂 Step-by-Step Implementation

### 1️⃣ Data Storage – Amazon S3

* Created an S3 bucket with public access blocked.
* Uploaded structured CSV datasets.
* Used **Standard Storage** for active data and **Glacier Deep Archive** for long-term storage.
* Organized data using folders to support analytics tools.

**Key Takeaway:** Athena and Glue read data at the *folder level*, not individual files.

---

### 2️⃣ Data Querying – Amazon Athena

* Configured Athena query result location in S3.
* Created databases and tables pointing to S3 folders.
* Manually defined schema for CSV files.
* Ran SQL queries to filter and analyze data.

**Key Takeaway:** Query output must be stored separately from raw data to avoid corruption.

---

### 3️⃣ Data Cleaning – AWS Glue DataBrew

* Created a DataBrew project using a sample dataset.
* Applied transformations such as filtering, grouping, aggregation, and sorting.
* Saved transformations as reusable **recipes**.
* Ran DataBrew jobs to generate cleaned datasets.
* Configured job output to produce a **single CSV file**.

**Key Takeaway:** DataBrew provides a seamless approach for data preparation.

---

### 4️⃣ Schema Automation – AWS Glue Crawlers

* Created a Glue Crawler to scan S3 data.
* Automatically detected column names and data types.
* Stored metadata in the **Glue Data Catalog**.
* Verified tables were available in Athena.

**Key Takeaway:** Crawlers remove the need for manual table creation and support automation.

---

### 5️⃣ ETL Pipeline – AWS Glue

* Built ETL workflows using Glue Visual ETL.
* Connected multiple S3 data sources.
* Applied transformations such as **Union**.
* Stored processed data back into S3.
* Automatically updated Glue Data Catalog tables.

**Key Takeaway:** Glue ETL supports scalable and production-ready pipelines.

<img width="1919" height="968" alt="ETL-SS" src="https://github.com/user-attachments/assets/e602ea7e-a9d4-4f86-8db6-5f69e79ea252" />

---

### 6️⃣ Data Visualization – Amazon QuickSight

* Connected QuickSight to Athena datasets.
* Created interactive charts and dashboards.
* Customized visuals, tooltips, and labels.

**Key Takeaway:** QuickSight is AWS’s native BI tool with strong Athena integration.

---

## ✅ Final Outcome

* Built a fully functional AWS-based analytics pipeline.
* Converted raw CSV data into clean, queryable, and visual insights.
* Gained hands-on experience with multiple AWS analytics services.

---

## 🎯 Skills Demonstrated

* Cloud Data Analytics
* SQL on Cloud Data
* ETL Pipeline Design
* Data Cleaning & Transformation
* AWS Glue & Athena Integration
* Dashboard Development
* IAM Roles & Permissions

---

## 🚀 Future Improvements

* Add real-time data ingestion.
* Integrate AWS Lambda for automation.
* Apply partitioning for Athena performance optimization.
* Connect QuickSight directly to production datasets.
