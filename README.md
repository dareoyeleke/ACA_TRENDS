# 📊 ACA Marketplace Premium Trends (2022–2026)

Analyzing U.S. Affordable Care Act (ACA) Marketplace premium trends using CMS public data

## 📌 Project Overview

This project analyzes Affordable Care Act (ACA) Marketplace premium trends across the United States from 2022–2026, focusing on how prices have changed over time, across states, and across insurance providers.

The goal is to understand pricing behavior, market variation, and temporal trends in the individual insurance market using publicly available CMS data.

All premiums are standardized to a 30-year-old enrollee to ensure fair comparison across states and years.

## 🧠 Key Questions Answered

How have ACA marketplace premiums changed from 2022–2026?

How do premiums vary by state and insurer?

Which Plan tiers (Bronze, Silver, Gold, etc.) experience the highest costs?

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

-  Standardized pricing to age 30 on rates Datasets 

-  Removed duplicate and incomplete records for both Tables, after which each datasets were concacted in yearly order

-  Normalized plan identifiers across years and merged across tables selecting only similar plan and rate identifiers

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

-  Average premium by plan tier

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

-  Breakdown by Plan tier

🔹 Geographic Analysis

-  State-level average premiums (map)

-  Top 10 states by premium

🔹 Issuer Comparison

-  Top insurers by average premium across years

🔹 Methodology Panel

-  Explains data assumptions and limitations for transparency

## 🧠 Key Insights

-  Average ACA premiums increased ~40% from 2022 to 2026 i.e from $367.97 to $513.68 calculated from Standardized Geographical premiuims for 30 Year Old enrollees (Shown in Average Premium across Years)

-  Across State Lines, even with age standardized to 30, Average Yearly Premium show a steep increase from the Highest in West Virginia to the 10th Highest North Carolina with a % increase across between both states, showing geographic variation

-  Premium growth varies significantly by insurer.

-  Higher Plan tiers consistently exhibit steeper price growth. Platinum (%) and Gold (%) plans show steeper increases in rates compared to other Plan tiers (Shown in Average Yearly Premium across Tiers). Compared to High and Low plans 


### Recommendations 
-  Policy analysts should reweight benchmark plans because of disproportionate inflation in high tiers

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

-  The following CSV's from generated data were loaded into PowerBI from Visual and Dashboard Creation
  -  metrics_avg_by_year.csv to generate 'Yearly Trend of Premiums'
  -  metrics_avg_by_year_tier.csv to generate 'Average Yearly Premiums across Plan Tiers' Chart. 
  -  metrics_avg_by_state_latest.csv to generate 'Average Premium by state' chart,  'AVG PREMIUIM 2026' and 'Filed Rate Records' KPI's, and  'Average Premium Per State 2026' Chart 
  -  metrics_issuer_avg_top.csv to generate 'Top 10 Issuers by Average Premium (22-26)'
  

-  Explore queries and modify filters for deeper analysis

### 📎 Author

[Dare Oyeleke]
Data Analyst | Healthcare Analytics
[(https://www.linkedin.com/in/dareoyeleke/)] | [(https://github.com/dareoyeleke)]
