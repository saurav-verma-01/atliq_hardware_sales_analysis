# DAX Notes

Project: AtliQ Hardware Sales Analysis

This document captures the DAX concepts, functions, and business logic learned while building this project. It is intended to serve as project documentation rather than a complete DAX reference.

---

## Topics Covered

- Measures
- Calculated Columns
- Filter
- Filter Context
- CALCULATE()
- Direct Filters
- Filter Functions
- ALL()
- ALLEXCEPT()

---

# Measures

## What is a Measure?

A Measure is a dynamic calculation evaluated at query time based on the current Filter Context.

Measures do not store values in the data model. Instead, Power BI calculates the result whenever a visual requests it.

### Example

```DAX
Total Sales =
SUM(fact_sales_monthly[Net_Invoice_Sales])
```

### Key Learning

The same measure can return different results depending on the active Filter Context.

Examples:

- Total Company Sales
- India Sales
- Laptop Sales
- FY2022 Sales

---

# Calculated Columns

## What is a Calculated Column?

A Calculated Column performs a row-by-row calculation during data refresh and stores the result in the model.

### When to Use

- Creating categories
- Generating new attributes
- Creating sort columns
- Building keys

### Difference from Measures

| Measure                     | Calculated Column         |
| --------------------------- | ------------------------- |
| Dynamic                     | Static                    |
| Calculated at query time    | Calculated during refresh |
| Doesn't increase model size | Increases model size      |

---

# Filter

A Filter is a condition that determines which rows participate in a calculation.

Example:

- Market = India
- Product = Laptop
- Fiscal Year = 2022

---

# Filter Context

## Definition

Filter Context is the collection of all active filters applied while evaluating a DAX expression.

Sources of Filter Context:

- Slicers
- Visuals
- Page Filters
- Report Filters
- Relationships

### Key Learning

The calculation usually remains the same.

Only the rows participating in the calculation change.

---

# CALCULATE()

## Definition

`CALCULATE()` evaluates an expression after modifying the existing Filter Context.

This is one of the most important DAX functions because it allows us to:

- Add filters
- Replace filters
- Remove filters

### Syntax

```DAX
CALCULATE(
    Expression,
    Filter1,
    Filter2
)
```

### Key Learning

I initially thought CALCULATE ignored Filter Context.

After studying it, I understood that CALCULATE **starts with the current Filter Context and then modifies it** before evaluating the expression.

---

# Direct Filters

Direct Filters explicitly specify filter conditions inside `CALCULATE()`.

Example:

```DAX
CALCULATE(
    [Total Sales],
    dim_market[market] = "India"
)
```

---

# Filter Functions

Filter Functions return tables that help modify the Filter Context.

Functions covered so far:

- ALL()
- ALLEXCEPT()

---

# ALL()

Removes filters from the specified table or column.

Examples:

- ALL(Table)
- ALL(Column)

### Common Use Case

Calculating percentage contribution against the company total.

---

# ALLEXCEPT()

Removes all filters from a table except the specified columns.

### Common Use Case

Keeping Customer while ignoring other customer attributes.

---

# Important Learnings

- Think about the business requirement before writing DAX.
- DAX is primarily about controlling which rows participate in a calculation.
- Measures are generally preferred over Calculated Columns.
- CALCULATE modifies the existing Filter Context.
- ALL removes filters.
- ALLEXCEPT preserves selected filters while removing the rest.

---

# Topics Not Yet Covered

- Row Context
- Context Transition
- RELATED()
- RELATEDTABLE()
- FILTER()
- Variables (VAR)
- Iterators (SUMX, AVERAGEX, etc.)
- Time Intelligence
