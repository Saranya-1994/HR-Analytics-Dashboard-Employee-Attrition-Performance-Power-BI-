# 👥 HR Analytics Dashboard — Power BI

> An interactive multi-page Power BI dashboard analyzing **employee attrition and performance** across a 1,470-employee workforce, delivering data-driven insights to support HR leadership in workforce planning, retention strategy, and employee engagement.

---
---

## 📌 Project Overview

This project analyzes HR data to uncover the key drivers of employee attrition, identify high-risk employee groups, and provide actionable recommendations to reduce turnover and improve workforce satisfaction.

| Metric | Value |
|---|---|
| Total Employees | 1,470 |
| Attrition Count | 237 |
| Attrition Rate | 16.12% |
| Avg Monthly Income | $6.50K |
| Highest Attrition Role | Sales Executive (326) |
| Dashboard Pages | 2 |

---

## 📂 Repository Structure

```
hr-analytics-dashboard/
│
├── README.md
├── dataset/
│   └── HR_Analytics.csv              # Raw HR dataset
├── powerbi/
│   └── HR_Analytics_Dashboard.pbix   # Power BI report file
└── screenshots/
    ├── page1_overview.png             # HR Analytics Overview page
    └── page2_satisfaction.png         # Performance Satisfaction Analysis page
```

---

## 📊 Dashboard Pages

### Page 1 — HR Analytics Overview

| Visual | Description |
|---|---|
| KPI Cards | Avg Monthly Income, Attrition Rate %, Total Employees, Attrition Count |
| Attrition by JobRole | Bar chart ranking all job roles by attrition count |
| Performance Rating VS Attrition | Grouped bar — Excellent vs Outstanding performance |
| Avg Monthly Income by Education | Clustered bar by education level and attrition status |
| Attrition by Marital Status | Pie chart — Divorced, Married, Single distribution |
| Key Insights Panel | Auto-generated business observations for HR leadership |

<img width="1318" height="718" alt="Screenshot 2026-04-17 105449" src="https://github.com/user-attachments/assets/32a3e405-68da-4bfe-ab9e-9d9f3d55eec9" />


### Page 2 — Performance Satisfaction Analysis

| Visual | Description |
|---|---|
| Distance From Home by JobRole | Clustered bar showing attrition by commute distance |
| Attrition by Work Life Balance | Horizontal bar — Bad, Best, Better, Good ratings |
| Job Satisfaction VS Attrition | Stacked bar by satisfaction level (Very High, High, Low, Medium) |
| Job Involvement VS Attrition | Stacked bar by involvement level |
| Insight Cards | Distance Attrition, Satisfaction Attrition, Involvement Attrition summaries |

<img width="1330" height="739" alt="Screenshot 2026-04-17 105501" src="https://github.com/user-attachments/assets/60c21002-49a0-49a9-b182-cad74cb39c86" />


---

## 🔍 Key Business Insights

- **Sales Executives have the highest attrition (326 employees)** — targeted retention programs needed for this role
- **Attrition is higher among employees with Excellent performance ratings** — high performers may be leaving due to low engagement or compensation gaps
- **Employees living closer to the workplace show higher attrition** — commute distance alone is not a retention factor
- **Attrition is highest among employees with High and Very High job satisfaction** — satisfaction ratings may not reflect true engagement
- **Employees with High job involvement show the highest attrition count** — workload and burnout may be contributing factors
- **Doctors have the highest average income but moderate attrition** — income alone does not guarantee retention

---

## 🛠 Tools & Techniques

| Tool | Purpose |
|---|---|
| Power BI Desktop | Dashboard design and report development |
| DAX | Custom KPI measures, calculated columns, time intelligence |
| Power Query (M Language) | Data cleaning and transformation |
| Data Modeling | Star schema relationships across HR tables |

### DAX Measures Used
- `Attrition Rate % = DIVIDE([Attrition Count], [Total Employees], 0)`
- `Avg Monthly Income = AVERAGE(HR_Analytics[MonthlyIncome])`
- `Attrition Count = COUNTROWS(FILTER(HR_Analytics, HR_Analytics[Attrition] = "Yes"))`
- `Total Employees = COUNTROWS(HR_Analytics)`

---

## 🎛 Slicers and Filters

The dashboard includes 5 interactive slicers for self-service HR reporting:

- **JobRole** — Filter by specific job roles
- **EducationField** — Filter by field of education
- **Attrition** — Toggle between Yes / No attrition status
- **Gender** — Filter by Female / Male
- **Age** — Filter by age group

---

## 📁 Dataset

| Column | Description |
|---|---|
| Age | Employee age |
| Attrition | Yes / No attrition status |
| JobRole | Employee job title |
| MonthlyIncome | Monthly salary in USD |
| PerformanceRating | Excellent / Outstanding |
| JobSatisfaction | 1 to 4 scale |
| WorkLifeBalance | 1 to 4 scale |
| JobInvolvement | 1 to 4 scale |
| DistanceFromHome | Commute distance in km |
| Education | Education level |
| MaritalStatus | Divorced / Married / Single |

> Source: IBM HR Analytics Employee Attrition Dataset (open dataset)

---



---






