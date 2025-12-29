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

Plan Attributes (Plan-level metadata)

Rate PUFs (Age-based premium pricing)

🔗 https://www.cms.gov/cciio/resources/data-resources/marketplace-puf

## 🧮 Methodology
**1. Data Preparation**

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

-  Average ACA premiums increased ~40% from 2022 to 2026.

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

### 📎 Author

[Dare Oyeleke]
Data Analyst | Healthcare Analytics
[(https://www.linkedin.com/in/dareoyeleke/)] | [(https://github.com/dareoyeleke)]
