# Interview Questions

> This document contains interview questions and answers based on the concepts learned while building the **AtliQ Hardware Sales Analysis** project.
>
> The questions are grouped by topic and focus only on concepts covered during the project.

---

# Table of Contents

1. Business Understanding
2. Data Modeling
3. Power Query
4. DAX Fundamentals
5. Project-Based Questions

---

# 1. Business Understanding

## Q1. What is Business Intelligence?

### Answer

Business Intelligence (BI) is the process of collecting, transforming, analyzing, and visualizing data to support better business decision-making.

The goal of BI is to convert raw data into meaningful insights that help organizations monitor performance and make informed decisions.

---

## Q2. Why is business understanding important before creating a dashboard?

### Answer

A dashboard should answer business questions rather than simply display charts.

Understanding the business helps identify:

- Important KPIs
- Stakeholder requirements
- Business goals
- Decision-making needs

Without business understanding, even a visually attractive dashboard may provide little value.

---

## Q3. Explain the AtliQ Hardware business model.

### Answer

AtliQ Hardware is a computer hardware manufacturer that sells products across multiple countries through different customer segments.

Customer Segments

- Retail
- Direct
- Distributor

Sales Channels

- Brick & Mortar
- E-Commerce

---

# 2. Data Modeling

## Q4. What is a Fact Table?

### Answer

A Fact Table stores measurable business data such as sales, quantity, or costs.

Fact tables usually contain:

- Numeric values
- Foreign keys
- Large number of records

Examples from this project:

- fact_sales_monthly
- fact_forecast_monthly

---

## Q5. What is a Dimension Table?

### Answer

A Dimension Table stores descriptive information that provides context to fact data.

Examples include:

- Customer
- Product
- Market

Examples from this project:

- dim_customer
- dim_product
- dim_market

---

## Q6. What is a Star Schema?

### Answer

A Star Schema is a data modeling technique where a central Fact Table connects to multiple Dimension Tables.

Benefits include:

- Simpler relationships
- Better performance
- Easier report development

---

## Q7. Why are relationships important in Power BI?

### Answer

Relationships allow filters to propagate between tables.

Without proper relationships:

- DAX calculations may return incorrect results.
- Visuals may not interact correctly.
- Data analysis becomes unreliable.

---

# 3. Power Query

## Q8. What is the difference between Power Query and DAX?

### Answer

Power Query is used for extracting, cleaning, and transforming data before it is loaded into the data model.

DAX is used after the data has been loaded to perform business calculations and analysis.

Power Query focuses on ETL.

DAX focuses on analytics.

---

## Q9. What is ETL?

### Answer

ETL stands for:

- Extract
- Transform
- Load

It is the process of collecting raw data, transforming it into a usable format, and loading it into the data model.

---

## Q10. What is the difference between Merge and Append?

### Answer

Merge combines tables horizontally by adding columns based on matching keys.

Append combines tables vertically by adding rows from one table to another.

---

## Q11. What is a Reference Query?

### Answer

A Reference Query creates a new query based on an existing query without duplicating the original transformations.

It helps reuse cleaned datasets while keeping transformations maintainable.

---

## Q12. Why should data transformations be performed in Power Query instead of DAX?

### Answer

Power Query performs transformations during data refresh, reducing the amount of work required during report interaction.

Keeping ETL logic in Power Query results in cleaner data models and better report performance.

---

# 4. DAX Fundamentals

## Q13. What is DAX?

### Answer

DAX (Data Analysis Expressions) is the formula language used in Power BI to create calculations such as Measures, Calculated Columns, and calculated tables.

---

## Q14. What is a Measure?

### Answer

A Measure is a dynamic calculation evaluated at query time based on the current Filter Context.

Measures do not store values in the model.

---

## Q15. What is a Calculated Column?

### Answer

A Calculated Column performs a row-by-row calculation during data refresh and stores the result in the data model.

---

## Q16. Difference between Measures and Calculated Columns.

| Measure                              | Calculated Column          |
| ------------------------------------ | -------------------------- |
| Dynamic                              | Static                     |
| Calculated during report interaction | Calculated during refresh  |
| Doesn't consume storage for results  | Stores values in the model |

---

## Q17. What is a Filter?

### Answer

A Filter is a condition that determines which rows participate in a calculation.

Examples include filtering by Market, Product, or Fiscal Year.

---

## Q18. What is Filter Context?

### Answer

Filter Context is the collection of all active filters applied while evaluating a DAX expression.

These filters can originate from slicers, visuals, page filters, report filters, or model relationships.

---

## Q19. What is CALCULATE()?

### Answer

CALCULATE() evaluates an expression after modifying the existing Filter Context.

It is used to add, replace, or remove filters before performing a calculation.

---

## Q20. Why is CALCULATE() considered the most important DAX function?

### Answer

Many business calculations require changing the default Filter Context.

CALCULATE provides the ability to control which rows participate in a calculation, making it fundamental to writing dynamic business measures.

---

## Q21. What are Direct Filters?

### Answer

Direct Filters explicitly define filter conditions inside CALCULATE().

Example:

```DAX
CALCULATE(
    [Total Sales],
    dim_market[market] = "India"
)
```

---

## Q22. What are Filter Functions?

### Answer

Filter Functions return tables that modify the Filter Context.

Examples covered so far:

- ALL()
- ALLEXCEPT()

---

## Q23. What is ALL()?

### Answer

ALL() removes filters from a specified table or column.

It is commonly used for grand totals and percentage contribution calculations.

---

## Q24. What is ALLEXCEPT()?

### Answer

ALLEXCEPT() removes all filters from a table except the specified columns.

It is useful when a calculation should preserve one grouping while ignoring the remaining filters from the same table.

---

# 5. Project-Based Questions

## Q25. Why did you create the Landing Estimate table?

### Answer

The Landing Estimate table was created by appending Sales and Forecast data into a single table to provide a continuous dataset for reporting and analysis.

---

## Q26. How did you calculate Gross Sales Amount?

### Answer

Gross Sales Amount was calculated by merging Gross Price with the Landing Estimate table and multiplying Gross Price by Quantity.

---

## Q27. How was Net Invoice Sales calculated?

### Answer

After merging Pre-Invoice Deduction percentages into the Landing Estimate table, Net Invoice Sales was calculated by subtracting the applicable discount from the Gross Sales Amount.

---

## Q28. How did you validate the imported data?

### Answer

The calculated values in Power BI were compared against benchmark values provided in the course.

Minor decimal differences were identified as precision differences rather than calculation errors.

---

## Q29. What was the most challenging concept during this project?

### Answer

Understanding Filter Context and CALCULATE().

Initially, I focused on memorizing DAX syntax, but later realized that DAX is primarily about controlling which rows participate in a calculation through the Filter Context.

---

## Q30. What is your biggest learning from this project so far?

### Answer

Building a Business Intelligence solution involves much more than creating dashboards.

It requires understanding business requirements, designing a clean data model, preparing data through ETL, writing efficient DAX calculations, validating results, and communicating insights effectively.
