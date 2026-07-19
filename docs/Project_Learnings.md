# Project Learnings

> This document captures the key technical concepts, business understanding, challenges, and lessons learned while building the **AtliQ Hardware Sales Analysis** project as part of the Codebasics Power BI Bootcamp.
>
> Rather than documenting every lecture, this file highlights the knowledge and practical experience gained throughout the project.

---

# Learning Timeline

| Module   | Topic                             | Status       |
| -------- | --------------------------------- | ------------ |
| Module 1 | Business Understanding            | ✅ Completed |
| Module 2 | Data Collection & Exploration     | ✅ Completed |
| Module 3 | Data Modeling                     | ✅ Completed |
| Module 4 | Basic Dashboard & Data Validation | ✅ Completed |
| Module 5 | Power Query (Data Transformation) | ✅ Completed |
| Module 6 | DAX Fundamentals                  | ✅ Completed |

---

# Module 1 — Business Understanding

## What I Learned

- Importance of understanding the business before building reports.
- Understanding the AtliQ Hardware business model.
- Different customer segments and sales channels.
- Importance of asking business questions before creating dashboards.

## Business Knowledge Gained

Customer Segments

- Retail
- Direct
- Distributor

Sales Channels

- Brick & Mortar
- E-Commerce

## Key Takeaways

A dashboard is valuable only when it answers business questions, not when it contains many visuals.

---

# Module 2 — Dataset Understanding

## What I Learned

- Difference between Fact Tables and Dimension Tables.
- Importance of table relationships.
- Understanding data granularity (Grain).
- Structure of a Star Schema.

## Dataset Overview

Dimension Tables

- dim_customer
- dim_product
- dim_market

Fact Tables

- fact_sales_monthly
- fact_forecast_monthly
- freight_cost
- gross_price
- manufacturing_cost
- post_invoice_deductions
- pre_invoice_deductions

## Key Takeaways

A well-designed data model simplifies report development and improves performance.

---

# Module 3 — Data Modeling

## What I Learned

- Creating relationships between tables.
- Understanding one-to-many relationships.
- Importance of clean dimension tables.
- Building a proper Star Schema.

## Challenges

Initially focused more on connecting tables than understanding why relationships mattered.

## Key Takeaways

Power BI relationships determine how filters propagate through the model.

Without proper relationships, DAX calculations become unreliable.

---

# Module 4 — Data Validation

## What I Learned

- Validating imported data before building reports.
- Comparing Power BI results with benchmark values.
- Importance of verifying calculations before creating dashboards.

## Challenges

Observed small decimal differences when comparing benchmark values.

## Resolution

Confirmed that the differences were due to decimal precision rather than incorrect calculations.

## Key Takeaways

Never assume imported data is correct.
Always validate important metrics.

---

# Module 5 — Power Query (Data Transformation)

## What I Learned

- Cleaning and transforming raw data.
- Creating reusable queries.
- Using Merge Queries.
- Using Append Queries.
- Creating Reference Queries.
- Building an ETL workflow inside Power Query.

## Project Work

Created a Landing Estimate table by combining:

- Sales Data
- Forecast Data

Additional transformations:

- Added Fiscal Year
- Merged Gross Price
- Calculated Gross Sales Amount
- Added Pre-Invoice Deductions
- Calculated Net Invoice Sales

## Key Takeaways

Power Query should perform data preparation.

Avoid pushing data cleaning logic into DAX whenever possible.

---

# Module 6 — DAX Fundamentals

## What I Learned

### Measures

- Dynamic calculations evaluated at query time.
- Respond automatically to Filter Context.

### Calculated Columns

- Row-level calculations stored in the model.
- Best used for creating new attributes.

### Filter

A filter is simply a condition that determines which rows participate in a calculation.

### Filter Context

The same DAX measure can return different results because the active Filter Context changes.

### CALCULATE()

Initially, I believed CALCULATE ignored Filter Context.

After studying the concept, I understood that CALCULATE starts with the current Filter Context and then modifies it before evaluating an expression.

### Direct Filters

Learned how to explicitly apply filters inside CALCULATE.

### ALL()

Used to remove filters from a table or column.

Useful for percentage contribution calculations.

### ALLEXCEPT()

Removes all filters except the specified columns.

Useful when preserving a specific business grouping.

## Biggest Learning

Writing DAX is less about memorizing functions and more about understanding **which rows should participate in the calculation**.

---

# Challenges Faced During the Project

## Understanding DAX Evaluation Context

Initially found Filter Context difficult to understand.

The concept became much clearer after relating it to business scenarios instead of memorizing syntax.

---

## Row Context

Introduced to Row Context and RELATEDTABLE() during the DAX module.

Instead of forcing myself to memorize these advanced concepts, I decided to continue with the project and revisit them after gaining more experience with Data Modeling and dashboard development.

This decision helped maintain learning momentum while avoiding unnecessary confusion.

---

# Overall Learnings

Throughout this project I learned that successful BI development involves much more than writing DAX formulas.

A complete Business Intelligence solution requires:

- Understanding business requirements.
- Designing an efficient data model.
- Preparing clean data through ETL.
- Writing reliable DAX calculations.
- Validating results.
- Communicating insights effectively through dashboards.

---

# Next Learning Goals

- Dashboard Design
- Business Storytelling
- Performance Optimization
- Advanced DAX
- Row Context
- Context Transition
- Time Intelligence
- Advanced Data Modeling
