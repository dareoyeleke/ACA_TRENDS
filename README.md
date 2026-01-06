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

-  Across State Lines, even with age standardized to 30, Average Yearly Premium show a steep increase from the Highest in West Virginia to the 10th Highest North Carolina with a 39% difference between both states, showing geographic variation

-  Premium growth varies significantly by insurer. 

-  Higher Plan tiers consistently exhibit steeper price growth. Platinum (44%) and Gold (27%) plans show steeper increases in rates compared to other Plan tiers (Shown in Average Yearly Premium across Tiers). Compared to High(2%) and Low(-180%) plans. The increase in rates do not mirror subsidies for holders of such plan or those in the mirrored tax bracket that purchasing such plans apply to. 


### Recommendations 
-  Policy analysts should reweight benchmark plans because of disproportionate inflation in high tiers to discourage disincentivization of Platinum and Gold plan holders from investing in shared cost programs that balance out cost of other tiers.
-  Insurers will be affected by demand of plan purchases due to disproportionate increase of premium rates, leading to revenue loss over time. Policy Analyst should evaluate brackets and reweight premium rates to avoid losing revenue. 
-  Average ACA premiums over time out weighs inflation rates by a huge margin, and the biggest increase comes from Platinum and Gold plans, subsidies for shared cost across tiers does not balance out increase in premiums and might lead to plan holders seeking other avenues of insurance such as employee insurance as opposed to ACA plans. The government should adjust subsidies to reflect increase in premiums to avoid holders of lower tier plans from taking on the brunt of higher tier plan holders seeking out alternatives to ACA plans.
-  Geographic Variations will in plan premiums will discourage plan holders from fully commiting to ACA plan across all medical sectors, as the explosion of virtual health has opened other avenues of purchasing health care solutions over the internet, therefore plan holders are not limited to ACA plans bound by state lines and will compare and seek help with cheaper virtual options as opposed to fully subscribing to all healthcare options "vision, dental, prescription, mental health" avaiable through ACA to avoid cost. Insurers should compare alternative virtual cost options to knw and adjust to their competition to avoid losing revenue to virtual care programs.   

## 🛠️ Tools Used

-  Python (Pandas, NumPy)

-  Power BI

-  CMS Public Use Files

## 📌 Limitations

-  Analysis reflects filed rates, not actual enrollment-weighted costs.

-  Age-standardized to 30; results may differ for other age groups.

-  Does not totally account for subsidies, tax credits, inflation or plan selection behavior.

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

-  The Dashboard above was created using the final_plans_rates.csv file to encapsulate the full data spectrum. Python Script helped arrive at conclusions before Visualization began
  -  'Yearly Trend of Premiums' generated by using Measure for Average Yearly Premium against the years 2022 - 2026 
  -  'Average Yearly Premiums across Plan Tiers' Chart. generated by using Measure for Average Yearly Premium against the years using plan tiers as a legend 
  -  'Average Premium by state' generated by using Measure for Average Yearly Premium for the top 10 highest rates against their respective state codes
  -  'AVG PREMIUIM 2026' generated by filtering Average Yearly Premium to show only 2016
  -  'Filed Rate Records' KPI's generated by showing the count of plans in the merged table
  -  'Average Premium Per State 2026' Chart generated using the average Yearly Premium measure as a value of the Arc Gis chart with the state codes as the bubbles
  -  'Top 10 Issuers by Average Premium (22-26) generates using the Average Yearly Premium measure against the issuers and filtering for the top 10 values. 
  

-  Explore queries and modify filters for deeper analysis

### 📎 Author

[Dare Oyeleke]
Data Analyst | Healthcare Analytics
[(https://www.linkedin.com/in/dareoyeleke/)] | [(https://github.com/dareoyeleke)]
