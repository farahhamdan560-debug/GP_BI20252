# Business Intelligence Graduation Project Template

**University of Petra, Graduation Projects, Business Intelligence, 20252**



## Project Structure

```
smart DSS for pharmacy inventory and profit inventory/
├── README.md                 # Project overview (UPDATE THIS)
├── docs/                     # All project documentation
│   └── 01_project_description.md
├── data/
│   ├── raw/                  # Original data files
│   └── processed/            # Cleaned, transformed data
├── notebooks/                # Jupyter notebooks for analysis
├── src/                       # Source code (scripts, apps)
├── dashboards/               # BI tool exports (Tableau, Power BI, etc.)
├── models/                    # Trained ML/AI models
├── requirements.txt          # Python dependencies
└── .gitignore                # Git ignore file
```

---

## [Documentation Template Sections](docs/documentation.md)

## [**Title Page & Authors**](docs/documentation.md#title-page-authors)
```
[Smart DSS for pharmacy inventory and profit optimization]
Authors
- [Farah Hamdan], [202211233]
- [Lujain Alshibi], [202211156]

Supervised by: [Dr.husam barham]

Course: 307498 – Graduation Project
Semester: second semester , 2025/2026

Date: [Submission Date]
```

## [Table of Content](docs.domcumentation.md#table-of-content) 

- ### [**Abstract**](docs/documentation.md#abstract)
- ### [**Acknowledgment**](docs/documentation.md#acknowledgment)
- ### [**Business Intelligence Project Description and Objectives**](docs/documentation.md#business-intelligence-project-description-and-objectives)
- ### [**Data Research and Acquiring Effort**](docs/documentation.md#data-research-and-acquiring-effort)
- ### [**Data Description and Understanding**](docs/documentation.md#data-description-and-understanding)
- ### [**Data Primary Cleaning and Transformation**](docs/documentation.md#data-primary-cleaning-and-transformation)
- ### [**Data Visualization and Insights**](docs/documentation.md#data-visualization-and-insights)
- ### [**Dashboard Design & Business Insights**](docs/documentation.md#dashboard-design--business-insights)
- ### [**Advanced Analytics and AI Modeling**](docs/documentation.md#advanced-analytics-and-ai-modeling)
- ### [**Tools Research and Selection Effort**](docs/documentation.md#tools-research-and-selection-effort)
- ### [**Project Deployment Effort – Use Case**](docs/documentation.md#project-deployment-effort-use-case)
- ### [**Results**](docs/documentation.md#results)
- ### [**References**](docs/documentation.md#references)
# Smart Decision Support System (DSS) for Pharmacy Inventory Management

An integrated Business Intelligence (BI) and Decision Support System designed to optimize inventory levels, manage pharmacy stock, and support strategic decision-making through advanced data analytics.

---

## 🎯 Project Scope & Data Understanding
The system operates on historical pharmacy transaction logs, structured around the exact data dictionary specified in the project documentation:
* **Barcode (الباركود):** Unique identifier for medication tracking.
* **Drug Name (اسم الدواء):** Commercial or generic brand names.
* **Entered Quantity (الكمية المدخلة):** Total batch volume received.
* **Expiration Date (تاريخ الانتهاء):** The core temporal parameter for shelf-life tracking and alerting.
* **Remaining Quantity (الكمية المتبقية):** Real-time shelf balance used for stockout risk detection.
* **Entry ID & Type (رقم ونوع الإدخال):** Audit trails used to isolate actual supply movements from manual adjustments.
* **Purchase Price (سعر الشراء):** Financial metric used to calculate tied-up capital and dead-stock losses.
* **Entry Date (تاريخ الإدخال):** Timeline marker for calculating item holding times.

---

## 🚀 Technical Methodology & Pipeline

### 1. Data Preparation & ETL (KNIME)
* **Data Cleansing:** Implemented structured workflows to handle missing system attributes, eliminate duplicate transaction numbers, and audit physical data types.
* **Data Transformation:** Filtered transactional noise using internal entry type codes, leaving an optimized, deployment-ready dataset (`cleaned.xlsx`).

### 2. Business Intelligence & Dashboard Engineering (Power BI)
* **Interactive Visualization:** Designed custom visual interfaces tracking dynamic supply metrics, near-expiry alerts, and sales performance indicators.
* **Analytical Modeling (DAX):** Built advanced DAX measures to calculate moving averages, precise reorder points, and cumulative profit tracking.

### 3. Decision Support & Advanced Analytics
* **Predictive Analysis (Time Series Forecasting):** Deployed demand forecasting directly integrated into the dashboard pipeline to guide automated procurement and minimize stockouts.
* **Descriptive Segmentation (Cluster Analysis):** Applied advanced machine learning algorithms (K-Means Clustering) to categorize inventory products into operational clusters based on velocity and purchasing behavior.

---

## 📁 Repository Structure
* 📊 **`/dashboards`**: Contains the primary Power BI application files (`.pbix`).
* 📁 **`/data`**: Contains both raw transactional source logs and the refined processed dataset.
* 📁 **`/docs`**: Complete academic documentation, technical reports, and system architectures.
* 📁 **`/models`**: Full descriptive documentation, evaluation charts, and screenshots of forecasting and clustering configurations.

---

## 🎓 Developed By
* **Farah Hamdan** & **lujain ALshibi** team   
* *Department of Business Intelligence - University of Petra*
