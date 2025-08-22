# ETL Data Pipeline on Google Cloud with Cloud Data Fusion & Apache Airflow

## Project Overview  
This project demonstrates how to build an **ETL (Extract, Transform, Load) data pipeline** on **Google Cloud Platform (GCP)** using:
- **Google Cloud Data Fusion** for data transformation
- **Apache Airflow** for automation
- **BigQuery** for data storage and analysis
- **Looker Studio** for visualization

The data is **synthetically generated using the Faker library**, stored as a **CSV file**, and uploaded to **Google Cloud Storage (GCS)**. The pipeline extracts, transforms, and loads data into **BigQuery**, and an automated **Airflow DAG** ensures scheduled execution.

---

## Technologies Used  
- **Google Cloud Platform (GCP)**
  - Google Cloud Storage (GCS)
  - Cloud Data Fusion
  - BigQuery
  - Looker Studio
  - Cloud Composer (Apache Airflow)
- **Python** (for data generation & Airflow DAG)
- **Faker Library** (to create synthetic data)
- **SQL** (for querying in BigQuery)

---

## Architecture
![Architecture](https://github.com/muhdshahan/etl-pipeline-datafusion-airflow/blob/main/Architecture.png)

---

## Project Steps

### **Step 1: Data Generation (Extract Phase)**
- Used the **Faker library** to generate synthetic employee data.
- Created a **CSV file** containing fields like `first_name`, `last_name`, `email`, `address`, and `salary`.
- Saved the data locally and uploaded it to **Google Cloud Storage (GCS)**.

---

### **Step 2: Uploading Data to Google Cloud Storage (GCS)**
- Uploaded the CSV file to GCS to be used in the ETL pipeline.

---

### **Step 3: Data Processing with Cloud Data Fusion (Transform Phase)**
- Created a **Cloud Data Fusion pipeline** to transform the data.
- Applied transformations:
    - **Masked the salary** to protect sensitive information.
    - **Hashed the email** using SHA-256 for privacy.
    - **Concatenated first name and last name** into a `full_name` column.
- Configured the pipeline to write processed data to BigQuery.

---

### **Step 4: Loading Data into BigQuery (Load Phase)**
- Created a **BigQuery dataset (`employee`)**.
- Defined a table schema (`emp_data`).
- Verified data integrity through SQL queries.

---

### **Step 5: Data Visualization with Looker Studio**
- Connected **Looker Studio** to BigQuery.
- Created interactive dashboards with:
  - **Filters for exploring data**
  - **Tables displaying key insights**

---

### **Step 6: Automating with Apache Airflow**
- Created an **Airflow DAG** (`dag`) with two tasks:
  1. **Extract Data** – Load data from GCS to BigQuery.
  2. **Run Cloud Data Fusion pipeline** – Trigger the transformation process.

---

## Final Output
- **Data successfully extracted, transformed, and loaded into BigQuery**
- **Looker Studio dashboard visualizing processed data**
- **Automated ETL pipeline using Apache Airflow**
- **Data privacy maintained through salary masking and email hashing**

---

## Setup & Deployment
1. **Clone the repository:**
2. **Install dependencies:**
3. **Run the data generation script.**
4. **Upload the CSV to GCS.**
5. **Deploy Cloud Data Fusion pipeline.**
6. **Run the Airflow DAG.**
7. **Check data in BigQuery.**
8. **Create a Looker Studio dashboard.**

---

## Contact
For questions, contact me at **datasinan1111@gmail.com** or connect on LinkedIn **https://www.linkedin.com/in/muhammed-sinan-ev-0b96b131b/**.
