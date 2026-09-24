# College Placement Analytics – Power BI

A Power BI dashboard for analyzing historical college placement data across academic years, companies, students, and CTC ranges.

## Project Overview

This project transforms historical placement records into a structured Power BI data model and an interactive one-page dashboard.

The dashboard provides insights into:
- Total students placed
- Placement records
- Recruiting companies
- CTC distribution
- Year-wise placement trends
- Company-wise student recruitment
- Average and highest CTC
- Placement performance across CTC categories

The report covers the academic years **2023–24, 2024–25, and 2025–26**.

## Objectives

1. Clean and prepare historical placement data.
2. Build a reliable Power BI data model.
3. Create reusable DAX measures for key metrics.
4. Develop interactive visuals for placement analysis.
5. Present the results through a professional single-page dashboard.
6. Maintain the project in GitHub using version control.

## Tools & Technologies

- **Power BI Desktop** – data modeling, DAX, and dashboard development
- **Microsoft Excel** – source data preparation
- **DAX** – calculated measures and KPI analysis
- **Git & GitHub** – version control and project management

## Dataset

The consolidated dataset contains historical placement information including:

- Academic Year
- Company
- CTC
- CTC Category
- Number of Students

The final dataset contains **192 placement records** and **2,011 students** across three academic years.

### CTC Categories

- Below 5 LPA
- 5–10 LPA
- Above 10 LPA

## Project Workflow

### 1. Data Collection

Historical placement records were consolidated into a single Excel-based dataset.

### 2. Data Cleaning & Preparation

The source data was reviewed and transformed before importing it into Power BI.

Key preparation tasks included:

- Standardizing academic year values
- Cleaning and standardizing company names
- Removing duplicate company entries
- Separating CTC ranges into minimum and maximum LPA fields
- Creating a fixed CTC value where appropriate
- Categorizing CTC into three placement bands
- Identifying missing or questionable records through data-quality flags

### 3. Power BI Data Model

The project uses a simple star-style model consisting of:

- **FactPlacement** – placement-level data
- **DimAcademicYear** – academic year dimension
- **DimCTCCategory** – CTC category dimension
- **DimCompany** – company dimension
- **DimDataQuality** – data-quality reference

Relationships were created between the fact table and the main dimensions using one-to-many relationships with single-direction filtering.

### 4. DAX Measures

Measures were created for the main KPIs and analytical calculations, including:

- Total Students
- Placement Records
- Recruiting Companies
- Highest CTC
- Average CTC
- Students Below 5 LPA
- Students 5–10 LPA
- Students Above 10 LPA
- Below 5 LPA %
- 5–10 LPA %
- Above 10 LPA %
- Average Students per Record

Formatted display measures were also used where exact student counts were required instead of abbreviated values such as `2K`.

### 5. Dashboard Development

The final dashboard includes:

- KPI cards
- Academic Year slicer
- Year-wise student trend
- CTC category analysis
- CTC category by academic year
- Top 10 recruiting companies
- All companies with student recruitment counts
- Average CTC by academic year
- Placement records by academic year
- Student distribution by CTC category
- Placement records by CTC category
- CTC category trend using a ribbon chart
- Total Students and Average CTC comparison
- Average CTC vs Highest CTC gauge

### 6. Dashboard Design

The report was designed as a single-page **16:9** dashboard with:

- Clean professional layout
- Consistent visual spacing
- KPI-focused top section
- Interactive filtering
- Clear chart titles
- Subtle background and borders
- Minimal visual decoration

### 7. Validation

Before finalizing the report, the dashboard was checked for:

- Correct student totals
- Correct CTC category calculations
- Active data relationships
- Company-name consistency
- Proper academic-year filtering
- Correct visual aggregation
- Readable labels and KPI values

## Key Dashboard Metrics

Across the complete dataset:

| Metric | Value |
|---|---:|
| Students | 2,011 |
| Placement Records | 192 |
| Students Below 5 LPA | 1,632 |
| Students 5–10 LPA | 333 |
| Students Above 10 LPA | 46 |
| Academic Years | 3 |

## Project Structure

```text
Placement-Analysis-PowerBI/
│
├── Placement_Analysis_PowerBI.pbix
├── Placement_Analytics_PowerBI_Ready.xlsx
├── README.md
└── .gitignore
```

## How to Use

1. Clone or download the repository.
2. Open `Placement_Analysis_PowerBI.pbix` using Power BI Desktop.
3. Use the **Academic Year** slicer to filter the dashboard.
4. Explore the KPI cards and analytical visuals.
5. Use the company and CTC visuals to examine recruitment patterns.

## Data Quality Notes

A small number of source records require special handling, including:

- CTC ranges instead of a single value
- Numeric CTC entries that could not be safely interpreted as LPA
- Missing company names

These records were retained with data-quality indicators rather than being silently converted or discarded.

## GitHub Workflow

The project is maintained using Git for version control.

Typical update workflow:

```bash
git status
git add .
git commit -m "Update Power BI placement analytics dashboard"
git push origin main
```

When the remote repository contains commits not present locally, synchronize before pushing:

```bash
git pull origin main --allow-unrelated-histories
git push origin main
```

## Outcome

The project delivers a compact Power BI dashboard that converts historical placement records into structured KPIs, trends, company-level recruitment insights, and CTC analysis.

It demonstrates practical skills in **data preparation, data modeling, DAX, data visualization, dashboard design, and Git/GitHub workflow**.

## Author

**Mohammad Azmath Ali**

GitHub: `mohammad-724`
