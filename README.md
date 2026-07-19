# 📊 AtliQ Hardware Business Intelligence Project

> **An end-to-end Business Intelligence project built using Power BI, Power Query, DAX, SQL, and dimensional data modeling to transform raw business data into actionable insights.**

![Status](https://img.shields.io/badge/Status-In%20Progress-blue)
![Power BI](https://img.shields.io/badge/Power%20BI-Project-yellow)
![Version](https://img.shields.io/badge/Version-v0.6.0-success)
![Documentation](https://img.shields.io/badge/Documentation-Available-brightgreen)

---

# 📌 Project Overview

This repository documents the development of a complete Business Intelligence solution for **AtliQ Hardware**, a fictional multinational computer hardware manufacturer.

The project follows a real-world BI workflow—from understanding business requirements and preparing data to building scalable data models, implementing ETL pipelines, writing DAX calculations, and developing interactive dashboards for business stakeholders.

Rather than focusing solely on dashboard creation, this repository also captures the reasoning behind technical decisions, business logic, and implementation practices used throughout the project.

---

# 🎯 Business Objective

AtliQ Hardware operates across **27 countries** through multiple customer channels, including Retailers, Direct Sales, and Distributors.

The objective of this project is to help business stakeholders:

- Monitor company performance
- Analyze Sales and Financial metrics
- Compare Actual Sales against Forecasts
- Identify high-performing and underperforming markets
- Support data-driven business decisions through interactive dashboards

---

# 🏢 Business Model

### Products

- Desktop Computers
- Laptops
- Computer Accessories

### Customer Channels

- Retailers
- Direct (Exclusive Stores & Website)
- Distributors

### Sales Platforms

- Brick & Mortar
- E-Commerce

---

# 🛠 Technology Stack

- Power BI Desktop
- Power Query (M)
- DAX (Data Analysis Expressions)
- MySQL
- Dimensional Data Modeling
- Git & GitHub

---

# 🗂 Dataset Overview

The project consists of a dimensional data model built using Fact and Dimension tables.

## Dimension Tables

- dim_customer
- dim_product
- dim_market

## Fact Tables

- fact_sales_monthly
- fact_forecast_monthly
- gross_price
- manufacturing_cost
- freight_cost
- pre_invoice_deductions
- post_invoice_deductions

---

# 🧱 Data Model

The project follows a **Star Schema** to ensure efficient querying, simplified relationships, and scalable reporting.

Key concepts implemented include:

- Fact & Dimension Tables
- Primary & Foreign Keys
- One-to-Many Relationships
- Custom Fiscal Calendar
- Filter Propagation

---

# 📅 Custom Date Dimension

A custom Date Dimension (`dim_date`) was created to support both Calendar and Fiscal reporting.

Columns include:

- Date
- Day
- Day Name
- Month
- Month Name
- Calendar Year
- Fiscal Year
- Fiscal Quarter
- Fiscal Month
- Quarter

> **Fiscal Year Start:** September 1

---

# 🔄 ETL Pipeline

Data preparation is performed using **Power Query**.

The ETL process includes:

## Data Validation

- Benchmark Validation
- Relationship Validation
- KPI Validation

## Power Query Transformations

- Merge Queries
- Append Queries
- Reference Queries
- Custom Columns
- Dynamic Filtering
- Schema Standardization

---

# 🚀 Dynamic Landing Estimate Table

One of the major ETL implementations in this project is the creation of a dynamic **Landing Estimate** table.

Workflow:

```text
Sales
      │
      ▼
LastSalesMonth (List.Max)

      │
      ▼
Forecast
(Filter records after latest Sales Month)

      │
      ▼
Append

      │
      ▼
fact_landing_estimate
```

### Benefits

- Eliminates hardcoded dates
- Prevents duplicate Actual & Forecast records
- Automatically adapts after each refresh
- Creates a scalable ETL workflow

---

# 💰 Financial Metrics Implemented

Current calculations include:

- Gross Sales Amount
- Pre-Invoice Discount Amount
- Net Invoice Sales

Additional KPIs will be added during later development.

---

# 📚 DAX Concepts Covered

Current DAX concepts implemented include:

- Measures
- Calculated Columns
- Filter Context
- CALCULATE()
- Direct Filters
- Filter Functions
- ALL()
- ALLEXCEPT()

Advanced DAX concepts will be added in future milestones.

---

# 🌟 Project Highlights

This project demonstrates a complete Business Intelligence workflow by combining:

- Business Understanding
- Data Exploration
- Data Validation
- Star Schema Design
- Power Query ETL
- Financial Data Modeling
- DAX Calculations
- Technical Documentation
- Version Tracking

---

# 📈 Project Status

## ✅ Completed

- Business Understanding
- Dataset Exploration
- Data Modeling
- Custom Date Dimension
- Data Validation
- Power Query ETL
- Landing Estimate Table
- Financial Data Preparation
- DAX Fundamentals
- Project Documentation

---

## 🚧 In Progress

- Advanced DAX
- Dashboard Development

---

## ⏳ Upcoming

- Finance Dashboard
- Sales Dashboard
- Executive Dashboard
- Business Insights
- Performance Optimization
- Final Project Release (v1.0.0)

---

# 🗂 Repository Structure

```text
AtliQ-Hardware-BI/
│
├── README.md
├── CHANGELOG.md
│
├── docs/
│   ├── DAX_Notes.md
│   ├── Project_Learnings.md
│   ├── Interview_Questions.md
│   ├── Dataset_Overview.md        (Coming Soon)
│   ├── Data_Model.md              (Coming Soon)
│   └── Business_Insights.md       (Coming Soon)
│
├── pbix/
│
├── assets/
│
└── data/
```

---

# 🗺 Project Roadmap

```text
Business Understanding          ✅

Dataset Exploration             ✅

Data Modeling                   ✅

Data Validation                 ✅

Power Query ETL                 ✅

Financial Metrics               ✅

DAX Fundamentals                ✅

Advanced DAX                    🚧

Dashboard Development           ⏳

Business Insights               ⏳

Performance Optimization        ⏳

Portfolio Release               ⏳
```

---

# 📖 Documentation

This repository contains project-specific documentation that explains both the implementation and the reasoning behind key design decisions.

### Available Documentation

- 📘 DAX Notes
- 📗 Project Learnings
- 📙 Interview Questions
- 📕 Changelog

### Planned Documentation

- Dataset Overview
- Data Model
- Business Insights

---

# 🎯 Learning Outcomes

Through this project, I have gained practical experience with:

- Business Intelligence fundamentals
- Dimensional Data Modeling
- Power Query ETL
- Financial Data Modeling
- DAX Fundamentals
- Data Validation
- Git & GitHub documentation
- Technical documentation for portfolio projects

---

# 👨‍💻 Author

**Saurav Verma**

Aspiring Business Intelligence Analyst

Currently learning:

- Power BI
- SQL
- DAX
- Power Query
- Data Modeling
- Business Intelligence

---

## ⭐ Support

If you found this project useful or interesting, consider giving the repository a **Star**.
