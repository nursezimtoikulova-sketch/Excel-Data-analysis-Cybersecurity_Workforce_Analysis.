# Full GitHub README.md — Cybersecurity Workforce Analysis

```markdown
# Cybersecurity Workforce Analysis Report

## Dataset Overview

- **Dataset:** Cybersecurity Team — Employee Records
- **Total Employees:** 150
- **Reference Date:** January 1, 2025
- **Tool Used:** Microsoft Excel
- **Fields:** First Name, Last Name, Gender, Date of Birth,
  Position, Salary (USD), Start Year

---

## Project Structure

```
Cybersecurity-Workforce-Analysis/
│
├── data/
│   └── employees.csv
│
├── screenshots/
│   ├── 01_raw_data.png
│   ├── 02_age_analysis.png
│   ├── 03_experience_analysis.png
│   ├── 04_salary_analysis.png
│   ├── 05_gender_analysis.png
│   ├── 06_hiring_trend.png
│   └── 07_role_category.png
│
├── Cybersecurity_Workforce_Analysis.xlsx
└── README.md
```

---

## Excel Sheet Structure

| Sheet | Purpose |
|---|---|
| `Raw_Data` | Original dataset with calculated columns |
| `Calculations` | All summary tables and formulas |
| `Dashboard` | All charts and visual analysis |
| `Findings` | Written conclusions and key insights |

---

## Screenshot 1 — Raw Data Sheet

![Raw Data](screenshots/01_raw_data.png)

> *Raw_Data sheet showing original employee records with
> added calculated columns:
> Age, Experience (Years), Age Group,
> Experience Level, Salary Band, Role Category*

---

## Section 1 — Age Analysis

### Screenshot 2 — Age Analysis

![Age Analysis](screenshots/02_age_analysis.png)

> *Age distribution chart and summary table
> showing minimum, maximum, average and median age*

### Age Summary Table

| Metric | Value |
|---|---|
| Minimum Age | 25 years |
| Maximum Age | 49 years |
| Average Age | 36.4 years |
| Median Age | 36 years |
| Std Deviation | 5.8 years |

### Age Group Distribution

| Age Group | Employees |
|---|---|
| Under 25 | 0 |
| 25 – 29 | 18 |
| 30 – 34 | 32 |
| 35 – 39 | 41 |
| 40 – 44 | 35 |
| 45 – 49 | 24 |
| 50+ | 0 |

### Formulas Used

| Metric | Formula |
|---|---|
| Age | `=DATEDIF(D2,DATE(2025,1,1),"Y")` |
| Minimum Age | `=MIN(Raw_Data!H:H)` |
| Maximum Age | `=MAX(Raw_Data!H:H)` |
| Average Age | `=AVERAGE(Raw_Data!H:H)` |
| Median Age | `=MEDIAN(Raw_Data!H:H)` |
| Age Group Count | `=COUNTIF(Raw_Data!J:J,"25-29")` |

### Key Findings
- The majority of employees are in the **35–39 age group**
- The workforce is relatively **young and mid-career**
- No employees under 25 or over 50 years old
- Average age of **36 years** indicates an experienced team

---

## Section 2 — Experience Analysis

### Screenshot 3 — Experience Analysis

![Experience Analysis](screenshots/03_experience_analysis.png)

> *Experience level bar chart and summary table
> showing experience distribution across the team*

### Experience Summary Table

| Metric | Value |
|---|---|
| Minimum Experience | 1 year |
| Maximum Experience | 13 years |
| Average Experience | 6.5 years |
| Median Experience | 7 years |

### Experience Level Distribution

| Level | Years | Employees |
|---|---|---|
| Junior | 0 – 2 years | 15 |
| Mid-Level | 3 – 5 years | 38 |
| Senior | 6 – 9 years | 65 |
| Expert | 10+ years | 32 |

### Formulas Used

| Metric | Formula |
|---|---|
| Experience | `=2025-G2` |
| Minimum | `=MIN(Raw_Data!I:I)` |
| Maximum | `=MAX(Raw_Data!I:I)` |
| Average | `=AVERAGE(Raw_Data!I:I)` |
| Level Count | `=COUNTIF(Raw_Data!K:K,"Senior (6-9 yrs)")` |

### Key Findings
- **Senior level (6–9 years)** is the largest group in the team
- **Expert employees (10+ years)** command the highest salaries
- Only **~10%** of the team are Junior level
- Strong **positive correlation** between experience and salary

---

## Section 3 — Salary Analysis

### Screenshot 4 — Salary Analysis

![Salary Analysis](screenshots/04_salary_analysis.png)

> *Salary distribution chart and salary band breakdown
> showing compensation spread across the team*

### Salary Summary Table

| Metric | Value |
|---|---|
| Minimum Salary | $52,000 |
| Maximum Salary | $245,000 |
| Average Salary | $130,200 |
| Median Salary | $130,000 |
| Std Deviation | $33,400 |

### Salary Band Distribution

| Salary Band | Employees |
|---|---|
| Under $80K | 12 |
| $80K – $99K | 14 |
| $100K – $129K | 38 |
| $130K – $159K | 52 |
| $160K – $199K | 27 |
| $200K+ | 7 |

### Formulas Used

| Metric | Formula |
|---|---|
| Minimum Salary | `=MIN(Raw_Data!F:F)` |
| Maximum Salary | `=MAX(Raw_Data!F:F)` |
| Average Salary | `=AVERAGE(Raw_Data!F:F)` |
| Median Salary | `=MEDIAN(Raw_Data!F:F)` |
| Band Count | `=COUNTIF(Raw_Data!L:L,"$130K - $159K")` |

### Key Findings
- The **$130K – $159K** band has the highest concentration
- **CISO** holds the highest salary at **$245,000**
- Interns and Trainees fall in the **Under $80K** range
- Average and median salary are nearly equal — **balanced distribution**
- Top 10% of earners are all in **Management or Expert** roles

---

## Section 4 — Gender Analysis

### Screenshot 5 — Gender Analysis

![Gender Analysis](screenshots/05_gender_analysis.png)

> *Gender distribution pie chart and
> average salary comparison by gender*

### Gender Summary Table

| Metric | Male | Female |
|---|---|---|
| Headcount | 75 | 75 |
| Average Salary | $133,000 | $127,000 |
| Average Age | 36.2 years | 36.6 years |
| Avg Experience | 6.6 years | 6.4 years |

### Formulas Used

| Metric | Formula |
|---|---|
| Male Count | `=COUNTIF(Raw_Data!C:C,"Male")` |
| Female Count | `=COUNTIF(Raw_Data!C:C,"Female")` |
| Avg Salary Male | `=AVERAGEIF(Raw_Data!C:C,"Male",Raw_Data!F:F)` |
| Avg Salary Female | `=AVERAGEIF(Raw_Data!C:C,"Female",Raw_Data!F:F)` |
| Avg Age Male | `=AVERAGEIF(Raw_Data!C:C,"Male",Raw_Data!H:H)` |

### Key Findings
- Gender split is **exactly 50/50** — equal representation
- A **salary gap of ~$6,000** exists in favor of male employees
- Age and experience levels are **nearly identical** across genders
- Gap is most visible in **Management and Expert** tier roles

---

## Section 5 — Hiring Trend Analysis

### Screenshot 6 — Hiring Trend

![Hiring Trend](screenshots/06_hiring_trend.png)

> *Annual hiring trend line chart from 2012 to 2024
> showing team growth over time*

### Hiring Per Year

| Year | Employees Hired |
|---|---|
| 2012 | 1 |
| 2013 | 2 |
| 2014 | 7 |
| 2015 | 11 |
| 2016 | 17 |
| 2017 | 16 |
| 2018 | 22 |
| 2019 | 18 |
| 2020 | 19 |
| 2021 | 13 |
| 2022 | 9 |
| 2023 | 10 |
| 2024 | 5 |

### Formulas Used

| Metric | Formula |
|---|---|
| Count by Year | `=COUNTIF(Raw_Data!G:G,2018)` |

### Key Findings
- **2018** was the peak hiring year with **22 new employees**
- Team grew consistently from **2012 through 2020**
- Hiring slowed slightly after **2020**
- Recent hires in **2023–2024** are mostly **Junior and Intern** level
- The team has been **growing for over 12 years**

---

## Section 6 — Role Category Analysis

### Screenshot 7 — Role Category Salary

![Role Category](screenshots/07_role_category.png)

> *Average salary by role category horizontal bar chart*

### Role Category Summary

| Role Category | Avg Salary | Headcount |
|---|---|---|
| Management / Director | $175,000 | 28 |
| Engineering | $148,000 | 35 |
| Analyst / Specialist | $132,000 | 42 |
| Operations | $125,000 | 30 |
| Junior / Intern | $76,000 | 15 |

### Formulas Used

| Metric | Formula |
|---|---|
| Avg Salary by Category | `=AVERAGEIF(Raw_Data!M:M,"Management",Raw_Data!F:F)` |
| Count by Category | `=COUNTIF(Raw_Data!M:M,"Engineering")` |

### Key Findings
- **Management roles** command the highest average salary
- **Engineering roles** are second highest — reflecting market demand
- **Analyst roles** form the largest group in the team
- **Junior/Intern** salaries are significantly below team average

---

## Overall Findings Summary

| Metric | Value |
|---|---|
| Total Employees | 150 |
| Age Range | 25 – 49 years |
| Average Age | 36.4 years |
| Experience Range | 1 – 13 years |
| Average Experience | 6.5 years |
| Salary Range | $52,000 – $245,000 |
| Average Salary | $130,200 |
| Gender Split | 50% Male / 50% Female |
| Unique Positions | 100+ roles |
| Peak Hiring Year | 2018 |
| Largest Age Group | 35 – 39 years |
| Largest Experience Group | Senior (6–9 years) |
| Highest Paid Role | CISO — $245,000 |
| Lowest Paid Role | Cyber Security Intern — $52,000 |

---

## Tools Used

- Microsoft Excel
- Git
- GitHub

---

*Analyst:]*
*Date: 2025*
*Project: Cybersecurity-Workforce-Analysis*
```
