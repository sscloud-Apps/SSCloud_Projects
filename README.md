
# ❄️ Snowflake Data Platform Starter Project
## A foundational project repository for initializing, configuring, and managing a Snowflake data warehouse environment using SQL scripts and version-controlled database objects.

## 📌 Project Overview

## This repository provides a foundational architecture for deploying a Snowflake data warehouse following standard enterprise design practices. It includes scripts for:
* **Role-Based Access Control (RBAC):** Principle of least privilege security model.
* **Compute Architecture:** Virtual warehouse configuration and sizing.
* **Medallion Architecture:** Multi-layered schema implementation (**Bronze**, **Silver**, **Gold**).
* **Ingestion & Transformation:** COPY INTO commands and analytical view definitions.

## 📁 Repository Structure

```text
SSCloud_Projects/
├── config/
│   └── snowflake_config.template.yml  # Template configuration for environment settings
├── ddl/
│   ├── 01_setup_roles_and_privileges.sql    # Security & RBAC setup
│   ├── 02_setup_databases_and_schemas.sql   # Environment initialization
│   ├── 03_create_bronze_tables.sql           # Raw landing tables
│   ├── 04_create_silver_tables.sql           # Transformed/Staging tables
│   └── 05_create_gold_tables.sql             # Fact & Dimension schema setup
├── dml/
│   ├── 01_copy_into_bronze.sql        # Ingestion scripts
│   └── 02_transform_silver_gold.sql   # Transformation logic
├── data/                              # Sample CSV/JSON seed files
├── tests/                             # Data quality & verification SQL queries
    └── data_validation_checks.sql        # Data quality checks and assertion
├── .gitignore
├── LICENSE
└── README.md                          # Project documentation

