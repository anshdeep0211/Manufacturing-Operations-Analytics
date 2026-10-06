# Manufacturing Operations Analytics Dashboard (Power BI)

An end-to-end interactive Power BI dashboard designed to evaluate manufacturing performance, operational efficiency, quality control, and machine maintenance across production lines.

---

## Executive Summary

This project provides a comprehensive overview of manufacturing operations by tracking core business metrics including work order fulfillment, production output, quality control pass rates, and machine downtime causes. 

### Key Dashboard Insights:
* **Total Work Orders Processed:** 1,000 orders across 6 machinery assets.
* **Overall Production Output:** 407,000 units produced with peak volume occurring in October 2025 (43K units).
* **Quality Assurance Performance:** **94.45%** pass rate across 5,265 total quality checks.
* **Maintenance & Downtime:** 64 total downtime hours logged across 30 maintenance events, with *Operator Error* (30.51%) being the leading downtime cause.

---

## Dashboard Views & Architecture

The report contains 4 core analytical pages tailored for executive, operational, quality, and maintenance stakeholders:

### 1. Executive Overview
Focuses on macro-level manufacturing KPIs and output trends.
* **KPI Cards:** Work Orders (1,000), Units Produced (407K), Defective Units (905), Active Machines (6), Active Products (4).
* **Production Line Output:** Assembly Line A (150K+ units), Component Line C, and Finishing Line B.
* **Product Mix:** Beta Gizmo, Delta Device, Gamma Gadget, and Alpha Widget.
* **Work Order Status:** 35.6% In Progress, 35.2% Pending, 29.2% Completed.

### 2. Production Performance Analysis
Deep dives into manufacturing throughput, bottlenecks, and cross-tabulation matrix.
* **Production Contribution Matrix:** Displays line-by-product breakdown across 5,265 production logs.
* **Status Distribution:** Evaluates progress states across product families.
* **Monthly Peak Trends:** Identifies top-performing months (Oct-25: 43K, Feb-26: 39K, Jan-26/Aug-25/May-25: 38K each).

### 3. Quality Control Analysis
Monitors yield metrics, defect categorization, and inspection breakdown.
* **Pass/Fail Distribution:** 4.97K Passed Checks (94.45%) vs. 292 Failed Checks (5.55%) resulting in 905 total defective units.
* **Top Defect Types:** Missing Component (218), Scratch (199), Dent (177), Functional Failure (165), Incorrect Color (146).
* **Defect Decomposition Tree:** Interactive root-cause breakdown by Check Type $\rightarrow$ Product $\rightarrow$ Defect Type.

### 4. Machine Health & Maintenance Analysis
Tracks machinery reliability, environmental telemetry, and downtime root causes.
* **Telemetry Benchmarks:** Average Temperature (100°F/°C), Average Pressure (325 PSI).
* **Downtime Hours by Asset:** Stamping Press (14 hrs), Circuit Printer (13 hrs), CNC Mill (12 hrs), Injection Molder (11 hrs), Paint Booth (9 hrs), Polishing Station (5 hrs).
* **Root Cause Breakdown:** Operator Error (30.51%), Unscheduled Maintenance (26.27%), Power Outage (22.03%), Material Shortage (21.19%).

---

## Data Model & Tech Stack

* **Tool:** Power BI Desktop
* **Data Transformation:** Power Query (Data cleaning, type casting, missing value handling)
* **Modeling & Metrics:** DAX (Data Analysis Expressions) for aggregated metrics, percentages, dynamic filtering, and conditional formatting
* **Visuals:** Custom KPI Cards, Line Charts, Stacked Bar Charts, Decomposition Tree, Donut Charts, Data Matrices

---

## Repository Structure

```text
├── README.md                          <-- Project documentation & overview
├── data/                              <-- Raw / Sample datasets (CSVs)
├── powerbi/
│   └── Manufacturing_Analytics.pbix  <-- Power BI Report File
└── pdf/                       <-- Visual previews of report pages
