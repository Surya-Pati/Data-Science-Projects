# Hospital Operations & Patient Analytics Dashboard

This project delivers a three-view interactive Power BI dashboard built on a star schema hospital dataset to analyze patient metrics, operational KPIs, bed utilization, and treatment costs across 10 departments. The objective is to provide healthcare administrators and analysts with actionable insights for improving patient care, resource allocation, and operational efficiency.

---

## Project Overview

Healthcare organizations generate large volumes of data across patient records, treatments, staffing, and bed management. This dashboard transforms a normalized star schema (5 tables, 2,506 patient records) into a drill-through Power BI report with three analytical layers — an executive Overview, a Department Drill-through for granular department-level analysis, and a Patient & Staff Analysis view for resource and cost intelligence.

The dashboard enables stakeholders to monitor patient outcomes, identify operational bottlenecks, track bed utilization, and support data-driven staffing and resource decisions.

---

## Objectives

- Build a multi-view Power BI dashboard to visualize healthcare KPIs across patient, operational, and staff dimensions
- Analyze patient demographics, admission trends, treatment costs, and bed utilization by department
- Implement drill-through navigation for department-level deep dives
- Surface rating and satisfaction insights to support patient experience improvements
- Provide interactive filters for dynamic, stakeholder-ready exploration

---

## Dataset — Star Schema (5 Tables)

| Table | Rows | Key Columns |
|---|---|---|
| Fact_Patient_Admissions | 2,506 | Patient_ID, Staff_ID, Department_ID, Bed_ID, Admission_Date, LOS, Treatment_Cost, ER_Time, Rating, Discharge_Date |
| Patient_Dim | 2,506 | Patient_ID, Gender, Age, City, State, Patient_Type, Status |
| Staff_Dim | 262 | Staff_ID, Staff_Name |
| Department_Dim | 10 | Department_ID, Department_Name |
| Bed_Dim | 2,847 | Bed_ID, Bed_Number |

- **Date Range:** January 2007 – December 2007
- **Departments:** OPD, Physical Medicine & Rehabilitation, Surgery, OT, Dermatology, Orthopaedics, Neurology, Gynaecology, Cardiology, Oncology

---

## Key Business Findings

### Patient Overview
- **2,506 total patients** across 10 departments in 2007
- **67% Inpatients** (1,679) vs 33% Outpatients (827)
- Average Length of Stay: **1.70 days**
- OPD is the highest-volume department at **824 patients** — nearly one-third of total admissions

### Patient Satisfaction
- **72.94% of patients rated their experience 5/5** — a strong patient satisfaction signal
- 22.67% rated 4/5 — combined 95.6% positive ratings (4 or 5)
- Only 4.4% of patients gave ratings of 3 or below — actionable target for quality improvement

### Bed Utilization
- **61.50% bed utilization** across 2,847 beds — 38.5% of beds were unused during 2007
- Bed Occupancy: **88.02%** of admitted patients were assigned a physical bed
- 755 patients (30%) categorized as Unassigned — predominantly outpatient same-day visits

### Staffing & Load
- **262 staff** managing 2,506 patients — average patient load of **9.56 patients per staff member**
- Physical Medicine & Rehabilitation carries the highest average patient load among inpatient departments
- Average ER time and treatment costs vary significantly by department — surfaced on drill-through pages

### Treatment Costs
- Average treatment cost: **₹807** per patient
- Maximum treatment cost: **₹6,207** (outlier — 12 patients exceed ₹5,000)
- Cost distribution is heavily right-skewed — majority of patients fall below ₹1,500

---

## Dashboard Architecture

### Page 1 — Overview
Executive-level summary for hospital administrators.
- KPI cards: Total Patients, Avg LOS, Total Staff, Bed Occupancy %
- Admissions Trend by date (2007 full year — seasonality visible)
- Patients by Department (horizontal bar — volume comparison)
- Patient Type distribution (Inpatient vs Outpatient donut)
- Avg Treatment Cost by Department (operational cost intelligence)

### Page 2 — Department Drill-through
Activated by clicking any department on Page 1. Filters all visuals to the selected department.
- KPI cards: Department-level Total Patients, Avg LOS, Total Staff, Bed Occupancy %
- Decomposition tree: Total Patients → Gender → Age Group
- Admissions trend (department-specific, drill-down by Year/Quarter/Month/Day)
- Bed Utilization % gauge (capped at 100%)
- Patient Rating distribution donut

### Page 3 — Patient & Staff Analysis
Operational deep-dive for resource planning and cost analysis.
- KPI cards: Total Patients, Avg LOS, Total Staff, Avg Patient Load per Staff
- Treatment Cost vs Total Patients scatter (cost distribution by department)
- Avg Patient Load by Department (bar chart — staffing pressure indicator)
- Bed Utilization % gauge
- Geographic patient distribution map (Total Patients, Avg Patient Load, Patients per Staff by State)

---

## Methodology

1. **Data Preparation**
   - Star schema already normalized across 5 dimension and fact tables
   - Validated relationships: Fact_Patient_Admissions → Patient_Dim, Staff_Dim, Department_Dim, Bed_Dim
   - Handled "Unassigned" Bed_ID values for outpatient records

2. **Key DAX Measures**
   - `Avg LOS = AVERAGE(Fact_Patient_Admissions[LOS])`
   - `Bed Occupancy % = DIVIDE(COUNTROWS(FILTER(Fact_Patient_Admissions, Bed_ID <> "Unassigned")), COUNTROWS(Fact_Patient_Admissions))`
   - `Bed Utilization % = DIVIDE(CALCULATE(COUNTROWS(Fact_Patient_Admissions), Bed_ID <> "Unassigned"), CALCULATE(COUNTROWS(Bed_Dim), ALL(Bed_Dim)))`
   - `Avg Patient Load = DIVIDE(COUNTROWS(Fact_Patient_Admissions), COUNTROWS(Staff_Dim))`

3. **Dashboard Development**
   - Drill-through navigation: Overview → Department page (filtered by Department_Name)
   - Report Connections: Single slicer set (Gender, Age Group, Admission Date, Department) controls all pages
   - Clear All Slicers button on every page for reset functionality
   - Gauge visuals capped at 100% maximum for utilization metrics

4. **Insights**
   - Patient satisfaction benchmarking (72.94% top-rated)
   - Bed utilization gap analysis (61.50% — 38.5% unused capacity)
   - Department-level staffing pressure identification
   - Geographic patient sourcing by state

---

## Results

- OPD identified as the highest-pressure department — 824 patients, highest volume by 60% over the next department
- Patient satisfaction is strong overall (95.6% rated 4 or 5) but varies by department — drill-through enables targeted quality review
- 38.5% unused bed capacity signals either overstaffed infrastructure or significant outpatient-to-inpatient conversion opportunity
- Physical Medicine & Rehabilitation has the highest avg patient load — resourcing priority for hospital management
- Treatment cost outliers (12 patients above ₹5,000) warrant clinical review — flagged via scatter chart on Page 3

---

## Technologies Used

- Microsoft Power BI (Desktop)
- DAX (Data Analysis Expressions) — calculated measures and KPIs
- Star Schema data modeling (5 tables)
- Drill-through navigation, Report Connections, slicer synchronization
- Map visual, decomposition tree, gauge chart, donut chart, scatter chart

---

## How to Run

- Open the file: `Healthcare_Dataset_Insights_Dashboard.pbix`
- Start on the **Overview** page for the executive summary
- Click any department bar on the Overview page to drill through to the **Department Analysis** page (Requires drill through to be enabled via click on chart -> goto to data/drill -> click drill-through)
- Use slicers (Gender, Age Group, Admission Date, Department) to filter all visuals simultaneously
- Click **Clear All Slicers** to reset filters on any page

---

## Purpose

This project demonstrates capabilities in:

- Multi-view Power BI dashboard design with drill-through navigation
- Star schema data modeling and DAX measure development
- Healthcare KPI analysis — bed utilization, patient load, LOS, treatment costs
- Patient satisfaction analytics and department benchmarking
- Translating raw hospital data into stakeholder-ready, decision-driving insights

---

## Acknowledgements

Thanks to the dataset providers, open-source resources, and the data science community for enabling this analysis.
