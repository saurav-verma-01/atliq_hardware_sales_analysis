# Changelog

All notable changes to the **AtliQ Hardware Sales Analysis** project are documented in this file.

This project follows a milestone-based changelog to track significant development progress, technical improvements, documentation updates, and key learnings throughout the project lifecycle.

---

## [Unreleased]

### Planned

- Dashboard Development
- Executive Summary Dashboard
- Finance Analytics Dashboard
- Sales Analytics Dashboard
- Business Insights Documentation
- Performance Optimization
- Advanced DAX
- Final Project Release (v1.0.0)

---

# [v0.6.0] - DAX Fundamentals

## Added

### Project Documentation

- Created `docs/DAX_Notes.md`
- Created `docs/Project_Learnings.md`
- Created `docs/Interview_Questions.md`
- Standardized project documentation structure

### DAX Concepts Covered

- Introduction to DAX
- Measures
- Calculated Columns
- Filter
- Filter Context
- CALCULATE()
- Direct Filters
- Filter Functions
- ALL()
- ALLEXCEPT()

## Learned

- DAX is primarily about controlling which rows participate in a calculation.
- Measures are dynamic calculations evaluated at query time.
- Calculated Columns are computed during data refresh and stored in the model.
- Filter Context determines how DAX expressions are evaluated.
- `CALCULATE()` starts with the existing Filter Context and then modifies it before evaluating an expression.
- `ALL()` removes filters from a specified table or column.
- `ALLEXCEPT()` preserves selected filters while removing the remaining filters from the same table.

---

# [v0.5.0] - Power Query & ETL

## Added

- Landing Estimate table by appending Sales and Forecast datasets.
- Fiscal Year column.
- Gross Sales Amount calculation.
- Net Invoice Sales calculation.

## Power Query Operations

- Merge Queries
- Append Queries
- Reference Queries
- Data Cleaning
- Data Transformation
- ETL Workflow

## Learned

- Power Query should be responsible for data preparation.
- Reusable queries simplify ETL workflows.
- Data transformations should be completed before loading data into the model whenever possible.
- Keeping transformation logic inside Power Query results in cleaner and more maintainable DAX.

---

# [v0.4.0] - Data Validation

## Added

- Data validation workflow.
- Benchmark comparison.
- Relationship verification.
- Initial dashboard validation.

## Learned

- Imported data should always be validated before report development.
- Minor decimal differences may occur because of precision and rounding.
- Validation improves confidence in the accuracy of business reports.

---

# [v0.3.0] - Data Modeling

## Added

- Star Schema implementation.
- Relationships between Fact and Dimension tables.
- Custom Fiscal Date Table (`dim_date`).
- Fiscal Year, Fiscal Quarter, and Fiscal Month logic.

## Learned

- Data modeling directly affects report performance.
- Proper relationships are essential for correct filter propagation.
- A clean Star Schema simplifies DAX development.
- Understanding data granularity is critical before creating relationships.

---

# [v0.2.0] - Dataset Understanding

## Added

### Dataset Exploration

- Fact Table analysis.
- Dimension Table analysis.
- Data granularity assessment.
- Business terminology documentation.

### Business Understanding

- Customer Segments
- Sales Channels
- Revenue Metrics
- Pricing Structure

## Learned

- Business understanding should always come before report development.
- Fact Tables store measurable business events.
- Dimension Tables provide descriptive business context.
- Understanding the dataset is the foundation of successful BI projects.

---

# [v0.1.0] - Project Initialization

## Added

- GitHub repository created.
- AtliQ Hardware dataset imported.
- Initial Power BI project setup.
- Repository folder structure.
- Project documentation framework.

## Learned

- Establishing a structured project from the beginning improves maintainability.
- Well-organized documentation makes the project easier to understand and extend.

---

## Version Roadmap

| Version | Milestone                        | Status       |
| ------- | -------------------------------- | ------------ |
| v0.1.0  | Project Initialization           | ✅ Completed |
| v0.2.0  | Business & Dataset Understanding | ✅ Completed |
| v0.3.0  | Data Modeling                    | ✅ Completed |
| v0.4.0  | Data Validation                  | ✅ Completed |
| v0.5.0  | Power Query & ETL                | ✅ Completed |
| v0.6.0  | DAX Fundamentals                 | ✅ Completed |
| v0.7.0  | Advanced DAX                     | ⏳ Planned   |
| v0.8.0  | Dashboard Development            | ⏳ Planned   |
| v0.9.0  | Business Insights & Optimization | ⏳ Planned   |
| v1.0.0  | Final Project Release            | ⏳ Planned   |
