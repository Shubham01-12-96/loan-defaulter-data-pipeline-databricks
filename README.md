# Loan Defaulter Data Pipeline using Databricks & PySpark

## Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Solution Architecture](#solution-architecture)
- [Technologies Used](#technologies-used)
- [Key Features](#key-features)
- [Execution Workflow](#execution-workflow)
- [Real-World Use Case](#real-world-use-case)
- [Production Readiness Considerations](#production-readiness-considerations)
- [Outcome](#outcome)
- [Repository Structure](#repository-structure)
- [Key Takeaway](#key-takeaway)

---

## Project Overview

This project demonstrates how to build a scalable Loan Data Engineering Pipeline using PySpark on Databricks. It simulates a real-world financial data processing scenario where loan application data must be validated, cleaned, and prepared before being used for risk assessment or predictive modeling.

The pipeline ensures high-quality financial data through schema enforcement, validation checks, missing value handling, and distributed outlier detection.

---

## Problem Statement

Financial institutions rely on accurate and clean loan data to assess borrower risk and prevent loan defaults. However, real-world financial datasets often contain:

- Missing values  
- Duplicate records  
- Inconsistent schema definitions  
- Extreme outliers in financial metrics  

Poor data quality directly impacts credit risk models, increases financial exposure, and leads to incorrect lending decisions.

The objective of this project is to build a scalable data engineering pipeline using Databricks and PySpark to:

- Enforce schema validation  
- Perform data quality checks  
- Detect and handle missing values  
- Identify and flag financial outliers using the IQR method  
- Prepare a reliable dataset for downstream risk modeling  

---

## Solution Architecture

Raw Loan CSV  
⬇  
Schema Enforcement using StructType  
⬇  
Data Validation (Record Count, Distinct Check, Null Audit)  
⬇  
Missing Value Handling  
⬇  
IQR-Based Outlier Detection (approxQuantile)  
⬇  
Clean & Reliable Dataset  

<!-- Add your screenshot below after uploading it to images folder -->
<!-- ![Loan Pipeline Execution](images/notebook_execution.png) -->

---

## Technologies Used

- Azure Databricks  
- PySpark  
- Spark SQL  
- Python  
- Matplotlib  
- Git & GitHub  

---

## Key Features

✔ Custom schema enforcement using StructType  
✔ Dynamic schema generation from structured definition  
✔ Automated null value auditing across all columns  
✔ Duplicate record validation  
✔ Missing value handling for categorical data (Emp_Type → "Missing")  
✔ Distributed IQR-based outlier detection using approxQuantile  
✔ Functional programming approach using reduce()  
✔ Modular, production-oriented design  

---

## Execution Workflow

1. Define a custom schema to ensure data type consistency  
2. Load CSV file using enforced schema  
3. Validate total and distinct record counts  
4. Perform null value audit dynamically across all columns  
5. Identify columns with missing values  
6. Handle missing categorical values  
7. Calculate Q1 and Q3 using approxQuantile  
8. Compute IQR and determine lower/upper bounds  
9. Flag and filter financial outliers  
10. Produce a clean dataset ready for modeling or analytics  

---

## Real-World Use Case

This solution can be applied in:

- Banking & Financial Services  
- NBFCs (Non-Banking Financial Companies)  
- Loan Underwriting Systems  
- Credit Risk Analytics Platforms  

It ensures:

- Reliable borrower risk assessment  
- Reduced model bias due to dirty data  
- Detection of abnormal financial patterns  
- Improved regulatory compliance  

---

## Production Readiness Considerations

✔ Designed for distributed processing in Spark  
✔ Schema validation enforces strong data contracts  
✔ Scalable to millions of loan records  
✔ Easily integrable with:
  - Delta Lake  
  - Unity Catalog  
  - CI/CD pipelines  
  - ML modeling layers  
✔ Modular structure (ingestion, validation, preprocessing, outlier detection)  

---

## Outcome

- Improved financial data reliability  
- Reduced anomalies in numeric attributes  
- Automated quality checks  
- Clean dataset suitable for risk analytics  
- Foundation built for loan default prediction models  

---


---

## Key Takeaway

This project demonstrates strong Data Engineering capabilities including schema enforcement, distributed data validation, automated null auditing, and scalable outlier detection using PySpark in Databricks.

It highlights the critical role of data quality in financial risk systems and builds a solid foundation for enterprise-grade loan default prediction pipelines.



