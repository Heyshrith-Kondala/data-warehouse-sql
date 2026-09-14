# SQL Data Warehouse - Medallion Architecture(Bronze / Silver / Gold)

An end-to-end SQL Server data warehouse that ingests raw ERP and CRM source data and transforms it into clean, analytics-ready datasets using the medallion architecture.

## Overview 

This project takes raw CSV source files and moves them through three progressively refined layers, ending in star-schema model ready for BI/reporting tools.

| Layer | Purpose | Approach |
|---|---|---|
| **Bronze** | Raw landing zone | Full load, truncate & insert, no transformations — preserves source data as-is for traceability |
| **Silver** | Cleaned & standardized | Data type fixes, deduplication, null handling, business rule application |
| **Gold** | Analytics-ready | Fact and dimension tables (star schema) built for querying and reporting |

## Architecture

```
Source (CSV: ERP + CRM)
        │
        ▼
   ┌─────────┐
   │ BRONZE  │  raw ingestion, no transforms
   └─────────┘
        │
        ▼
   ┌─────────┐
   │ SILVER  │  cleaning, standardization, data enrichment 
   └─────────┘
        │
        ▼
   ┌─────────┐
   │  GOLD   │  aggregations, business logic and rules
   └─────────┘
        │
        ▼
   SQL-based analytics & reporting
```

## Repository Structure

```
├── dataset/    # Raw source CSV files (ERP + CRM)
├── docs/       # Architecture diagrams and data documentation
├── scripts/    # SQL scripts for bronze/silver/gold layer builds
├── tests/      # Data quality checks
├── LICENSE
└── README.md
```

## Tools & Technologies

- SQL Server
- T-SQL (DDL, stored procedures, ETL logic)
- Draw.io (architecture diagrams)
- Git/GitHub (version control)







