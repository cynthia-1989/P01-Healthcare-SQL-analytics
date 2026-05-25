# P01 ⭐ — Healthcare SQL 🏥

## Overview

This project builds a healthcare SQL extraction pipeline for analysing patient records, appointment activity, hospital billing information, doctor performance, and departmental operations.

The pipeline connects to a PostgreSQL healthcare database, performs SQL extraction queries, joins multiple healthcare tables, and generates a flat raw dataset for downstream ETL and analytics workflows.

---

## Table of Contents

1. [Project Brief](#project-brief)
2. [SQL Workflow](#sql-workflow)
3. [Input and Output](#input-and-output)
4. [Project Structure](#project-structure)
5. [Patient Analysis](#patient-analysis)
6. [Appointment Analysis](#appointment-analysis)
7. [Billing Analysis](#billing-analysis)
8. [Aggregation Queries](#aggregation-queries)
9. [Join Operations](#join-operations)
10. [CTE and Window Functions](#cte-and-window-functions)
11. [Visualisations](#visualisations)
12. [How to Run](#how-to-run)
13. [Tests](#tests)
14. [Git Workflow](#git-workflow)

---

## Project Brief

**Company:** MedCore Analytics  
**Client:** St. Aurelius General Hospital  
**Role:** Data Analyst

The healthcare dataset includes records such as:

- Patient records
- Appointment history
- Billing transactions
- Doctor information
- Department operations

The analysis focuses on extracting operational healthcare data from PostgreSQL and preparing a flat analytical dataset for downstream ETL processing.

---

## SQL Workflow

### 1. Database Connection

Connect to the PostgreSQL healthcare database using:

- Supabase
- SQLAlchemy
- PostgreSQL driver

Database schema used:

```text
healthcare
```

---

### 2. SQL Extraction

Run SQL extraction queries against the healthcare schema.

Key healthcare tables include:

```text
patients
appointments
billing
doctors
departments
```

---

### 3. SQL Basics

The project includes basic SQL operations such as:

- SELECT
- WHERE
- ORDER BY
- LIMIT
- DISTINCT

---

### 4. Aggregation Queries

The project performs healthcare aggregations including:

- Patient counts
- Appointment totals
- Revenue summaries
- Billing averages
- Department statistics

SQL functions used include:

```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
GROUP BY
```

---

### 5. Join Operations

The project joins healthcare tables to create a flat analytical dataset.

Joins include:

- Patients + appointments
- Appointments + billing
- Doctors + departments
- Patient + billing history

The final dataset combines healthcare operational records into one extract.

---

### 6. CTE and Window Functions

The project includes advanced SQL using:

- Common Table Expressions (CTEs)
- Window functions

Examples include:

```sql
ROW_NUMBER()
RANK()
DENSE_RANK()
OVER(PARTITION BY ...)
```

CTEs are used to simplify complex healthcare analytics queries.

---

## Input and Output

### Input

```text
PostgreSQL healthcare database
```

### Outputs

```text
data/raw-data.csv
sql/
reports/
```

---

## Project Structure

```text
P01-healthcare-sql/
│
├── data/
│   └── raw-data.csv
│
├── reports/
│
├── sql/
│   ├── 01_sql_basics.sql
│   ├── 02_aggregations.sql
│   ├── 03_joins.sql
│   ├── 04_cte_window.sql
│   └── 05_extract_raw_data.sql
│
├── src/
│   ├── query_runner.py
│   └── data_extractor.py
│
├── tests/
│
├── run.py
├── config.py
├── requirements.txt
└── README.md
```

---

## Patient Analysis

The project analyses patient healthcare data including:

- Patient demographics
- Age distribution
- Gender analysis
- Patient registration activity
- Patient appointment history

Metrics generated include:

- Total patients
- Average patient age
- Patient counts by gender
- Active patient statistics

---

## Appointment Analysis

The project analyses hospital appointment records.

Analysis includes:

- Appointment counts
- Appointment scheduling activity
- Doctor appointment workload
- Department appointment statistics

Metrics generated include:

- Total appointments
- Average appointments per doctor
- Appointment trends
- Department activity

---

## Billing Analysis

The project analyses hospital financial records.

Analysis includes:

- Billing totals
- Revenue summaries
- Patient billing history
- Average billing amount
- Department billing performance

Metrics generated include:

- Total hospital revenue
- Average billing amount
- Revenue by department
- Revenue by doctor

---

## Aggregation Queries

The project performs healthcare aggregation analysis using:

```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
GROUP BY
```

Aggregations help summarise operational hospital activity.

---

## Join Operations

The project joins multiple healthcare tables into one analytical dataset.

Joined tables include:

```text
patients
appointments
billing
doctors
departments
```

The joined dataset is exported as:

```text
data/raw-data.csv
```

---

## CTE and Window Functions

Advanced SQL functionality includes:

- CTE-based queries
- Ranking functions
- Partitioned analysis
- Running totals

Examples include:

- Ranking doctors by appointment count
- Ranking departments by revenue
- Patient billing comparisons

---

## Visualisations

The project notebook can generate healthcare visualisations including:

- Patient distribution charts
- Appointment activity charts
- Revenue comparison charts
- Department performance charts

Saved charts are stored in:

```text
reports/
```

---

## How to Run

Run the complete healthcare SQL extraction pipeline:

```bash
python run.py
```

The pipeline performs:

1. Database connection
2. SQL query execution
3. Join extraction
4. Raw dataset creation
5. CSV export

---

## Tests

Run unit tests using:

```bash
pytest tests/
```

Tests cover:

- Database connectivity
- SQL query execution
- Aggregation queries
- Join operations
- Data extraction
- CSV generation

---

## Git Workflow

```bash
git status
git add .
git commit -m "feat: complete healthcare SQL extraction project"
git push
```

---

## Success Criteria Achieved

- Database connection successful
- SQL basics completed
- Aggregation queries completed
- Join operations completed
- CTE and window functions implemented
- raw-data.csv generated
- Multiple tables joined successfully
- Project pushed to GitHub

---