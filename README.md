# 📊 HR Employee Attrition Dashboard — Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-185FA5?style=for-the-badge&logoColor=white)
![Dataset](https://img.shields.io/badge/Dataset-IBM%20HR%20Analytics-purple?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

> **"Why are employees leaving?"** — An interactive Power BI dashboard built on the IBM HR Analytics Attrition Dataset to visually explore and answer this question using real data.

---

## 🖼️ Dashboard Preview

![HR Attrition Dashboard](https://github.com/bhavyajain0408/HR-Employee-Attrition-Dashboard/blob/main/HR%20attrition.png)

> *Add your dashboard screenshot here — rename your screenshot to `dashboard_screenshot.png` and place it in this folder*

---

## 📌 Project Overview

| Detail | Info |
|---|---|
| **Tool** | Power BI Desktop |
| **Dataset** | IBM HR Analytics Attrition Dataset |
| **Records** | 1,470 employees · 35 features |
| **Objective** | Identify key drivers of employee attrition |
| **Type** | Exploratory Data Analysis (EDA) — Visual |
| **Internship** | SkillCraft Technology |

---

## 🎯 Objective

Instead of building a Machine Learning model, this project focuses on the **"Why"** — using visual EDA to uncover which factors most strongly correlate with employees leaving the organization.

---

## ✅ Dashboard Features

### KPI Cards
| Metric | Value |
|---|---|
| Total Employees | 1,470 |
| Attrition Count | 237 |
| Attrition Rate | 16.12% |
| Avg Monthly Income | $6,500 |

### 📊 Charts (6 Visuals)
- **Attrition Rate by OverTime** — Yes vs No comparison
- **Attrition Rate by AgeGroup** — 18-30, 31-45, 46+
- **Attrition Rate by JobSatisfaction** — Levels 1 to 4
- **Attrition Rate by WorkLifeBalance** — Scores 1 to 4
- **Attrition by Department** — R&D, Sales, HR
- **Avg Monthly Income by JobLevel and Attrition** — Leavers vs Stayers

### 🔽 Slicers (Filters)
- Gender
- Department
- AgeGroup

> All charts and KPI cards update dynamically when a slicer is clicked.

---

## 💡 Key Insights

1. **Overtime is the #1 factor** — Employees working overtime are **3× more likely** to leave (~38% attrition) compared to those who don't (~10%)
2. **Young employees leave most** — The **18–30 age group** has the highest attrition rate (~25%) — career growth expectations may not be met
3. **Low satisfaction = high churn** — **Job Satisfaction level 1** has the highest attrition (~22%) — clear inverse relationship
4. **Poor work-life balance drives exits** — **WLB score 1** shows 30%+ attrition — nearly double higher scores
5. **Income gap at entry level** — Employees at **Job Level 1 & 2** who earn below average are significantly more likely to quit

---

## 🛠️ DAX Measures Used

```dax
-- Attrition Rate
Attrition Rate = DIVIDE(SUM([AttritionNum]), COUNT([EmployeeNumber]))

-- AttritionNum Column
AttritionNum = IF([Attrition] = "Yes", 1, 0)

-- AgeGroup Column
AgeGroup = IF([Age] <= 30, "18-30", IF([Age] <= 45, "31-45", "46+"))
```

---

## 📁 Project Structure

```
HR-Attrition-Dashboard/
│
├── HR_Attrition_Dashboard.pbix    ← Power BI file
├── WA_Fn-UseC_-HR-Employee-Attrition.csv  ← Dataset
├── dashboard_screenshot.png       ← Dashboard image
└── README.md                      ← This file
```

---

## 📂 Dataset

- **Source:** IBM HR Analytics Employee Attrition & Performance
- **Platform:** Kaggle
- **Link:** [kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- **Size:** 1,470 rows × 35 columns
- **License:** Public / Open

---

## 🚀 How to Open

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop) (free)
2. Clone or download this repository
3. Open `HR_Attrition_Dashboard.pbix` in Power BI Desktop
4. Use the slicers (Gender, Department, AgeGroup) to explore the data interactively

---

## 👩‍💻 About

**Bhavya Jain** — Data Analytics Intern at SkillCraft Technology

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/bhavya-jain-4a883030b)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat&logo=github)](https://github.com/bhavyajain0408)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ **If you found this useful, give the repo a star!**
