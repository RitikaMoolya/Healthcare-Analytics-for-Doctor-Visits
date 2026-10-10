# 🧑‍⚕️ Healthcare-Analytics-for-Doctor-Visits
## 📌 Project Overview

Healthcare utilization can vary significantly across individuals due to differences in demographic characteristics, socioeconomic conditions, health status, illness burden, insurance coverage, and chronic health conditions. However, raw healthcare data does not directly reveal how these factors influence the frequency of doctor visits.

This project performs **Exploratory Data Analysis (EDA), statistical analysis, and data visualization** on a healthcare dataset to investigate variations in doctor visits and identify meaningful patterns, relationships, and differences within the available data.

The analysis focuses on **doctor visit distribution, demographics, income levels, illness burden, reduced activity, general health status, insurance coverage, and chronic conditions**.

The overall objective is to transform raw healthcare data into meaningful insights that can support **healthcare demand understanding, resource planning, and data-driven healthcare decision-making**.

---

## 🎯 Problem Statement

Healthcare utilization can differ across individuals based on demographic characteristics, socioeconomic conditions, health status, illness burden, insurance coverage, and chronic health conditions. As a result, the frequency of doctor visits may vary across different groups of individuals.

However, raw healthcare data does not clearly explain how doctor visit patterns vary across these factors or what relationships can be observed within the data.

The problem is to analyze the given healthcare dataset and investigate **variations in doctor visits** by identifying meaningful:

- Patterns
- Trends
- Relationships
- Variations

between healthcare utilization and factors such as age, gender, income, illness, reduced activity, health status, insurance coverage, and chronic conditions.

---

## 🎯 Project Objectives

The main objectives of this analysis are:

1. Understand the structure and quality of the healthcare dataset.
2. Analyze the overall distribution of doctor visit utilization.
3. Compare doctor visits across gender groups.
4. Analyze how doctor visit utilization varies across age groups.
5. Examine doctor visit differences across income levels.
6. Analyze the relationship between illness burden and doctor visits.
7. Investigate how reduced activity days relate to doctor visits.
8. Examine the relationship between general health status and doctor visits.
9. Compare doctor visits across private insurance and free healthcare coverage groups.
10. Analyze doctor visit patterns across non-limiting and activity-limiting chronic conditions.
11. Examine the composition of each utilization group (No visits, 1–2 visits, 3+ visits).
12. Identify the strongest relationships among numerical variables using correlation analysis.
13. Derive meaningful insights that can support healthcare planning and resource allocation.

---

## 📊 Dataset Overview

The dataset contains **5,190 individual-level healthcare records** with no missing values.

### Dataset Coverage

- **Records:** 5,190
- **Original Variables:** 12
- **Age Range:** 19 to 72 years
- **Doctor Visits Range:** 0 to 9
- **Gender Split:** 52.1% Female

### Major Variables

| Category | Variables |
|---|---|
| Healthcare Utilization | Visits |
| Demographics | Gender, Age |
| Socioeconomic | Income |
| Health Burden | Illness, Reduced Activity, Health Score |
| Insurance & Coverage | Private, Freepoor, Freerepat |
| Chronic Conditions | Nchronic, Lchronic |

### Derived Features

The following calculated columns were created:

- **Age (Years)** = `Age x 100`
- **Annual Income** = `Income x 10,000`
- **Age Group** = 19–30, 31–45, 46–60, 61+
- **Income Group** = Quartile-based (Low, Lower-Middle, Upper-Middle, High)
- **Visit Group** = No visits, 1–2 visits, 3+ visits
- **Combined Chronic Condition Group** = No chronic condition, Non-limiting chronic condition, Activity-limiting chronic condition

---

## 📌 Important Terminologies:
- **🩺 Visits:** Number of doctor visits recorded during the observation period.
- **🤒 Illness:** Number of illnesses reported by the individual.
- **🛌 Reduced Activity:** Number of days of reduced activity due to illness or injury.
- **❤️ Health Score:** General health score of the individual. Higher values indicate more health problems.
- **🏥 Private Insurance:** Whether the individual has private health insurance.
- **🆓 Freepoor:** Whether the individual receives free government healthcare due to low income.
- **🎖️ Freerepat:** Whether the individual receives free government healthcare under the repatriation category.
- **🫀 Nchronic:** Chronic condition that does not limit activity.
- **🦽 Lchronic:** Chronic condition that limits activity.

---

## 🔍 Analysis Workflow

The analysis follows the workflow below:

| Step | Analysis Stage |
|---|---|
| 1 | 📥 Data Import |
| 2 | 🔎 Data Exploration & Quality Assessment |
| 3 | 🧹 Data Preparation & Feature Transformation |
| 4 | 📊 Outlier Assessment |
| 5 | 🩺 Doctor Visit Distribution Analysis |
| 6 | 👥 Demographic Analysis |
| 7 | 💵 Socioeconomic Analysis |
| 8 | 🤒 Health Burden Analysis |
| 9 | 🏥 Insurance Analysis |
| 10 | 🫀 Chronic Condition Analysis |
| 11 | 📈 Correlation Analysis |
| 12 | 💡 Key Findings & Conclusion |

---

## 🏁 Overall Conclusion

The **Healthcare Analytics for Doctor Visits** analysis shows that doctor visits are rare and unevenly distributed, with a small high-need group driving most healthcare utilization.

**Health need emerges as the strongest driver of doctor visits.** Reduced activity days, illness burden, poorer health scores, and chronic conditions, especially activity-limiting chronic conditions, are all associated with higher utilization.

Demographic and socioeconomic factors also matter, though to a lesser degree. **Older individuals, females, and lower-income groups** show higher observed utilization, while private insurance coverage has very little impact on the number of doctor visits.

Overall, the findings demonstrate that **health condition, chronic illness burden, age, and income** are important considerations for understanding healthcare demand and planning healthcare resources.

---

## 🔑 Key Findings

### 🩺 Doctor Visit Distribution

- **79.79% of individuals (4,141) had no doctor visits**, while only **20.21% (1,049)** had at least one visit.
- The average number of visits was **0.30**, with a median of **0**, showing a strongly right-skewed distribution.

### 👥 Demographics

- **Females averaged 0.36 visits compared with 0.24 for males**, and made up about **64%** of the 1–2 visit group.
- **Average visits increased with age**, rising from **0.22 (ages 19–30)** to **0.43 (ages 61+)**.
- The share of individuals with at least one visit rose from **15.07% to 28.91%** across the same age groups.

### 💵 Socioeconomic Factors

- **Average visits declined as income increased**, from **0.40 (low income)** to **0.22 (high income)**.
- **Low-income individuals made up the largest share of the 3+ visit group.**

### 🤒 Health Burden

- **Average illnesses increased from 1.26 (no visits) to 2.42 (3+ visits).**
- **Average reduced-activity days increased from 0.43 to 7.75** across the same utilization groups.
- **Average health scores increased from 1.02 to 3.06** as utilization increased.

### 🏥 Insurance & Coverage

- **Private insurance made very little difference** (0.29 visits for insured vs 0.31 for uninsured individuals).
- **Individuals receiving free healthcare due to low income showed lower utilization** (0.16 vs 0.31 visits), although this group is very small.
- **Individuals receiving free government healthcare (freerepat) showed higher utilization** (0.47 vs 0.26 visits).

### 🫀 Chronic Conditions

- **Utilization increased with chronic condition severity.** Individuals with no chronic condition averaged **0.19 visits** (13.72% with at least one visit), those with non-limiting chronic conditions averaged **0.35 visits** (23.66%), and those with activity-limiting chronic conditions averaged **0.60 visits** (35.04%).
- **The share of individuals with activity-limiting chronic conditions rose from 9.49% (no visits) to 30.11% (3+ visits).**

### 📈 Correlation Analysis

The strongest relationships with doctor visits identified in the correlation analysis were:

| Relationship | Correlation |
|---|---:|
| Visits ↔ Reduced Activity | **0.42** |
| Visits ↔ Illness | **0.22** |
| Visits ↔ Health Score | **0.19** |
| Visits ↔ Age | **0.12** |
| Visits ↔ Income | **-0.08** |

The correlation heatmap shows that most linear relationships among the numeric variables are weak, which is expected for a dataset with many zero-visit records.

---

## 💡 Overall Insight

Overall, the analysis suggests that **older adults, individuals with chronic or activity-limiting conditions, and lower-income groups** should be prioritized for care management, preventive programs, and healthcare capacity planning.

The findings provide a data-driven perspective that can support **healthcare demand planning, resource allocation, policy analysis, and identification of high-need patient groups**.

> **Note:** Correlation represents statistical association and does not imply causation. The findings describe relationships observed within the analyzed dataset. A count model such as zero-inflated Poisson or negative binomial could be used in future work to measure the independent effect of each factor.

---

## 👥 End Users

- Healthcare Organizations
- Healthcare Policy Analysts
- Health Insurance Organizations
- Public Health Researchers
- Government / Public Healthcare Programs
- Data Analysts & BI Teams

---

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Development Environment:** Jupyter Notebook

---

## 👩‍💻 Author

Ritika Moolya  
Bachelor of Computer Applications (BCA)  
Interested in Data Analytics, Data Science, and Business Intelligence

---

⭐ If you found this project useful, consider giving the repository a star!
