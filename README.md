# 📊 ACA Marketplace Premium Trends (2022–2026)

Analyzing U.S. Affordable Care Act (ACA) Marketplace premium trends using CMS public data

## 📌 Project Overview

This project analyzes Affordable Care Act (ACA) Marketplace premium trends across the United States from 2022–2026, focusing on how prices have changed over time, across states, and across insurance providers.

The goal is to understand pricing behavior, market variation, and temporal trends in the individual insurance market using publicly available CMS data.

All premiums are standardized to a 30-year-old enrollee to ensure fair comparison across states and years.

## 🧠 Key Questions Answered

How have ACA marketplace premiums changed from 2022–2026?

How do premiums vary by state and insurer?

Which metal tiers (Bronze, Silver, Gold, etc.) experience the highest costs?

How much variation exists across insurers and geographies?

How have average premiums shifted over time?

## 📂 Data Sources

### Primary Source:

Centers for Medicare & Medicaid Services (CMS) 
Health Insurance Exchange Public Use Files (PUF)

Files Used:

Plan Attributes (Plan-level metadata) Years 2022-2026

Rate PUFs (Age-based premium pricing) Years 2022-2026

🔗 [https://www.cms.gov/marketplace/resources/data/public-use-files]

## 🧮 Methodology
**1. Data Preparation**

-  Plans and Rates information imported to Jupyter Notebook -aca_notebook.ipynb- 🔗 https://github.com/dareoyeleke/ACA_MARKETPLACE_TRENDS/blob/main/aca_notebook.ipynb
  
-  Filtered to individual market plans only

-  Standardized pricing to age 30

-  Removed duplicate and incomplete records

-  Normalized plan identifiers across years

**2. Aggregation Logic**

Premiums averaged across rating areas to obtain a single price per:

-  Plan

-  State

-  Year

This avoids geographic over-weighting while preserving pricing signals

**3. Analytical Scope**

-  Years analyzed: 2022–2026

-  Metrics calculated:

-  Average premium by year

-  Average premium by state

-  Average premium by metal tier

-  Top insurers by average premium

-  Year-over-year trend analysis

**4. Important Notes**

-  Prices represent filed premiums, not enrollment-weighted costs

-  Data reflects pricing behavior, not actual enrollment or utilization

-  All dollar values are nominal (not inflation-adjusted)

### 📊 Dashboard Overview


<img width="1920" height="1080" alt="ACA PREMIUM DASHBOARD" src="https://github.com/user-attachments/assets/e07ea26b-4088-4fef-b71a-8ed7c368a322" />

**The Power BI dashboard includes:**

🔹 KPI Summary

-  Average premium (latest year)

-  Total number of filed rate records

🔹 Trend Analysis

-  Line chart showing premium growth from 2022–2026

-  Breakdown by metal tier

🔹 Geographic Analysis

-  State-level average premiums (map)

-  Top 10 states by premium

🔹 Issuer Comparison

-  Top insurers by average premium across years

🔹 Methodology Panel

-  Explains data assumptions and limitations for transparency

## 🧠 Key Insights

-  Average ACA premiums increased ~40% from 2022 to 2026 calculated from Standardized Geographical premiuims for 30 Year Old enrollees 

-  Premium growth varies significantly by state and insurer.

-  Higher metal tiers consistently exhibit steeper price growth.

-  Geographic variation remains substantial even after standardization.

## 🛠️ Tools Used

-  Python (Pandas, NumPy)

-  Power BI

-  CMS Public Use Files

## 📌 Limitations

-  Analysis reflects filed rates, not actual enrollment-weighted costs.

-  Age-standardized to 30; results may differ for other age groups.

-  Does not account for subsidies, tax credits, or plan selection behavior.

## 📈 Future Enhancements

-  Incorporate enrollment-weighted premiums

-  Add inflation-adjusted pricing

-  Expand analysis to include Silver benchmark plans

-  Compare Marketplace vs Employer-sponsored premiums

-  Add demographic overlays using Census data


## ⚙️ How to Reproduce
### Requirements

-  Data Access Link 🔗 [https://www.cms.gov/marketplace/resources/data/public-use-files]

-  Jupyter Notebook
  
-  Power Bi To run CSV files

## Steps

-  Access Data files from 🔗 [https://www.cms.gov/marketplace/resources/data/public-use-files] Plan Attributes (Plan-level metadata) Years 2022-2026 and Rate PUFs (Age-based premium pricing) Years 2022-2026

-  Load source files into Jupyter Notebook

-  Access Python Script -aca_notebook.ipynb- at 🔗 [https://github.com/dareoyeleke/ACA_MARKETPLACE_TRENDS/blob/main/aca_notebook.ipynb]

-  Run Queries to generate Data 

-  CSV's from generated data can be loaded into PowerBI from Visual and Dashboard Creation

-  Explore queries and modify filters for deeper analysis

### 📎 Author

[Dare Oyeleke]
Data Analyst | Healthcare Analytics
[(https://www.linkedin.com/in/dareoyeleke/)] | [(https://github.com/dareoyeleke)]
