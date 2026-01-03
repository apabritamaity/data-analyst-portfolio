# Methodology

The methodology encompasses data preprocessing, exploratory data analysis (EDA), feature engineering, model selection, evaluation, and interpretation of results.

The project is organized into clearly defined layers to separate responsibilities and improve maintainability:

```
data → scripts → sql → notebooks → dashboards → reports → docs
```

Each layer corresponds to a specific stage in the analytics lifecycle.

<br/>

### Data Ingestion (Raw Data Layer)

**Location:** `data/raw/`

- The original CSV dataset is stored without modification.
- This directory acts as the single source of truth.

File:
- `telco_customer_churn.csv`

<br/>

### Data Cleaning (Processing Layer)

**Location:** `scripts/data_cleaning.py`

Data cleaning includes:
- Removing duplicate records
- Handling missing or inconsistent values
- Validating data types and ranges

The cleaned dataset is saved to:

**Location:** `data/processed/cleaned_telco_churn.csv`

<br/>

### Feature Engineering

**Location:** `scripts/feature_engineering.py`

Feature engineering is performed to improve interpretability and analysis, including:
- Tenure-based customer groupings
- Monthly spend buckets
- Simplified categorical groupings

These features support segmentation and business analysis.

<br/>

### Database Integration

**Locations:**
- `sql/schema.sql`
- `scripts/load_to_mysql.py`

Steps:
- A MySQL database is used as the analytical data store
- A structured schema is defined to represent customer data
- The cleaned dataset is loaded into MySQL using Python

The database acts as the **single source of truth** for analysis, dashboards, and reporting.

<br/>

### SQL-Based Analysis

**Location:** `sql/`

- `data_quality_checks.sql`  
  Used to validate row counts, null values, and data integrity.

- `business_analysis.sql`  
  Contains business-focused SQL queries to compute KPIs such as churn rate and segment-level churn.

SQL is the primary tool for generating analytical insights.

<br/>

### Pipeline Automation

**Location:** `scripts/main.py`

The entire pipeline—from data cleaning to SQL analysis—is orchestrated through a single entry point to ensure reproducibility.

This enables the project to be executed end-to-end with one command.

<br/>

### Exploratory Data Analysis (EDA)

**Location:** `notebooks/`

Notebooks are used for exploratory analysis and insight validation:
- `01_data_overview.ipynb` – Dataset structure and basic statistics
- `02_eda.ipynb` – Visual exploration of churn patterns
- `03_insights_validation.ipynb` – Validation of SQL insights using charts

Notebooks focus on **exploration and storytelling**, not pipeline automation.

<br/>

### Dashboard Development

**Location:** `dashboards/`

Dashboards are created using BI tools and connected directly to the MySQL database.

- `dashboards/tableau/` – Tableau dashboard and screenshots
- `dashboards/powerbi/` – Power BI dashboard and screenshots

These dashboards present churn KPIs and trends for non-technical stakeholders.

<br/>

### Insight Generation

Analytical results from SQL, notebooks, and dashboards are interpreted in a business context to identify:
- High-risk customer segments
- Retention opportunities
- Service and pricing-related churn drivers

<br/>

### Reporting

**Location:** `reports/`

- `insights_report.md` – Detailed analytical insights and recommendations
- `executive_summary.pdf` – High-level summary for decision-makers
- `figures/` – Key charts used in reports

Reports focus on clarity, impact, and actionability.

<br/>

### Documentation

**Location:** `docs/`

Supporting documentation ensures transparency and clarity:
- `problem_statement.md`
- `dataset_description.md`
- `methodology.md`
- `assumptions_and_limitations.md`

<br/>

### Data Quality & Validation

**Location:** `tests/`

Automated checks are included to validate:
- Data integrity
- Schema consistency
- Basic quality rules

This reflects best practices for reliable analytics.
