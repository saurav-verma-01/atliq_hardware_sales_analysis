# 📖 BI Analyst Notebook

> Personal knowledge base created while building the **AtliQ Hardware Business Intelligence Project**.

**Purpose**

This notebook captures only the most important concepts, business reasoning, and interview-ready notes. It is intentionally concise and will grow incrementally throughout the project.

---

# Module 1 — Business Understanding

## Core Principle

> Business Intelligence is about solving business problems, not building dashboards.

A dashboard is only valuable if it helps stakeholders make better business decisions.

---

## Understanding AtliQ Hardware

AtliQ Hardware is a multinational computer hardware manufacturer operating across multiple countries.

### Customer Channels

**Retailers**

- Brick & Mortar
- E-commerce

**Direct**

- AtliQ Exclusive Stores
- Official Website
- Mobile App

**Distributors**

- Large distributors supplying smaller retailers.

---

## Business Objective

The project focuses on answering questions such as:

- Which markets perform best?
- Which customer channels are most profitable?
- Which products contribute the highest Gross Margin?
- How accurate are sales forecasts?
- Where should the business invest next?

---

# Module 2 — Data Modeling Fundamentals

## Dimension Tables

Dimension tables describe business entities.

Examples:

- Customer
- Product
- Market
- Date

Dimension tables answer:

- Who?
- What?
- Where?
- When?

---

## Fact Tables

Fact tables record measurable business events.

Examples:

- Sales
- Forecast

Fact tables answer:

- How much?
- How many?
- When?

---

## Golden Rule

> Fact Tables record business events.

> Dimension Tables describe those events.

---

## Why Separate Tables?

Separate tables reduce redundancy, improve maintainability, and allow different business processes (sales, pricing, manufacturing, logistics) to be modeled independently while remaining connected through relationships.

---

## Primary Keys

Relationships should use stable identifiers.

Example:

Use `customer_code`

Avoid:

Customer Name

Reason:

Business names may change, while keys should remain stable.

---

# Module 3 — Business KPIs

## Gross Price

Product list price before any discounts.

---

## Pre-Invoice Deductions

Discounts applied before invoice generation.

Examples:

- Contract Discount
- Volume Discount
- Seasonal Discount

---

## Post-Invoice Deductions

Adjustments applied after invoicing.

Examples:

- Promotional Support
- Placement Fees
- Performance Rebates

---

## Net Sales

Revenue retained after all applicable deductions.

---

## Cost of Goods Sold (COGS)

Direct costs associated with manufacturing and delivering products.

Examples:

- Manufacturing
- Packaging
- Freight
- Logistics

Does not include indirect business expenses such as HR, administration, or taxes.

---

## Gross Margin

**Formula**

Gross Margin = Net Sales − COGS

Gross Margin measures profitability after direct costs.

---

# Module 4 — Date Dimension

## Purpose

The Date Dimension does not store transactions.

It enriches every date with descriptive calendar attributes that support consistent business analysis.

---

## Why a Separate Date Dimension?

Enables:

- Time Intelligence
- Fiscal Reporting
- Calendar Reporting
- Consistent Filtering
- Trend Analysis

---

## Current Date Columns

### Calendar

- Date
- Day
- Day Name
- Month Number
- Month Name
- Quarter
- Calendar Year

### Fiscal

- Fiscal Month
- Fiscal Quarter
- Fiscal Year

---

## Fiscal Calendar

AtliQ Fiscal Year starts on **1 September**.

### Fiscal Quarter Mapping

| Quarter | Months               |
| ------- | -------------------- |
| FQ1     | September – November |
| FQ2     | December – February  |
| FQ3     | March – May          |
| FQ4     | June – August        |

---

## Important Learning

Business Rule → Data Model → DAX → Dashboard

Never begin with DAX.

Always understand the business rule first.

---

# Analyst Mindset

Whenever learning a new concept, ask:

1. What business problem does this solve?
2. Why is it implemented this way?
3. How would I explain it in an interview?

---

# Interview Notes

Be able to explain:

- Fact vs Dimension Tables
- Why Date Dimension exists
- Calendar Year vs Fiscal Year
- Why Month Number is required
- Why relationships use keys instead of names
- Gross Price vs Net Sales
- Gross Margin vs Revenue

---

# Personal Takeaways

- Think in terms of business processes, not tables.
- Every column should have a business purpose.
- Build trust in data before building dashboards.
- Understand the logic before writing DAX.
- Great dashboards answer questions—they don't just display charts.
