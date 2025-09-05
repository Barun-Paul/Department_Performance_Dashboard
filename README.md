# 📊 Department_Performance_Dashboard

---

## 🔎 Project Overview

This repository contains a Power BI solution to help leadership **manage the workforce, understand financial risks, and monitor project health**.

> **Key Business Question**  
> Which **projects** and **departments** are at risk of being **over budget** or **underperforming**?  
> Budgets are set on **2-year intervals**, but leadership needs to see if **a 1-year budget can cover all expenses**.

---

## 🎯 Objectives

1. **Identify Departments & Projects in the Red**  
   Spotlight areas that are **over budget** or **underperforming** so corrective action can be taken.

2. **Data Organization**  
   Structure and validate inputs from multiple sources:
   - Employee information  
   - Salary data  
   - Department budgets  
   - Project details  

3. **Power BI Dashboard**  
   Deliver a comprehensive dashboard with visibility into:
   - Employee performance & headcount cost
   - Salary distribution and trends
   - Departmental project status
   - Financial risk and budget coverage

---

## 🗂️ Repository Contents

- `Project_0509.pbix` — Main Power BI report

---

## 🧮 Metrics & KPIs (Examples)

- **Budget Variance (₹ / %)** = Actuals − Budget; (Actuals / Budget − 1)
- **Run-Rate / Burn** = YTD Actuals ÷ Months Elapsed
- **Forecast to Complete (FTC)** = YTD Actuals + Remaining Forecast
- **Year-1 Coverage Check** = (Year-1 Budget − Year-1 Forecasted Spend)
- **Project Health** = composite score (Schedule, Cost, Quality signals)
- **Salary Distribution** = median, p10/p90, departmental spread

> Note: Model supports **2-year budget windows** with a dedicated calculation to test **1-year coverage**.

---

## 🧱 Data Model (Expected Inputs)

- **Employees**: EmployeeID, DeptID, Role, JoinDate, Status  
- **Salaries**: EmployeeID, Month, BasePay, Bonus, Benefits  
- **Departments**: DeptID, DeptName, Manager, CostCenter  
- **Budgets**: DeptID, ProjectID, FiscalYear, Period, BudgetAmount, Interval (1Y/2Y)  
- **Projects**: ProjectID, DeptID, ProjectName, StartDate, EndDate, Status, PlannedCost, ActualCost

You can map your fields to these expected columns via **Power Query**.

---

## ⚙️ Setup Instructions

1. **Clone the repository**  

2. **Open the report**  
   Launch **Power BI Desktop** and open `Project_0509.pbix`.

3. **Point to your data**  
   In **Transform Data** → **Data source settings**, update file paths/connection strings (Employee, Salary, Budgets, Projects).

4. **Configure parameters (if provided)**  
   Use **Home → Transform data → Edit parameters** to set environment (Dev/Test/Prod), fiscal year start, currency, etc.

5. **Refresh the model**  
   Click **Refresh** to load all tables and compute measures.

6. **Publish (optional)**  
   Publish to the **Power BI Service** and schedule refresh as needed.

---

## 🧭 Using the Dashboard

- **Overview**: Executive snapshot (variance, coverage, risk).  
- **Departments**: Drill into budget vs. actuals, run-rate, and YoY deltas.  
- **Projects**: Portfolio heatmap, health score, at-risk flags.  
- **Salaries**: Distribution, trends, and department comparisons.  
- **Budget Coverage**: Dedicated page validating **1-year coverage** within **2-year budgets**.  
- Use slicers (Department, Project, Time) to filter and export insights.

---

## ✨ Features

- At-risk **department/project** detection with color-coded thresholds  
- **1-Year coverage** check for **2-Year** budget intervals  
- Interactive drill-throughs and tooltips  
- Clean, presentation-ready visuals for leadership reviews  
- Modular data queries for easy source swaps

---

## 🖼️ Screenshots

<img width="1133" height="728" alt="Dashboard_Screenshot" src="https://github.com/user-attachments/assets/c9813ff0-c114-43d2-90cd-f56248461b78" />


---

## 🛣️ Roadmap

- Automated refresh (Gateway/DirectQuery where applicable)  
- Forecasting & scenario analysis (What-if parameters)  
- Row-level security (RLS) by department/role  
- Performance optimization (aggregations, incremental refresh)

---

## 🔐 Data & Privacy

This project is intended for sample or anonymized data.  
Do not commit confidential employee, salary, or financial information.

