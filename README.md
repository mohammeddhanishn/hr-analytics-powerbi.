# HR Analytics Dashboard (Power BI)

## 1. Business Question
Why are employees leaving, and which groups are most at risk?
The dashboard helps HR find where attrition is highest (by department, age group, salary slab, overtime, travel and job role) so retention efforts can be targeted.

## 2. Dataset
- **Name:** HR Analytics (`HR_Analytics-4.csv`)
- **Source:** [ADD DATASET SOURCE LINK, e.g. Open Dataset Directory / Kaggle]
- **Size:** 1,480 rows × 37 columns
- **Key columns:**
  - `EmpID`, `Age`, `AgeGroup`, `Gender`, `MaritalStatus`: employee profile
  - `Department`, `JobRole`, `JobLevel`: position
  - `MonthlyIncome`, `SalarySlab`, `SalaryHike %`: pay
  - `OverTime`, `BusinessTravel`, `DistanceFromHome(KM)`: working conditions
  - `JobSatisfaction`, `WorkLifeBalance`, `EnvironmentSatisfaction`: satisfaction scores (1–4)
  - `TotalExperience(Years)`, `YearsatCompany`, `YearsSincePromotion`: tenure
  - `Attrition` (Yes/No): target of the analysis

## 3. Tools Used
- **Power BI Desktop**: Power Query, data model, DAX, report pages
- **Visuals:** KPI cards, donut, pie, funnel, area, clustered column/bar, matrix, slicers

## 4. Steps Followed
1. Loaded the CSV into Power BI and cleaned it in Power Query (data types, duplicate EmpIDs, inconsistent `BusinessTravel` values such as `TravelRarely` vs `Travel_Rarely`).
2. Created `AttritionCount` and the `Attrition Rate %` measure.
3. Added further DAX measures: [LIST YOUR MEASURES, e.g. Active Employees, Overtime Attrition %, Avg Income, Avg Tenure, Avg Satisfaction].
4. **Page 1: HR Analytics Dashboard.** KPI cards, attrition by department, salary slab, gender, age group and experience, plus a job role × job satisfaction matrix. Slicers for Department and Age Group.
5. **Page 2: Attrition Drivers.** Attrition rate by overtime, business travel and job role.

## 5. Key Insights
1. Overall attrition is about **16.3%** (241 of 1,480 employees).
2. **Overtime is the strongest driver.** Employees working overtime leave at 31.2%, versus 10.4% for those who don't (about 3×).
3. **Sales Representatives have the highest attrition (40.5%)**, followed by HR (25.9%) and Laboratory Technicians (23.6%).
4. **Young and new employees leave most.** Ages 18–25 have 36.6% attrition, and employees with 0–2 years of experience about 44%.
5. **Frequent travellers leave at 25.8%**, compared with 7.9% for non-travellers.
6. By department, **HR (26.8%) and Sales (25.2%)** have the highest rates. Administration has the most leavers (88) mainly because it is a large department.
7. **Single employees leave at 21.7%**, nearly double the rate of married employees (11.5%).

**Recommendations:** review overtime workload, improve onboarding and early-career support for employees in their first two years, and run a retention plan for the Sales Representative role.

## 6. Screenshots or Output
![Page 1](screenshots/page1_dashboard.png)
![Page 2](screenshots/page2_attrition_drivers.png)

Full PDF export: `dashboard_export.pdf`

## 7. How to Run or Open
1. Download `PROJECT_DASHBOARD_POWER_BI.pbix` and open it in Power BI Desktop.
2. If the data source path is not found, go to *Transform data → Data source settings* and point it to `data/HR_Analytics-4.csv`.
3. Use the slicers on the page to filter by department and age group.

## 8. Author
Mohammed Danish N, Batch [YOUR BATCH], Axionz Global Pvt Ltd, Data Analytics Program
