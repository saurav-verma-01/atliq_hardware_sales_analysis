# 📊 AtliQ Hardware Business Intelligence Project

> An end-to-end Business Intelligence project built using **Power BI**, following industry-standard BI practices including data modeling, business understanding, KPI analysis, and dashboard development.

---

# 🚀 Project Status

**Current Phase:** Foundation & Data Modeling (Version 1.0)

Completed:

- ✅ Business Understanding
- ✅ Data Exploration
- ✅ Data Model Understanding
- ✅ Date Dimension Design
- ✅ Fiscal Calendar Implementation

Upcoming:

- ⏳ Data Validation
- ⏳ Data Cleaning (Power Query)
- ⏳ Data Modeling & Relationships
- ⏳ DAX Measures
- ⏳ Executive Dashboard Development
- ⏳ Business Insights & Recommendations

---

# 🎯 Project Objective

AtliQ Hardware is a multinational computer hardware manufacturer operating across multiple countries and sales channels.

The objective of this project is to transform raw business data into actionable insights that help stakeholders answer strategic business questions such as:

- Which markets generate the highest revenue?
- Which customer channels are most profitable?
- How does Gross Margin vary across products and regions?
- How accurate are sales forecasts?
- Which business areas require operational improvement?

---

# 🏢 Business Overview

### Customer Channels

- Retailers
  - Brick & Mortar
  - E-commerce

- Direct
  - AtliQ Exclusive Stores
  - Official Website
  - Mobile App

- Distributors

---

# 🗂 Dataset Overview

### Dimension Tables

- dim_customer
- dim_market
- dim_product
- dim_date _(Created during this project)_

### Fact Tables

- fact_sales_monthly
- fact_forecast_monthly
- gross_price
- manufacturing_cost
- freight_cost
- pre_invoice_deductions
- post_invoice_deductions

---

# 📅 Date Dimension

A custom Date Dimension was designed instead of relying solely on transaction dates.

### Implemented Columns

- Date
- Day
- Day Name
- Month Number
- Month Name
- Quarter
- Calendar Year
- Fiscal Month
- Fiscal Quarter
- Fiscal Year

### Fiscal Calendar

AtliQ follows a fiscal calendar beginning on **1 September**.

Fiscal Quarter Mapping:

| Fiscal Quarter | Months               |
| -------------- | -------------------- |
| FQ1            | September – November |
| FQ2            | December – February  |
| FQ3            | March – May          |
| FQ4            | June – August        |

---

# 🧠 Key Learning Outcomes (Version 1.0)

### Business Intelligence Mindset

- Business Intelligence is about solving business problems, not building charts.
- Every dashboard should answer a business question.
- Business understanding comes before visualization.

### Data Modeling

- Fact Tables record business events.
- Dimension Tables describe business entities.
- Relationships should be built using stable keys rather than descriptive fields.

### Financial Concepts

- Gross Price
- Pre-Invoice Deductions
- Post-Invoice Deductions
- Net Sales
- Cost of Goods Sold (COGS)
- Gross Margin

### Date Dimension

Learned why enterprise BI models use a dedicated Date Dimension to support:

- Calendar reporting
- Fiscal reporting
- Time Intelligence
- Consistent filtering
- Business-friendly analysis

---

# 🛠 Tools & Technologies

- Power BI Desktop
- DAX
- MySQL
- Power Query _(Upcoming)_
- GitHub

---

# 📌 Repository Roadmap

```
AtliQ-Hardware-BI-Project
│
├── README.md
├── BI_Analyst_Notebook.md
├── Dashboard.pbix
├── Dataset/
├── Images/
├── DAX/
└── Documentation/
```

---

# 📈 Current Progress

| Module                 | Status |
| ---------------------- | ------ |
| Business Understanding | ✅     |
| Data Collection        | ✅     |
| Data Exploration       | ✅     |
| Date Dimension         | ✅     |
| Data Validation        | ⏳     |
| Data Cleaning          | ⏳     |
| Data Modeling          | ⏳     |
| DAX Measures           | ⏳     |
| Dashboard Design       | ⏳     |
| Business Insights      | ⏳     |

---

# 🎯 Project Vision

The goal of this project is not only to build an interactive Power BI dashboard but also to develop a strong Business Intelligence mindset by understanding the business context, designing an efficient data model, validating data quality, and communicating insights that support better business decisions.

---

## 👨‍💻 Author

**Saurav Verma**

This repository documents my journey of learning and applying Business Intelligence concepts through a real-world Power BI case study based on AtliQ Hardware.
