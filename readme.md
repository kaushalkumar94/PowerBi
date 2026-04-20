# Power BI Learning Journey

A structured, module-by-module learning journal documenting a complete self-paced journey through Microsoft Power BI — from installing the tool for the first time to building a full, publication-ready dashboard from a real-world dataset.

Every module in this repository includes notes, screenshots, `.pbix` files, and datasets so that anyone reading through it can follow along, replicate the work, and understand not just *what* was done but *why*.

---

## Who Is This Repository For?

This repo is useful for you if:

- You are **completely new to Power BI** and want a guided, structured starting point
- You know the basics and want to **see how a real learning journey is documented**
- You are looking for **practical examples** using a real dataset rather than toy data
- You want to understand **when to use which chart** and why — not just how to click buttons
- You are building your own **data analytics portfolio** and want a reference for structure

No prior experience with Power BI is required to follow this repository from Module 01.

---

## What You Will Learn

By going through this repository module by module, you will be able to:

**Data Preparation**
- Connect Power BI to Excel and CSV data sources
- Use Power Query to inspect, clean, and shape data before loading it into a report
- Understand why transforming data before loading is always better practice than loading raw

**Data Modeling**
- Build relationships between multiple tables using primary and foreign keys
- Design a Star Schema with a central fact table and surrounding dimension tables
- Understand cardinality (Many-to-One) and cross-filter direction and when each setting applies

**DAX — Data Analysis Expressions**
- Write basic DAX measures for aggregations like SUM, AVERAGE, and COUNT
- Understand the difference between a calculated column and a measure
- Use DAX to create KPIs that respond dynamically to filters and slicers

**Visualizations**
- Build and configure 8+ chart types: Bar, Line, Donut, Treemap, Scatter, Combo, Gauge, and Card
- Choose the right chart for the right question — not just the most visually impressive one
- Create drill-down hierarchies that let users move between summary and detail views interactively

**Advanced Features**
- Apply conditional formatting — background color rules, font color, data bars, and icon sets — to tables
- Group continuous numeric data into Bins (e.g. Age groups) and categorical data into Lists (e.g. customer segments)
- Design a dashboard layout that tells a story rather than just displaying numbers

**Final Project**
- Apply all of the above to a real-world survey dataset with 630 records
- Build a complete, multi-visual dashboard from scratch
- Extract and communicate meaningful insights from raw data

---

## Repository Structure

```
PowerBI-Learning-Journey/
│
├── README.md                        ← You are here
│
├── 01_Installation_and_Setup/       ← Interface overview, first data connection
│   ├── notes.md
│   └── screenshots/
│
├── 02_Power_Query/                  ← Data loading and transformation
│   ├── transformations.pbix
│   └── dataset/
│
├── 03_Data_Modeling/                ← Star schema, relationships, cardinality
│   ├── README.md
│   ├── relationships.pbix
│   └── screenshots/
│
├── 04_DAX/                          ← Measures, calculated columns, aggregations
│   ├── notes.md
│   ├── dax_measures.pbix
│   └── screenshots/
│
├── 05_Visualizations/               ← Drill down hierarchies, chart interaction
│   ├── README.md
│   ├── charts.pbix
│   └── screenshots/
│
├── 06_Advanced_Features/            ← Conditional formatting, bins, lists, chart types
│   ├── README.md                    ← Conditional Formatting
│   ├── bins_lists.md                ← Bins and Lists
│   ├── visualizations.md            ← Chart type guide
│   └── screenshots/
│
└── 07_Final_Project/                ← End-to-end dashboard on real survey data
    ├── README.md
    ├── project.pbix
    ├── dataset/
    └── screenshots/
```

---

## Module Overview

### 01 — Installation & Setup
The starting point. Covers downloading and installing Power BI Desktop, understanding the three core views (Report, Table, Model), navigating the interface, connecting to a data source, and creating a first basic visualization. If you have never opened Power BI before, start here.

### 02 — Power Query
Before any data reaches your report, it passes through Power Query — Power BI's built-in ETL tool. This module covers loading data from Excel and CSV files, inspecting it for quality issues, and applying transformations to prepare it for modeling. The principle here is simple: clean data in, clean report out.

### 03 — Data Modeling
A report is only as reliable as the model underneath it. This module covers building a Star Schema using the Apocalypse Store dataset — three tables (Sales, Customers, Products) connected through properly configured Many-to-One relationships. Covers the Model View, cardinality settings, and cross-filter direction.

### 04 — DAX
DAX is what separates a static table display from a dynamic, interactive report. This module introduces DAX measures — formulas that calculate in response to the current filter context. Covers SUM, AVERAGE, COUNT, and the conceptual difference between measures (dynamic) and calculated columns (static).

### 05 — Visualizations & Drill Down
Charts are not just decoration — they are answers to questions. This module focuses on building drill-down hierarchies (Store → Product) so that a single visual can show both summary and detail views. Covers the three drill actions: Drill Down (single path), Expand All, and Drill Up.

### 06 — Advanced Features
Three topics that take reports from functional to professional:
- **Conditional Formatting** — automatically color cells, add data bars, and apply icon sets based on data rules
- **Bins & Lists** — group continuous numeric data (Age, Date) and categorical data (Customer names) into meaningful buckets
- **Chart Type Guide** — a reference for when to use each of Power BI's major chart types and why

### 07 — Final Project: Data Professional Survey Breakdown
A complete dashboard built from a real survey of 630 data professionals. Covers salary by job title, programming language preferences, gender pay comparison, geographic distribution, and satisfaction scores for work/life balance and salary. Every visual type and technique from the previous modules appears here in a single, coherent report.

---

## Dataset Used

The primary dataset across Modules 03–06 is the **Apocalypse Store** — a fictional post-apocalyptic supply store with three related tables covering customers, sales transactions, and product inventory.

The final project uses the **Data Professional Survey** dataset (sourced from Alex The Analyst), containing 630 real survey responses from people working in data roles worldwide.

---

## Progress Tracker

| Module | Topic | Status |
|--------|-------|--------|
| 01 | Installation & Setup | ✅ Complete |
| 02 | Power Query | ✅ Complete |
| 03 | Data Modeling | ✅ Complete |
| 04 | DAX | ✅ Complete |
| 05 | Visualizations & Drill Down | ✅ Complete |
| 06 | Advanced Features | ✅ Complete |
| 07 | Final Project | ✅ Complete |

---

## Tools & Requirements

| Tool | Version | Cost |
|------|---------|------|
| Power BI Desktop | Latest (Microsoft Store) | Free |
| Microsoft Excel | Any recent version | For opening datasets |
| GitHub | — | For browsing this repo |

Power BI Desktop runs on **Windows only**. No Power BI Pro subscription is needed to follow any module in this repository — everything is done in the free Desktop version.

---

## Key Concepts Index

| Concept | Module |
|---------|--------|
| Power Query / ETL | 02 |
| Star Schema | 03 |
| Many-to-One Relationships | 03 |
| Cross-filter Direction | 03 |
| DAX Measures | 04 |
| Calculated Columns | 04 |
| Drill Down Hierarchies | 05 |
| Expand All | 05 |
| Conditional Formatting | 06 |
| Data Bars & Icon Sets | 06 |
| Bins (numeric grouping) | 06 |
| Lists (categorical grouping) | 06 |
| Treemap | 07 |
| Gauge Chart | 07 |
| Donut Chart | 06, 07 |
| Combo Chart | 06 |
| Scatter Plot | 06 |
| KPI Cards | 07 |

---

*Documented module by module as each topic was learned — built from scratch, no shortcuts.*
