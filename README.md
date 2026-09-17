# SQL Data Warehouse - Medallion Architecture(Bronze / Silver / Gold)

An end-to-end SQL Server data warehouse that ingests raw ERP and CRM source data and transforms it into clean, analytics-ready datasets using the medallion architecture.

## Overview 

This project takes raw CSV source files and moves them through three progressively refined layers, ending in star-schema model ready for BI/reporting tools.

| Layer | Purpose | Approach |
|---|---|---|
| **Bronze** | Raw Ingestion | Full load, truncate & insert, no transformations — preserves source data as-is for traceability |
| **Silver** | Cleaned & standardized | Data type fixes, deduplication, null handling, business rule application |
| **Gold** | Analytics-ready | Fact and dimension tables (star schema) built for querying and reporting |

## Data Architecture

<img width="651" height="340" alt="data_architecture" src="https://github.com/user-attachments/assets/b61b4475-df00-466a-9f86-e204a6fba049" />

## Tools & Technologies

- SQL Server
- T-SQL (DDL, stored procedures, ETL logic)
- Draw.io (architecture diagrams)
- Git/GitHub (version control)

## Repository Structure

```
├── dataset/    # Raw source CSV files (ERP + CRM)
├── docs/       # Architecture diagrams and data documentation
├── scripts/    # SQL scripts for bronze/silver/gold layer builds
├── tests/      # Data quality checks
├── LICENSE
└── README.md
```

## Objective
Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

# Specifications
Data Sources: Import data from two source systems (ERP and CRM) provided as CSV files.
Data Quality: Cleanse and resolve data quality issues prior to analysis.
Integration: Combine both sources into a single, user-friendly data model designed for analytical queries.
Scope: Focus on the latest dataset only; historization of data is not required.
Documentation: Provide clear documentation of the data model to support both business stakeholders and analytics teams.

## Data Model 














