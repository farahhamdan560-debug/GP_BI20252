# Business Intelligence Graduation Project Template

**University of Petra, Graduation Projects, Business Intelligence, 20252**

---

## How to Use This Template

This repository serves as a **template for Business Intelligence graduation projects**. Students should **fork this repository** and use it as the foundation for their project work. All project-related files and documentation should be organized within this single repository.

### For Students: Quick Start
1. **Fork this repository** (Click on **Use this template** then **Create new repository** button in the top right corner) to fork your own copy.

![use-this-template](images/use-template.png)

2. **Clone your fork** to your local machine
3. **Follow the sections below** to structure your project documentation in markdown format
4. **Push your work** regularly to track progress

---

## Project Structure

```
Pharmacy Data and Decision Support System/
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
[Pharmacy Data and Decision Support System]

Authors
- [Farah Hamdan], [202211233]
- [Lujain Alshibi], [202211156]

Supervised by: [Dr.husam barham]

Course: 307498 – Graduation Project
Semester: First Semester, 2025/2026

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



## [**Abstract**](docs/documentation.md#abstract)
The management of pharmaceutical inventory represents a complex logistical challenge that demands high precision to balance patient needs with the reduction of waste caused by expired medications. This project aims to develop a comprehensive Decision Support System (DSS) based on historical pharmacy data analysis. The primary goal is to automate stock movement monitoring and provide proactive insights that enhance internal supply chain efficiency and ensure the optimal allocation of financial resources.

The project was executed by analyzing a real-world dataset comprising over 4,500 records. Data processing was conducted using the KNIME platform, where machine learning algorithms—specifically the Random Forest model—were applied to predict future demand patterns based on entry dates and purchase prices. Furthermore, interactive analytical dashboards were designed using Power BI, utilizing advanced DAX measures to extract key performance indicators (KPIs), such as imminent expiration alerts and high-turnover drug analysis, thereby streamlining the oversight process for system administrators.

The project concluded with significant results in transforming raw data into strategic assets. The system demonstrated a high capability to identify fast-moving items (such as Revanin and Tratul) and medications at risk of expiration, contributing to a notable reduction in financial losses. This system provides pharmacists and stakeholders with a holistic, real-time view that supports sustainable pharmaceutical supply with high efficiency, establishing the proposed solution as a fundamental pillar for digital transformation in small to medium-sized healthcare facilities.

## [**Acknowledgment**](docs/documentation.md#acknowledgment)
Upon the completion of this research work and the development of the "Pharmacy Decision Support System (DSS)", I would like to express my deepest gratitude and sincere appreciation to everyone who supported and guided me throughout my academic journey and the execution of this project.

I would like to extend my heartfelt thanks and appreciation to my academic supervisor for their invaluable guidance, constant patience, and constructive feedback. Their deep expertise and scientific vision were instrumental in shaping the methodology of this work and steering it in the right direction.

I also express my sincere gratitude to the faculty and staff of the College of Information Technology and the Department of Business Intelligence and Data Analytics for providing the strong academic foundation and knowledge that made the development of this statistical and predictive system possible.

Furthermore, I am deeply grateful to the pharmacy administration and the organizations that provided us with the real-world inventory and drug transaction dataset. This precise data—including detailed records of expiration dates, remaining quantities, and purchasing prices—was essential in building and validating accurate predictive models that simulate real-world healthcare challenges and advanced data analytics.

## [**Business Intelligence Project Description and Objectives**](docs/documentation.md#business-intelligence-project-description-and-objectives)
1. What is your project about?
The project involves the design and development of a computerized Pharmacy Decision Support System (DSS) based on Business Intelligence (BI) tools and statistical data analysis. The system extracts daily transactional logs accumulated within the pharmacy—such as entered quantities, remaining stock, expiration dates, and purchase prices. It then cleanses and processes this data to display it on interactive dashboards. These visual dashboards enable pharmacy management to monitor stock movements accurately and forecast future demands instead of relying on intuition or guesswork.

2. What industry or business domain does it address?
The project directly targets the Pharmaceutical and Healthcare Retail sector, specifically focusing on Inventory Management and Supply Chains in Pharmacies. This domain is highly critical because it requires a precise balance between two aspects: the commercial and financial side (maintaining pharmacy profitability, reducing waste, and avoiding tied-up liquidity) and the humanitarian/medical side (ensuring the continuous availability of critical medications and alternative treatments for patients in a safe, unexpired condition).

3. How will it help the industry/business?
The project shifts pharmacy operations from a traditional reactive workflow (waiting for a problem to occur) to a proactive strategy by:

Reducing Tied-Up Capital: It highlights slow-moving and dead stock to prevent the procurement team from ordering unnecessary additional quantities.

Automating Inventory Oversight: It eliminates the need for periodic manual shelf inspections by pharmacists, making all key indicators (quantities, dates, and shortages) updated and instantly visible on-screen.

Improving Supplier Negotiations: It provides concrete metrics and reports regarding consumption volumes and historical pricing, giving the pharmacy greater leverage to secure better discounts or more favorable return policies from drug distributors.

4. What specific business problems are you solving?
Financial Loss from Expired Medications: Drugs have strict shelf lives. Due to massive stock accumulation, items often expire unnoticed, leading to direct financial losses. The system solves this by sorting medicines by expiry dates and sending early warning notifications (e.g., for products expiring within 3 or 6 months) so they can be cleared through promotions or returned to suppliers.

Sudden Stockouts of High-Demand Items: When essential medication stock drops to zero unexpectedly, it leads to lost customers and disrupts patient treatments. The system addresses this by continuously tracking "Remaining Quantity" and setting safety stock limits that alert the pharmacist to place a new order before the current batch is completely depleted.

Inaccurate Purchasing Orders: Often, newly supplied quantities ("Entered Quantity") do not match the actual consumption velocity of the pharmacy. The system links new procurement orders directly to historical consumption records to optimize the volume and timing of future orders.

Lack of Visibility for Decision Makers: Reviewing and understanding thousands of manual logs, scattered invoices, or raw spreadsheets is highly inefficient. The system aggregates all these operational movements (whether new stock entries, customer returns, or adjustments made under administrative privileges) and consolidates them into simple, clear data visualizations to support sound decision-making.

## [**Data Research and Acquiring Effort**](docs/documentation.md#data-research-and-acquiring-effort)
1. What data did you search for and why?
To build a practical decision support system capable of addressing inventory imbalances and expiration risks, the research focused on extracting highly granular transactional records covering the following areas:

Identification Parameters (الباركود / Barcode, اسم الدواء / Drug Name): Retreived to establish a unique identity for each product line, preventing any overlap between similar brand names during data aggregation and statistical tracking.

Stock Metrics (الكمية المدخلة / Entered Quantity, الكمية المتبقية / Remaining Quantity): Collected to analyze inventory turnover rates and consumption velocity, which serve as the baseline for calculating safety stock limits and reorder points.

Temporal Dimensions (تاريخ الإدخال / Entry Date, تاريخ الانتهاء / Expiration Date): Tracked as a critical factor to link procurement timelines with product shelf-life calculations, forming the core input for the early warning mechanism for near-expiry batches.

Financial Metrics (سعر الشراء / Purchase Price): Gathered to bridge logistical management with financial impact, allowing the pharmacy to evaluate current asset value and identify tied-up capital on shelves.

2. How did you acquire it? Sources, APIs, Scraping
Primary Approach: The data was acquired via Direct Extraction from the live operational database of the management information system (MIS) utilized by the cooperating pharmacy.

3.Why APIs or Web Scraping Were Not Used: While public APIs and web scraping methods were initially considered, preliminary research showed they only offer generalized medical data (such as active ingredients, drug classifications, or global generic names). They completely lack the internal, highly confidential commercial and operational metrics required to develop an actual Business Intelligence (BI) environment—such as real-time stock levels on shelves, localized purchase costs, and specific receipt dates for active batches. Therefore, direct database extraction from the local enterprise system was the only viable path to ensure project success.


4. Brief Description of Each Data Source
The Pharmacy Operational Dataset: This primary source consists of a structural transactional export (.csv / .xlsx) containing historical inventory adjustments and tracking logs. The schema includes relational keys (such as the transaction ID and barcode), text fields for drug names and logged users (admin), alongside continuous and integer values representing financial costs, quantities, and standard expiration date formats (YYYY-MM-DD). The dataset exhibits realistic stock depletion patterns—visible where multiple records show remaining quantities dropping to zero—providing an excellent practical foundation for training predictive models to detect impending stockouts.


## [**Data Description and Understanding**](docs/documentation.md#data-description-and-understanding)
1. Data Dictionary:
Field Name (Source):
-Barcode (الباركود): String / Numerical,The primary unique identifier for each medication package; prevents item overlap during analysis.
-Drug Name (اسم الدواء)	String,	The commercial brand or generic name; used on dashboards for quick searching and filtering.
-Entered Quantity (الكمية المدخلة)	: Integer, Represents the total stock volume received; used to calculate baseline procurement metrics.
-Expiration Date (تاريخ الانتهاء):	Date ,	The core parameter for the alerting system; used to calculate the remaining shelf life of products.
-Remaining Quantity (الكمية المتبقية):	Integer,	The active stock balance currently on shelves; monitored to prevent sudden stockouts.
-Entry ID (رقم الإدخال)	:Integer,	The transaction log number generated by the database; ensures full data auditability.
-Entry Type (نوع الإدخال)	:Categorical (Code),	Identifies the nature of the transaction (e.g., new supply or adjustment) for data filtering.
Purchase Price (سعر الشراء):	Decimal,	The unit cost paid to the supplier; used to evaluate tied-up capital and financial waste.
-Entry Date (تاريخ الإدخال):	Date, The exact date the stock was received; used to track holding time and inventory turnover.
-Username (اسم المستخدم)	:String,	The profile credential responsible for the entry; maintains operational security and accountability.
2. Exploratory Data Analysis (EDA)
Charts and Graphs Showing Data Distribution
To understand the baseline characteristics of the pharmacy operational dataset, distributions for critical numerical and temporal attributes were analyzed:

-Stock Depletion Distribution: Plotting the Remaining Quantity across all active entries reveals a highly skewed distribution. A substantial portion of records cluster at exactly 0, representing batches that have successfully cleared or items that are facing immediate stockouts. The remaining records show a normal distribution centered around common batch ordering sizes (e.g., 50, 100, and 200 units).

-Purchase Price Distribution: The financial data shows a long-tailed distribution heavily concentrated between lower to mid-tier price ranges (e.g., 1.00 to 5.00 currency units per pack), reflecting the high volume of daily generic medicines, with a few extreme outliers representing specialized or high-cost chronic treatments.

-Temporal Shelf-Life Distribution: Plotting the time delta between Entry Date and Expiration Date establishes that most medications arrive with a standard operational shelf life of 2 to 3 years. However, isolating records by Remaining Quantity > 0 reveals the current inventory's remaining shelf-life distribution, pointing out specific clusters of products expiring within the current calendar year.

Patterns Discovered
The Zero-Stock Outlier Pattern: A significant number of logs maintain a Remaining Quantity of zero while holding an Expiration Date far into the future. This confirms that stock depletion occurs long before chemical degradation for high-demand items, highlighting the vital need for a reorder-point mechanism to trigger procurement before the shelf is completely empty.

-Batch Splitting Anomalies: Analysis of identical barcodes under different Entry IDs showed that the same medication frequently enters the system in separate batches with varying expiration dates and slight fluctuations in Purchase Price. This dictates that the DSS must evaluate inventory on a batch-by-batch level (FIFO - First In, First Out) rather than treating a single drug name as a homogeneous entity.

-Admin Dominance in Logs: The Username attribute is overwhelmingly dominated by the admin profile across both inventory intake and adjustments. This indicates a highly centralized data entry point, highlighting the need for cleaner multi-user role tracking in future system updates to preserve operational accountability.

-Correlations and Relationships Found
Purchase Price vs. Consumption Speed: Cross-referencing Purchase Price with the rate of stock depletion (Entered Quantity minus Remaining Quantity over time) shows an inverse correlation. Low-cost items move significantly faster and represent high-velocity transactions, whereas high-priced medications exhibit slow turnover rates, meaning they sit on shelves much longer and carry a higher risk of expiring before being sold.

-Entry Type and Volume Extremes: Examining the relationship between Entry Type and Entered Quantity revealed that Entry Type 1 (Standard Intake) correlates with large, uniform blocks of quantities (e.g., 100, 200 units). In contrast, Entry Type 2 (Adjustments/Returns) correlates with very small, fragmented counts (e.g., 4 units), confirming that Type 2 entries represent minor shelf corrections or damaged item logging
--Insights Relevant to Project Objectives
Insight for Expiry Management: By identifying the specific clusters of high-cost, slow-moving items with short remaining shelf lives, the system can bypass generic alerts and generate high-priority financial risk alerts. This enables management to focus clearing efforts or distributor returns on items that would cause the highest monetary losses.

Insight for Procurement Optimization: The historical gap between Entered Quantity and Remaining Quantity across specific dates reveals distinct seasonal or recurring consumption trends for core drug lines like Revanin or Ciprover. This data provides the baseline parameters needed to transition the pharmacy from a fixed-quantity ordering method to an automated, demand-driven replenishment model.




## [**Data Primary Cleaning and Transformation**](docs/documentation.md#data-primary-cleaning-and-transformation) 
cleaning and transformation process phase done by knime.
1. Data Ingestion
Node: Excel Reader   
Action: The workflow begins by importing the raw data directly from an Excel spreadsheet.
2. Column-Level Filtering
Column-Level FilteringNode: Column Filter 
Action:  based on this node it excluded the column of اسم المستخدم from the excel table ,Because it contains a single, repeated value for all rows, which is (admin), it does not add any analytical value, which helps to make the data size smaller and easier to handle.
3. Text & Data Cleansing (Transformations)
Node: String Manipulation  
Action: in the expression box by the rule of strip("اسم الدواء") ,it cleans the column  of اسم الدواء from  extra spaces To ensure that the same medication is not repeated due to an empty space.
4. Data Type Conversions
Node: String to Date_Time 
Action: This is applied to the "Expiry Date" and "Entry Date" columns. This conversion is very important because without this node the program will treat the date as just words, while after this node it will be able in the future to calculate time differences and know how many days or months are left until the expiry of the medicines.
5. Row-Level Filtering (Handling Values/Rules)
Node: Rule_based Row Filter  
Action:This step ensures that any movements or rows entered incorrectly into the system are excluded (such as the quantity remaining in the warehouse being greater than the quantity that originally entered the pharmacy), by appling this crietira ($الكمية المتبقية$ > $الكمية المدخله$ => FALSE
TRUE => TRUE )

## [**Data Visualization and Insights**](docs/documentation.md#data-visualization-and-insights)
- Include relevant charts and describe each one
- Explain the significance of each visualization
- Highlight key insights from your charts
- What patterns do these visualizations reveal?

## [**Dashboard Design & Business Insights**](docs/documentation.md#dashboard-design--business-insights)
- Showcase your final BI Dashboard
- Organize by **Business Questions Answered**

For each chart/component:
```
Chart [#]: [Title]
Description: [What does this chart show?]
Insight Derived: [What does this tell the business? Why is this important?]
```

Examples:
- Chart 1: Sales Trend Analysis – Shows growth pattern

![An example of a chart.](images/image-rendered.webp)
> The chart shows a cat

- Chart 2: Customer Segmentation – Identifies high-value segments
- Chart 3: Regional Performance – Highlights top/bottom performers

## [**Advanced Analytics and AI Modeling**](docs/documentation.md#advanced-analytics-and-ai-modeling)
- What type of model did you build? (Clustering, Predictive, Association, Generative AI, forecasting, agents, etc.)
- What pre built AI models did you use and how?
- What results were you seeking or what attribute are you predicting?
- **Model Characteristics**: Such as Accuracy, precision, recall, weights, parameters
- Include multiple iterations if applicable
- Explain your findings and model performance

## [**Tools Research and Selection Effort**](docs/documentation.md#tools-research-and-selection-effort)
- What tools did you evaluate?
- Which tools did you ultimately choose?
- Why did you select these tools?
- How do they support your project?

Examples:
- Data Analysis: Python, R, SQL
- Visualization: Tableau, Power BI, Looker
- Deployment: Streamlit, Fast API, Gradio, Flask, Cloud platforms

## [**Project Deployment Effort – Use Case**](docs/documentation.md#project-deployment-effort-use-case)
- How will a business user consume this project?
  - Interactive web dashboard (Streamlit)?
  - Scheduled reports?
  - Dashboard
  - Live API?
  - Mobile app?
- Implementation steps in chronological order
- If you built a prototype, describe deployment process
- Infrastructure and hosting considerations

## [**Results**](docs/documentation.md#results)
- Summary of findings (2-3 paragraphs)
- Most important insights or charts in your opinion
- Evaluation and interpretation of results
- Business impact and recommendations

## [**References**](docs/documentation.md#references)
List all sources cited in your project using a consistent citation format (APA, Chicago, etc.)

---

## Code setup and dependencies Instructions
Write procedure for setup and running code.
for example:
1. Clone the repository: 
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory: 
   ```bash
   cd <project-directory>
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the application: 
   ```bash
   python app.py
   ```

---




## Documentation Best Practices

✅ **Do's:**
- Write in clear, descriptive language documenting your work effort.
- Use consistent formatting and headings
- Include visuals (charts, screenshots, diagrams)
- Add links to your data sources and tools
- Update regularly as your project evolves
- Use version control (git commits with meaningful messages)

❌ **Don'ts:**
- Don't use Word documents – use Markdown (.md) here [Documentation](docs/documentation.md) for project documentation and version control, link main sections of documentation at the readme overview and Table of Content, as shown in the template.
- Don't commit large data files directly – use `.gitignore` and reference external sources
- Don't leave sections incomplete – mark as TODO if not ready
- Don't forget to document your data sources and methodology

---

## Flexibility by Project Type

**This template is flexible.** Adapt based on your project focus:

| Project Type | Emphasis | Key Sections |
|---|---|---|
| **Dashboard-Heavy** | Visualization & Design | Sections 8-9 (Dashboard, Visualizations) |
| **Predictive Analytics** | Advanced Modeling | Section 10 (AI/ML Modeling) |
| **Data Engineering** | Cleaning & Transformation | Section 7 (Data Prep) |
| **Business Analysis** | Insights & Recommendations | Sections 5-6, 13 (Data, Results) |
| **Web Application** | Deployment & Use Cases | Section 12 (Deployment) |

---

## Getting Started

1. **Fork this repository** to your GitHub account
2. **Clone your fork**: `git clone <your-fork-url>`
3. **Create your project directory structure** using the template above
4. **Start documenting in Markdown** – one `.md` file per major section
5. **Commit regularly**: `git add . && git commit -m "Add data analysis"` && `git push`
6. **Important --> Link everything in your main README.md** so it's easy to navigate

---

## Additional Template Files to Create

Your students should also create these supporting files:

### `.gitignore` - Prevent committing unnecessary files
```
# Data files (if large)
data/raw/*.csv
data/raw/*.xlsx
data/processed/*.parquet

# Python
__pycache__/
*.py[cod]
*$py.class
*.egg-info/
.venv/
venv/

# Notebooks
.ipynb_checkpoints/

# Models
models/*.pkl
models/*.joblib

# IDE
.vscode/
.idea/

# OS
.DS_Store
Thumbs.db
```

### `requirements.txt` - Python dependencies
```
pandas==2.0.0
numpy==1.24.0
matplotlib==3.7.0
seaborn==0.12.0
plotly==5.14.0
scikit-learn==1.3.0
jupyter==1.0.0
streamlit==1.25.0
sqlalchemy==2.0.0
```

### `docs/SETUP.md` - Environment setup guide
```
# Project Setup Guide

## Prerequisites
- Python 3.8+
- Git
- GitHub account

## Installation Steps
1. Clone your fork: `git clone <your-fork-url>`
2. Create virtual environment: `python -m venv venv`
3. Activate: `source venv/bin/activate` (Mac/Linux) or `venv\Scripts\activate` (Windows)
4. Install dependencies: `pip install -r requirements.txt`
5. Start Jupyter: `jupyter notebook`

## Data Setup
1. Download data from sources listed in docs/02_data_research.md
2. Place raw data in `data/raw/`
3. Run data cleaning scripts in `notebooks/`
```

### `docs/EVALUATION_CRITERIA.md` - Grading rubric
```
# Evaluation Criteria

| Criterion | Excellent (90-100%) | Good (80-89%) | Satisfactory (70-79%) | Needs Improvement (<70%) |
|---|---|---|---|---|
| **Project Definition** | Clear objectives, well-defined problem | Objectives stated, minor clarity issues | Objectives present but vague | Missing or unclear objectives |
| **Data Research** | Comprehensive sources, well-justified | Good sources, mostly justified | Limited sources, weak justification | Poor data selection |
| **Data Analysis** | Thorough EDA, insightful findings | Good analysis, clear insights | Basic analysis, some insights | Minimal analysis |
| **Visualizations** | Professional, insightful, well-labeled | Good quality, mostly clear | Acceptable but basic | Poor quality/unclear |
| **Dashboard Design** | Intuitive, answers key questions | Good design, mostly effective | Functional but cluttered | Poorly designed |
| **Advanced Analytics** | Sophisticated models, well-evaluated | Good models, clear methodology | Basic models, limited evaluation | Minimal or missing |
| **Documentation** | Clear, complete, well-organized | Good documentation, minor gaps | Adequate but some gaps | Incomplete/unclear |
| **Deployment** | Complete, production-ready | Good implementation plan | Basic implementation | No deployment plan |
| **Results & Insights** | Significant findings, business value | Good findings, clear implications | Adequate results, limited impact | Minimal results |
| **Code Quality** | Well-commented, organized, reproducible | Good structure, mostly reproducible | Adequate but messy | Difficult to understand |
```

---

## Need Help?

- **Markdown Guide**: [GitHub Markdown Documentation](https://guides.github.com/features/mastering-markdown/)
- **Git Tutorial**: [Git Basics](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)
- **BI Tools**: Research and document your tool choices in Section 11
- **Data Sources**: APIs, UCI ML Repository, Government Open Data, Industry Datasets, Web scraping, etc.

---

**Good luck with your Business Intelligence graduation project!** 
