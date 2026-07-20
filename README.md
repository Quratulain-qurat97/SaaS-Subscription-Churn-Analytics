# 🚀 SaaS Subscription & Churn Analytics

## An End-to-End B2B SaaS Retention Analysis Project

![Dashboard Preview](SaaS_Churn.gif)

---

## 📊 Executive Summary (30-Second Read)

**The Problem:** RavenStack is experiencing a severe retention crisis with **70% overall churn** and MRR Lost accelerating **18x in 2024** (from $15K to $293K monthly).

**The Root Causes:**
1. **Feature Gaps & Poor Support** drive **36%** of all churn
2. **Enterprise tier** causes **78.6%** of revenue loss ($926K)
3. **UK market** churns at **77.59%** (highest globally)
4. **Mid-market companies (21-50 seats)** churn at **74.5%**

**The Recommendations:**
1. **Immediate:** Launch "Save Desk" workflow for customers who downgrade (**75.41%** eventually churn)
2. **Short-term:** Investigate UK market operations and Enterprise feature gaps
3. **Long-term:** Redesign product roadmap to address top churn reasons

---

## 📋 Project Overview

This project analyzes customer churn patterns for a fictional B2B SaaS company (RavenStack) — identifying why customers cancel, which segments are most at risk, and where revenue loss is concentrated.

**Dataset:** [RavenStack SaaS Subscription & Churn Analytics (Kaggle)](https://www.kaggle.com/datasets/muhammadshahidazeem/customer-churn-dataset)                                       
**Tables:** 5 relational tables — accounts, subscriptions, feature_usage, support_tickets, churn_events  
**Total Records:** 500 accounts · 4,853 subscriptions · 25,068 feature usage records · 2,000 support tickets · 600 churn events  
**Tools:** MySQL Workbench · Power BI Desktop · Microsoft Excel  
**Scope:** January 2023 – December 2024  

---

## 🎯 Business Questions

| # | Question |
|---|----------|
| 1 | Which plan tier has the highest churn rate and most revenue loss? |
| 2 | What are the most common reasons customers are leaving? |
| 3 | What is the avg satisfaction score for churned vs retained customers? |
| 4 | What % of low-satisfaction customers eventually churned? |
| 5 | Which country is losing the most customers and revenue? |
| 6 | Does using certain features reduce churn? |
| 7 | Do customers who complain more churn more? |
| 8 | Do new customers churn more than long-term ones? |
| 9 | Do customers who downgrade eventually churn? |
| 10 | Does high error count in feature usage lead to higher churn? |
| 11 | Which industry has the highest churn rate? |
| 12 | Which referral source produces the most loyal customers? |
| 13 | Which company size has the highest churn rate? |

---

## 🔍 Key Findings

### 💰 Revenue Impact
- **Overall Churn Rate: 70%** — 352 out of 500 accounts churned
- **Total MRR Lost: $1,179,139**
- **MRR Lost grew 18x in 2024** — from $15,829 to $293,548

### 📊 Plan Tier Analysis
- Enterprise accounts for **78.56% of total MRR lost** ($926,345)
- One churned Enterprise customer = **12 churned Basic customers**

### 🎯 Churn Reasons (Top 5)
| Reason | Percentage |
|--------|------------|
| Feature Gaps | 19.00% |
| Poor Support | 17.33% |
| Competitor | 16.17% |
| No Reason Given | 15.83% |
| Pricing | 13.83% |

> **Key Takeaway:** Product and support issues (36%) > Pricing issues (13.83%)

### 🌍 Geographic Performance
| Country | Churn Rate | MRR Lost |
|---------|------------|----------|
| UK | 77.59% (Highest) | $244,933 |
| US | 68.04% | $645,721 (Highest) |
| Germany | 56.00% (Lowest) | $44,111 |

### 👥 Customer Segmentation
| Segment | Churn Rate |
|---------|------------|
| 21-50 seats (Mid-Market) | 74.50% (Highest) |
| 50+ seats (Enterprise) | 64.86% (Lowest) |

### 📈 Acquisition Channel Loyalty
| Source | Churn Rate |
|--------|------------|
| Partner | 75.00% |
| Organic | 75.00% |
| **Ads** | **60.20%** (Most loyal) |

### ⚠️ Downgrade Analysis (Corrected Insight)
- **75.41%** of customers who downgrade eventually churn
- Only **8.83%** of churned customers downgraded first
- **Recommendation:** Treat downgrades as urgent retention triggers

### ❌ What Does NOT Predict Churn
- Satisfaction Score (churned: 3.98 vs retained: 3.98)
- Support Ticket Volume (churned: 4.02 vs retained: 4.17)
- Feature Usage Frequency (identical across all features)
- Error Count (churned: 0.57 vs retained: 0.56)
- Customer Tenure (churned: 30.1 months vs retained: 30.1 months)

> **The signal lies in the extremes, not the averages.**

---

## 📊 Dashboard Pages

| Page | Visualizations |
|------|---------------|
| **Overview** | KPI Cards, MRR Lost by Plan, Churn Rate by Referral, Country Map |
| **Churn Drivers** | Top Churn Reason, Churn Reasons Bar Chart, Satisfaction Distribution, Downgrade Impact |
| **Product & Revenue** | Country KPIs, MRR Lost & Churn Rate Combo, Company Size Analysis, Plan Tier Analysis |
| **Executive Summary** | Executive Commentary, MRR vs MRR Lost Trend (Jan 2023–Dec 2024) |

**Features:** Interactive slicers · Tooltips · KPI cards with conditional formatting · Drill-through

---

## 🛠️ Technical Skills Demonstrated

| Skill Area | Techniques |
|------------|------------|
| **SQL** | Window Functions, Subqueries, CASE WHEN, Multi-table JOINs, Dynamic Bucketing, UNION ALL |
| **Power BI** | DAX Measures, Tooltips, Slicers, KPI Cards, Combo Charts, Map Visualizations, Conditional Formatting |
| **Data Analysis** | Churn Rate Calculation, MRR Trend Analysis, Cohort Segmentation, Leading Indicator Analysis |
| **Data Modeling** | Star Schema, Table Relationships, Data Cleansing, Null Handling |
| **Storytelling** | Executive Commentary, Actionable Recommendations, Data Limitations Documentation |

---

## 📁 SQL Analysis

All 13 business questions were answered using MySQL before building the dashboard. See **[SQL_ANALYSIS.md](SQL_ANALYSIS.md)** for all queries with result screenshots.

**Techniques used:** `GROUP BY`, `ORDER BY`, `COUNT()`, `SUM()`, `ROUND()`, `AVG()`, `CASE WHEN`, `UNION ALL`, Subqueries, Window Functions (`SUM() OVER()`), Multi-table JOINs across 5 relational tables

---

## ⚠️ Data Limitations

| Issue | Impact |
|-------|--------|
| 70% churn rate is abnormally high | Not representative of real SaaS (industry avg: 5-10%) |
| 41.25% missing satisfaction scores | Satisfaction analysis excludes incomplete records |
| Churn_flag inconsistency | Does not perfectly align with churn_events table |
| Single company dataset | Findings cannot be generalized across industries |

---

## 📈 Business Recommendations

### 🔴 Immediate (Next 30 Days)
1. **Launch "Save Desk" Workflow:** Trigger automated outreach to any customer who downgrades (75.41% eventually churn)
2. **UK Market Investigation:** Conduct customer interviews with UK churned accounts (77.59% churn rate)
3. **Enterprise Success Team:** Dedicate senior CSMs to Enterprise accounts (78.6% of MRR loss)

### 🟡 Short-Term (Next 90 Days)
4. **Feature Gap Prioritization:** Product roadmap review addressing top churn reasons (36% of churn)
5. **Mid-Market Retention Program:** Targeted campaign for 21-50 seat companies (74.5% churn)
6. **Support Quality Audit:** Investigate poor support as a top churn driver (17.33%)

### 🟢 Long-Term (Next 6-12 Months)
7. **Early Warning System:** Build predictive model combining downgrade flag, satisfaction extremes, and feature adoption
8. **Referral Program Review:** Investigate why partner/organic referrals churn at 75% vs Ads at 60%
9. **Revenue Trend Monitoring:** Track monthly MRR Lost % to measure intervention effectiveness

---

## 🚀 Getting Started

### Prerequisites
- MySQL Workbench 8.0+ (for SQL queries)
- Power BI Desktop (for dashboard viewing)
- Microsoft Excel (for initial data exploration)

### Setup Instructions
1. Clone this repository
2. Import the dataset into MySQL Workbench using the provided schema
3. Run the SQL queries in `SQL_ANALYSIS.md` to validate the data
4. Open `SaaS_Dashboard.pbix` in Power BI Desktop
5. Ensure data source connections point to your MySQL database

---

## 📁 Repository Structure

```
SaaS-Subscription-Churn-Analytics/
│
├── SaaS_Dashboard.pbix # Power BI dashboard file
├── SQL_ANALYSIS.md # All 13 SQL queries with result screenshots
├── README.md # Project documentation (this file)
├── SaaS_Churn.gif # Dashboard preview animation
└── images/ # SQL result grid screenshots directory
├── Q1.png
├── Q2.png
├── Q3.png
├── Q4.png
├── Q5.png
├── Q6.png
├── Q7.png
├── Q8.png
├── Q9a.png
├── Q9b.png
├── Q10.png
├── Q11.png
├── Q12.png
└── Q13.png
```
---

## 📬 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/quratulain-siddiqui)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Quratulain-qurat97)
[![Fiverr](https://img.shields.io/badge/Fiverr-1DBF73?style=for-the-badge&logo=fiverr&logoColor=white)](https://www.fiverr.com/quratulain0097)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:qurat33002@gmail.com)

---

**Author:** Quratulain Tariq  
**Role:** Junior Data Analyst  
**Last Updated:** July 2026  
**Status:** ✅ Portfolio-Ready

---

*"Data doesn't tell stories—analysts do."* 🚀
