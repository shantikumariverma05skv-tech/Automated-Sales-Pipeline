# Automated Sales Data Cleaning & Reporting Pipeline

**Author:** Shanti Kumari Verma  
**Role Simulated:** Data Analyst  

---

## 📌 Objective
Automate data cleaning and reporting for raw sales data to reduce manual effort and improve reporting accuracy.

---

## 🧩 Business Problem Statement
Manual sales reporting is:
- Time-consuming  
- Error-prone  
- Difficult to scale  

**Business teams require:**
- Monthly sales insights  
- Category-level performance analysis  
- Standardized KPI reporting  

**Goal:** Build a fully automated Python-based data cleaning and reporting pipeline.

---

## 🛠 Tools Used
- Python  
- Pandas  
- NumPy  
- Excel  

---

## 📊 Dataset Overview
- **Dataset Name:** Superstore Sales Dataset  
- **Total Records:** 9,800+  
- **Total Columns:** 18  

### Key Columns
- Order Date  
- Category  
- Sub-Category  
- Sales  

**Caption:** Raw Superstore sales dataset containing inconsistent formats, missing values, and categorical inconsistencies typical of real business data.

---

## 🧹 Data Cleaning & Feature Engineering
- Removed duplicate records  
- Handled missing values  
- Converted date columns to datetime  
- Standardized column names  
- Validated numeric fields (Sales)  
- Created Month and Year features  

**Caption:** Cleaned dataset with engineered time-based and categorical features.

---

## 🔁 Automation Workflow
Raw CSV → Python Script → Cleaned CSV → Excel Report
- Fully automated using a single command  
- No manual Excel work required  

---

## ⚙ End-to-End Automation Pipeline
- Config-driven file paths  
- Error handling & logging  
- Command-line execution  
- Date-stamped output files  

**Caption:** Python script implementing end-to-end automated data processing.

---

## 📈 Business Reporting (Excel Summary)

### KPIs Generated
- Total Sales  
- Average Sales  
- Maximum Sale  
- Total Orders  

### Reports Included
- Executive Summary Sheet  
- Monthly Sales Trend  
- Category-wise Sales Analysis  

**Caption:** Executive-ready Excel report for business stakeholders.

---

## 🚀 Results & Impact
- Reduced reporting time from hours to seconds  
- Standardized KPI calculation  
- Enabled repeatable and scalable reporting  

---

## 🏁 Conclusion
This project demonstrates the ability to design a reliable data automation pipeline, transform raw business data into structured insights, and deliver executive-ready reports using Python and Excel.

> Below is a high-level excerpt from the automation script. Full implementation is available in `automation.py`.

## Python Automation Script

The complete automation logic is implemented in `automation.py`.
The script performs the following steps:

- Loads file paths from `config.json`
- Reads raw sales data from the input folder
- Cleans and validates data
- Performs feature engineering
- Calculates business KPIs
- Generates an Excel report with multiple sheets
- Writes execution logs with timestamps



### Config-Driven Design (Example)

```python
with open("config.json", "r") as f:
    config = json.load(f)

RAW_DATA_PATH = config["raw_data_path"]
CLEANED_DATA_PATH = config["cleaned_data_path"]
LOG_PATH = config["log_path"]
REPORT_PATH = config["report_path"]

## 📂 Folder Structure

```text
Automated-Sales-Reporting/
│
├── automation.py
├── config.json
│
├── input/
│   └── superstore_sales_raw.csv
│
├── output/
│   ├── cleaned_data/
│   │   └── cleaned_superstore.csv
│   │
│   ├── logs/
│   │   └── log_2026-01-21.txt
│   │
│   └── reports/
│       └── superstore_summary_2026-01-21.xlsx
