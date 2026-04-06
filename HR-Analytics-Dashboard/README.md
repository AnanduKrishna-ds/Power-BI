# HR Analytics Dashboard — Power BI

## 📊 Overview
An interactive HR Analytics Dashboard built in Power BI analyzing workforce data for **1,020 employees** across **6 departments** and **6 US states**.

This project demonstrates the full data analyst workflow — from messy raw data to a polished interactive dashboard.

---

## 🖼 Dashboard Preview

(Add screenshot here)

Key Metrics:

- Attrition Rate: **30.59%**
- Total Employees: **1,020**
- Average Salary: **$85K**

---

## 🔄 Project Workflow

### Phase 1 — Data Understanding
- Audited raw CSV dataset
- Identified **8 data quality issues**
- Reviewed columns:
  - Age
  - Join_Date
  - Salary
  - Phone
  - Department_Region
  - Status
  - Remote_Work

---

### Phase 2 — Data Cleaning (Power Query)

- Fixed mixed date formats using locale conversion
- Replaced invalid salary values
- Removed negative signs from phone numbers
- Split Department_Region column
- Renamed columns for consistency
- Verified **0% errors** using Column Quality view

---

### Phase 3 — DAX Measures

```DAX
Total Employees = COUNTROWS(Messy_Employee_dataset)

Avg Salary = AVERAGE(Messy_Employee_dataset[Salary])

Attrition Rate =
DIVIDE(
    COUNTROWS(
        FILTER(
            Messy_Employee_dataset,
            Messy_Employee_dataset[Status] = "Inactive"
        )
    ),
    COUNTROWS(Messy_Employee_dataset)
)

Avg Age = AVERAGE(Messy_Employee_dataset[Age])



## Visualizations Used

- KPI Cards — Attrition Rate, Total Employees, Avg Salary  
- Donut Chart — Employee Status  
- Map — Geographic Distribution  
- Bar Charts — Department & Region Analysis  
- Scatter Plot — Salary vs Age  
- Slicers — Department & Status filtering  

---

## Key Findings

- Attrition rate is **30.59%**
- Sales department shows highest average salary (~$87K)
- California and Florida have highest employee counts
- Salary distribution across departments is consistent

---

## Dataset

- Source: Kaggle — Messy Employee Dataset  
- Rows: ~1,000  
- Columns: 13 (after cleaning)

---

## Tools Used

- Power BI Desktop  
- Power Query  
- DAX  

---

## Skills Demonstrated

- Data Cleaning  
- Data Transformation  
- DAX Measure Creation  
- Dashboard Design  
- KPI Visualization  
- Interactive Filtering
