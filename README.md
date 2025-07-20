# Comprehensive-COVID-19-Analysis-by-WHO-Region

**📘 Project Overview**

  This project presents an interactive Power BI dashboard offering a comprehensive analysis of COVID-19 cases and deaths categorized by WHO regions. The goal was to understand the global and regional impact of the pandemic using visual storytelling and key performance metrics.

**🌍 Dataset Summary

**Source:** https://www.kaggle.com/datasets/imdevskp/corona-virus-report?select=country_wise_latest.csv

**Time Period:** Week-based data from early 2020 to 2023

**Granularity:** Weekly aggregated

**Regions Analyzed:**

  - Africa

  - Americas

  - Eastern Mediterranean

  - Europe

  - South-East Asia

  - Western Pacific

**⚙️ Project Workflow**

1. <ins>Data Import & Cleaning</ins>

  - Loaded data into Power BI

  - Removed null or blank records

  - Transformed date column into week number for time-based analysis

  - Standardized WHO region names

  - Ensured numerical fields like new_cases and new_deaths were in correct format

2. <ins>Data Modeling</ins>

  - Created relationships between date, region, and metrics

  - Added calendar table to support weekly analysis and filtering

  - Introduced calculated columns for week number generation:

        DAX
        Week Number = WEEKNUM('Date Table'[Date], 2)
    
3. <ins>DAX Measures Created</ins>
Key DAX measures were built to provide dynamic insights:

       DAX
       Total Cases = SUM('COVID'[new_cases])
       Total Deaths = SUM('COVID'[new_deaths])
       CFR (Case Fatality Rate) = DIVIDE([Total Deaths], [Total Cases])
   
Other metrics include:

   - Total Cases (Region-wise & Global)

   - Total Deaths

   - CFR %

   - Weekly Case Trends

   - Peak Week Identifiers

4. <ins>Power BI Visuals & Layout</ins>

   - Line Chart - Weekly trend of COVID-19 cases by WHO region

   - Stacked Bar Chart -	Regional comparison of total cases and deaths

   - Pie/Donut Chart	- Case Fatality Rate (CFR%) by region

   - Map Visual	- Heatmap showing case intensity across countries

   - Card KPIs	- Total Global Cases, Deaths, and CFR

   - Slicer - Week number filter to analyze specific timeframes

🔹 No exact date field used – visualizations rely entirely on week numbers for time slicing.

**📌 Key Features & Insights**

📈 Dynamic Weekly Trend analysis by WHO Region

🌐 Global Overview of total cases, deaths, and fatality rates

🧭 Drill-down functionality for region-wise trends

⚙️ Clean UI with region-based color consistency

🔎 Slicer to control Week Number and view specific peaks or troughs

**🛠 Tools & Technologies Used**

   - Power BI – Dashboard development and data modeling

   - DAX – Dynamic calculations and KPI measures

   - Excel / CSV – Data cleaning and structure

   - WHO API / Public CSVs – Data source

**📍 Conclusion**

This dashboard enables users to monitor, compare, and analyze the progression of COVID-19 across various WHO regions without relying on exact dates. It is ideal for public health analysts, researchers, and policymakers seeking clear weekly trends and region-specific insights.
