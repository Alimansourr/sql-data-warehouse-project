# Data Warehouse and Analytics Project

## Project Overview

This project demonstrates the design and implementation of a modern **Data Warehouse and Analytics solution** using **SQL Server**. The main objective is to consolidate sales data from multiple source systems, clean and transform the data, build an analytical data model, and generate useful business insights.

The project follows the **Medallion Architecture**, which organizes the data warehouse into three layers: **Bronze**, **Silver**, and **Gold**. This structure improves data quality, traceability, and usability for reporting and analysis.

---

## Project Objectives

The objective of this project is to build a modern data warehouse that consolidates sales data from two source systems:

* **CRM system**
* **ERP system**

The final data warehouse is designed to support analytical reporting and informed decision-making.

---

## Project Requirements

### Data Engineering Scope

The data warehouse should meet the following requirements:

* Import data from ERP and CRM source systems provided as CSV files.
* Store raw data in the Bronze layer.
* Clean and standardize data in the Silver layer.
* Integrate the cleaned data into a business-friendly model in the Gold layer.
* Build fact and dimension tables optimized for analytics.
* Focus only on the latest dataset; historical tracking is not required.
* Provide clear documentation for both technical and business users.

---

## Data Architecture

This project uses the **Medallion Architecture**:

### Bronze Layer

The Bronze layer stores the raw data exactly as received from the source CSV files.
No major transformations are applied at this stage.

### Silver Layer

The Silver layer contains cleaned and standardized data.
In this layer, data quality issues are fixed, such as:

* Missing values
* Duplicate records
* Inconsistent formats
* Invalid or incorrect values
* Standardization of names, dates, and categories

### Gold Layer

The Gold layer contains the final business-ready data model.
This layer includes fact and dimension tables that are used for reporting and analytics.

---

## ETL Process

The ETL process includes three main steps:

### 1. Extract

Data is extracted from CSV files provided by the ERP and CRM systems.

### 2. Transform

The extracted data is cleaned, standardized, and integrated.
Transformation steps include data cleansing, joining related datasets, creating surrogate keys, and preparing analytical tables.

### 3. Load

The transformed data is loaded into the appropriate data warehouse layers:

* Raw data into Bronze
* Cleaned data into Silver
* Analytical model into Gold

---

## Data Warehouse Layers

```text
Source CSV Files
       |
       v
Bronze Layer
Raw data from ERP and CRM
       |
       v
Silver Layer
Cleaned and standardized data
       |
       v
Gold Layer
Fact and dimension tables for analytics
```

---

## Technologies Used

* SQL Server
* SQL Server Management Studio
* T-SQL
* CSV files
* Data Warehouse Concepts
* ETL Pipelines
* Medallion Architecture
* Data Modeling

---

## Database Structure

The project is organized using three schemas inside the `DataWarehouse` database:

```text
DataWarehouse
│
├── bronze
│   └── Raw source tables
│
├── silver
│   └── Cleaned and transformed tables
│
└── gold
    └── Final analytical fact and dimension tables
```

---

## Data Modeling

The Gold layer is designed using a dimensional model suitable for analytics.

The model includes:

* **Dimension tables**: descriptive business entities such as customers, products, and dates.
* **Fact tables**: measurable business events such as sales transactions.

This structure allows users to easily analyze sales performance, customer behavior, and business trends.

---

## Analytics and Reporting

After building the data warehouse, SQL queries can be used to generate insights such as:

* Total sales
* Sales by product
* Sales by customer
* Sales by country or region
* Monthly sales trends
* Best-performing products
* Customer purchasing behavior

These insights help support business decision-making.

---

## Example Business Questions

This data warehouse can help answer questions such as:

* Which products generate the highest revenue?
* Which customers contribute the most to sales?
* How do sales change over time?
* Which regions have the strongest sales performance?
* What are the main trends in customer purchasing behavior?

---

## Project Skills Demonstrated

This project demonstrates practical skills in:

* SQL Development
* Data Engineering
* Data Warehouse Design
* ETL Pipeline Development
* Data Cleaning
* Data Integration
* Data Modeling
* Analytical Reporting
* Business Intelligence Preparation

---

## Project Outcome

The final result is a complete data warehouse solution that transforms raw ERP and CRM data into a clean, integrated, and analytics-ready model. The project shows how raw business data can be converted into meaningful insights using SQL Server and data warehousing best practices.

