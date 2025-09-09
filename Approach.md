# Technical Approach

This project follows a structured, multi-step approach to ensure the dataset was cleaned, validated, enriched, and analyzed in a way that reflects real-world data analyst workflows.

---

## a) Data Profiling
- Counted total rows and validated column data types.  
- Checked date formats and ensured uniformity.  
- Identified missing values across numeric and categorical columns.  
- Performed distribution checks for numeric fields (min, max, ranges).  
- Assessed categorical consistency for campaign names, locations, devices, and keywords.

---

## b) Data Cleaning
- Standardized text categories (campaign names, devices, keywords, and locations).  
- Imputed missing numeric values:  
  - Null counts converted to zero where appropriate (e.g., clicks, impressions, conversions).  
  - Recalculated **Conversion Rate** dynamically instead of imputing.  
- Flagged suspicious records (e.g., `Conversions > 0` but `Sale_Amount = 0`).  
- Built a **Data Quality Dashboard** inside SQL to monitor anomalies such as:  
  - `Sale_Amount < Cost`  
  - `Clicks > Impressions`  
  - Conversions without revenue  

---

## c) Data Enrichment
- Applied **systematic partitioning** to split one campaign into multiple synthetic campaigns for richer variation.  
- Randomly redistributed locations across four cities (Hyderabad, Bengaluru, Gurgaon, Mumbai) to simulate realistic geographic spread.  

---

## d) Analysis
- Conducted multi-level SQL analysis across key business areas:  
  - **Campaign performance** → clicks, conversions, revenue, conversion rate.  
  - **Location effectiveness** → ROAS by city.  
  - **Device insights** → conversion efficiency, CPC, CPA.  
  - **Keyword performance** → CTR and conversions by keyword.  
  - **Time trends** → daily impressions, clicks, conversions, revenue.  
  - **Portfolio-level metrics** → CTR, CPC, CPA, ROAS.  
- Created a **Performance Dashboard View** in SQL for ongoing monitoring of KPIs across campaigns, locations, and devices.  

---
