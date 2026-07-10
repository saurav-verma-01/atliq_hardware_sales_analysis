# 📊 AtliQ Hardware Business Intelligence Project

> **A complete end-to-end Business Intelligence project built using Power BI, Power Query, DAX, SQL, and dimensional data modeling.**

![Status](https://img.shields.io/badge/Status-In%20Progress-blue)
![Power BI](https://img.shields.io/badge/Power%20BI-Project-yellow)
![Version](https://img.shields.io/badge/Version-v1.0-success)
![Learning](https://img.shields.io/badge/Learning-Business%20Intelligence-orange)

---

# 📌 Project Overview

This project is based on a fictional multinational computer hardware manufacturer **AtliQ Hardware**.

The objective is to transform raw transactional data into business-ready information and develop interactive Power BI dashboards that help stakeholders make informed business decisions.

The project follows an industry-oriented Business Intelligence workflow including:

- Business Understanding
- Data Exploration
- Data Validation
- Data Modeling
- Power Query ETL
- DAX Calculations
- Dashboard Development
- Business Storytelling

---

# 🎯 Business Objective

AtliQ Hardware operates across **27 countries** and sells products through multiple customer channels including Retailers, Direct Sales, and Distributors.

The company wants to:

- Monitor financial performance
- Track Net Sales and Gross Margin
- Compare actual sales with forecasts
- Identify underperforming markets
- Improve business decision-making through interactive dashboards

---

# 🏢 Business Model

AtliQ Hardware manufactures:

- Desktop Computers
- Laptops
- Computer Accessories

Customer Channels:

- Retailers
- Direct (AtliQ Exclusive Stores & Website)
- Distributors

Platforms:

- Brick & Mortar
- E-Commerce

---

# 🗂 Dataset Overview

### Dimension Tables

- dim_customer
- dim_product
- dim_market

### Fact Tables

- fact_sales_monthly
- fact_forecast_monthly
- gross_price
- manufacturing_cost
- freight_cost
- pre_invoice_deductions
- post_invoice_deductions

---

# 🧱 Data Model

The project follows a **Star Schema**.

Dimension tables provide descriptive information while fact tables contain business transactions and measurable metrics.

---

# 📅 Date Dimension

A custom Date Dimension table was created containing:

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

The fiscal year begins on **1 September**.

---

# 🔄 ETL Pipeline

The data preparation process includes:

### Data Validation

- Benchmark validation
- Relationship validation
- KPI validation

### Power Query

- Reference Queries
- Merge Queries
- Append Queries
- Dynamic Filtering
- Custom Columns
- Schema Standardization

---

# 🚀 Dynamic ETL Implementation

One of the key ETL improvements implemented in this project is the creation of a dynamic **Landing Estimate** table.

Workflow:

```text
Sales
      ↓
LastSalesMonth (List.Max)

      ↓

Forecast
(Filter records after latest sales month)

      ↓

Append

      ↓

fact_landing_estimate
```

This approach:

- Eliminates hardcoded dates
- Prevents overlapping Actual and Forecast records
- Automatically adapts to new data after refresh
- Supports scalable ETL design

---

# 💰 Financial Metrics Built

Current financial calculations include:

- Gross Sales Amount
- Pre-Invoice Discount Amount
- Net Invoice Sales

Additional KPIs will be added during future development.

---

# 🛠 Technologies Used

- Power BI Desktop
- Power Query (M)
- DAX
- MySQL
- Data Modeling
- Git & GitHub

---

# 📚 Key Business Concepts Learned

- Fact vs Dimension Tables
- Star Schema
- Primary & Foreign Keys
- Fiscal Calendar
- Dynamic ETL
- Reference vs Duplicate Queries
- Merge vs Append
- Data Validation
- Business Keys
- Financial Data Modeling

---

# 📈 Current Project Status

## ✅ Completed

- Business Understanding
- Dataset Exploration
- Data Modeling
- Date Dimension
- Data Validation
- Power Query Foundations
- Dynamic ETL Pipeline
- Landing Estimate Table
- Financial Data Preparation

## 🚧 In Progress

- Power Query Transformations
- Financial View

## ⏳ Upcoming

- DAX
- Measures
- Finance Dashboard
- Sales Dashboard
- Executive Dashboard
- Business Storytelling
- Performance Optimization

---

# 📂 Repository Structure

```
AtliQ-Hardware-BI/
│
├── README.md
│
├── docs/
│   ├── The-BI-Playbook.md
│   ├── Communication-Notebook.md
│   ├── Interview-Insights.md
│   ├── BI-Principles.md
│   ├── Business-Glossary.md
│   ├── PowerQuery-M-CheatSheet.md
│   ├── ETL-Architecture.md
│   └── Learning-Journal.md
│
├── pbix/
│
├── assets/
│   ├── mockups/
│   ├── screenshots/
│   └── linkedin/
│
└── data/
```

---

# 🧠 My Learning Philosophy

This repository is more than a Power BI project.

It documents my journey from beginner to Business Intelligence Analyst by focusing on:

- Understanding business problems before building dashboards.
- Learning the reasoning behind every technical decision.
- Building production-style ETL pipelines instead of simply following tutorials.
- Improving communication alongside technical skills.
- Documenting concepts for long-term retention and interview preparation.

---

# 🚀 Project Roadmap

```text
Business Understanding
        ✅

Data Exploration
        ✅

Data Validation
        ✅

Power Query ETL
        🚧

Financial Metrics
        🚧

DAX
        ⏳

Dashboard Development
        ⏳

Business Storytelling
        ⏳

Portfolio Ready
        ⏳
```

---

# 📖 Documentation

This repository contains a growing collection of structured documentation including:

- The BI Playbook
- Communication Notebook
- Interview Preparation Notes
- ETL Architecture
- Power Query M Cheat Sheet
- Business Glossary
- BI Principles

These documents capture not only _how_ each solution was implemented, but also _why_ each business and technical decision was made.

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

## ⭐ If you found this project interesting, consider giving it a Star.
