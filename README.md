# Elevate ETL Data Pipeline - Enhanced Edition
A comprehensive, enterprise-grade Extract, Transform, Load (ETL) data pipeline built with SQLite for processing customer, product, and sales data with advanced monitoring, data quality controls, and automated operations.

## 🚀 Project Overview

This advanced ETL pipeline transforms raw CSV data into a structured data warehouse with proper data types, relationships, and comprehensive audit trails. The system features multi-layer data validation, automated data quality monitoring, real-time alerting, and advanced analytics capabilities.

## 🏗️ Architecture

### Enhanced Data Flow
1. **Extract**: Raw CSV files are loaded into staging tables with validation
2. **Validate**: Data quality checks and business rule validation
3. **Transform**: Data is cleaned, standardized, and enriched
4. **Load**: Clean data is loaded into production tables with ACID compliance
5. **Monitor**: Real-time monitoring and alerting
6. **Audit**: Comprehensive audit trails and change tracking

### Database Schema

#### Staging Layer (Raw Data Ingestion)
- `stg_customers` - Raw customer data with ingestion metadata
- `stg_products` - Raw product data with source tracking
- `stg_sales` - Raw sales transaction data with validation flags
- `stg_data_lineage` - Tracks data source and ingestion details

#### Production Layer (Clean Data)
- `dim_customers` - Customer dimension with SCD Type 2 support
- `dim_products` - Product dimension with category hierarchy
- `dim_sales_reps` - Sales representative dimension
- `dim_time` - Time dimension for temporal analysis
- `fact_sales` - Sales fact table with comprehensive metrics
- `fact_inventory` - Inventory tracking fact table

#### Audit & Monitoring Layer
- `audit_etl_log` - Enhanced ETL process execution tracking
- `audit_data_quality` - Detailed data quality metrics
- `audit_record_changes` - Complete change data capture
- `audit_performance_metrics` - ETL performance monitoring
- `audit_alerts` - System alerts and notifications
- `audit_data_lineage` - End-to-end data lineage tracking

#### Configuration Layer
- `config_etl_parameters` - Runtime configuration parameters
- `config_data_quality_rules` - Configurable data quality rules
- `config_alert_thresholds` - Alert threshold configurations
- `config_retention_policies` - Data retention policy settings

## 📁 Enhanced Files Structure

```
├── sql/
│   ├── schema/
│   │   ├── 01_create_staging_tables.sql
│   │   ├── 02_create_production_tables.sql
│   │   ├── 03_create_audit_tables.sql
│   │   ├── 04_create_configuration_tables.sql
│   │   └── 05_create_indexes.sql
│   ├── procedures/
│   │   ├── data_validation.sql
│   │   ├── data_transformation.sql
│   │   ├── data_quality_checks.sql
│   │   └── maintenance_procedures.sql
│   ├── triggers/
│   │   ├── audit_triggers.sql
│   │   ├── data_quality_triggers.sql
│   │   └── alert_triggers.sql
│   ├── views/
│   │   ├── reporting_vi
