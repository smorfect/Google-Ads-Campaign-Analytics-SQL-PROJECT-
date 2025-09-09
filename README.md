# Google-Ads-Campaign-Analytics-SQL-PROJECT

SQL-based end-to-end analysis of simulated Google Ads data — profiling, cleaning, anomaly detection, and multi-level performance insights with business recommendations.

## 1. Project Background & Overview  
This project simulates the role of a data analyst working with Google Ads campaign data for a **Data Analytics Course**.  
The dataset represents ad performance metrics (*impressions, clicks, conversions, costs, sales*) across **campaigns, locations, devices, and keywords**.  

The dataset used for this project is publicly available on Kaggle and can be accessed [here](https://www.kaggle.com/datasets/nayakganesh007/google-ads-sales-dataset).

The goal was to treat this dataset as if it were delivered by a business stakeholder and apply professional data analytics practices:  
- Profiling  
- Cleaning  
- Anomaly detection  
- Performance analysis  

The following are the key areas for gathering insights as they directly influence marketing ROI and business decision-making:  
- **Campaign Performance** → Identify which campaigns drive the most revenue & conversions.  
- **Location Effectiveness** → Highlight high-ROI geographies for budget allocation.  
- **Device Insights** → Assess Desktop vs. Mobile vs. Tablet efficiency to guide optimization.  
- **Keyword Analysis** → Evaluate which keywords bring the most qualified traffic.  
- **Time Trends** → Detect daily performance patterns & opportunities for scheduling/promotions.  

---

## 2. Objective  
The goal of this project was to analyze simulated Google Ads data for a Data Analytics Course campaign.  

Focus areas:  
- Profiled dataset for missing values, anomalies, and categorical consistency.  
- Cleaned and standardized campaign, location, device, and keyword fields; flagged quality issues.  
- Enriched dataset by simulating campaigns and redistributing locations for realistic variation.  
- Conducted multi-level SQL analysis (campaign, location, device, keyword, time, portfolio) and built a performance dashboard view.  

 A brief methodology can be found in [Technical Approach](Approach.md).

🔗 **SQL Scripts**  (available upon request or in interview)
- [Profiling & Data Quality Checks](#)  
- [Cleaning & Standardization](#)  
- [Analytical Queries (Campaigns, Locations, Devices, Keywords, Time Trends)](#)  

---

## 3. Data Structure and Initial Checks  
The dataset contains ~2,600 rows of ad-level records with details on campaign metadata, ad engagement, conversions, and revenue outcomes.  

**Key fields:**  
- `Ad_ID` → Unique identifier for each ad.  
- `Campaign_Name` → Name of the marketing campaign.  
- `Clicks` & `Impressions` → Engagement metrics.  
- `Cost` → Advertising spend.  
- `Leads` & `Conversions` → Outcomes generated.  
- `Conversion_Rate` → Efficiency metric (Conversions ÷ Clicks).  
- `Sale_Amount` → Revenue generated.  
- `Ad_Date` → Date when the ad was active.  
- `Location` → City where the ad was served (Hyderabad, Bengaluru, Gurgaon, Mumbai).  
- `Device` → Platform (Desktop, Mobile, Tablet).  
- `Keyword` → Search keyword that triggered the ad.  

<img width="1161" height="416" alt="image" src="https://github.com/user-attachments/assets/3697c558-ab0a-4aec-ad9f-f71de8ee4048" />

---

## 4. Executive Summary  

In November 2024, simulated Google Ads data for the Data Analytics Course campaigns was analyzed across 2,600 ad records. Overall portfolio performance was strong, delivering a Return on Ad Spend (ROAS) of 6.85, with more than 345K clicks generated from 11.5M impressions at an average CTR of 3.0%. 
The Beginners and Certification campaigns emerged as the top revenue drivers (₹750K each), while Advanced and Training – Online contributed slightly lower returns. At the city level, Gurgaon outperformed all markets with ROAS 7.07, followed by Bengaluru (6.83) and Mumbai (6.83), whereas Hyderabad lagged at 6.67 despite high volume. Device analysis revealed Desktop conversions (4.83%) slightly outpaced Mobile (4.77%) and Tablet (4.69%), with cost efficiency stable across both. Keyword-level insights highlighted “Online Data Analytics” and “Learn Data Analytics” as the top-performing drivers, each exceeding 2,800 conversions at ~3% CTR. Finally, time trend analysis showed revenue peaks on Nov 14 and Nov 25, aligning with likely campaign pushes, while dips on Nov 6, 11 and Nov 17 suggest delivery or targeting inefficiencies.

**Key takeaways:**  
- Campaigns are profitable overall (ROAS 6.85).  
- Beginners & Certification = key revenue drivers.  
- Gurgaon = most efficient market.  
- Desktop slightly outperforms Mobile and Tablet.  
- Top keywords drive majority of conversions.  
- **Next Steps**: Shift budget to Gurgaon + high-performing campaigns/keywords, optimize Hyderabad, and improve Mobile UX.  

<img width="1035" height="535" alt="image" src="https://github.com/user-attachments/assets/a77a33bf-ec13-458a-b11c-a418b3cc2a2c" />

<img width="975" height="445" alt="image" src="https://github.com/user-attachments/assets/e8928964-f42c-4756-98eb-6f5796f90b66" />

<img width="975" height="454" alt="image" src="https://github.com/user-attachments/assets/44dcfe87-020e-404c-a1fd-87febd337c0f" />

---

## 5. Insights Deep Dive & Recommendations  

### 5.1 Campaign Performance
*Which campaigns deliver the highest ROI?*

- Beginners & Certification = highest revenue (~₹750K each).  
- Advanced & Training = good but slightly lower ROI.  
- Conversion rates consistent (~4.6–4.9%).  

<img width="1005" height="536" alt="image" src="https://github.com/user-attachments/assets/312cff34-67aa-4ebd-bfcf-e8562972709a" />

**Recommendations:**  
- Keep investing in Beginners & Certification.  
- Refresh creatives for Advanced & Training.  
- Allocate ~10–15% test budget to Bootcamp.  

---

### 5.2 Location Effectiveness
*Which locations maximize revenue efficiency?*

- Gurgaon = strongest (ROAS 7.07).  
- Bengaluru & Mumbai stable (6.83).  
- Hyderabad underperformed (6.67).  

 <img width="931" height="538" alt="image" src="https://github.com/user-attachments/assets/c22399bb-4b4d-4f13-b837-c2a3e38e1c9f" />

**Recommendations:**  
- Reallocate incremental spend to Gurgaon.  
- Maintain investment in Bengaluru & Mumbai.  
- Audit Hyderabad campaigns (targeting/creative).  

---

### 5.3 Device Insights
*Do users convert better on Desktop, Mobile or Tablet?*

- Desktop (4.83% conversion rate) slightly outperformed Mobile (4.77%) and Tablet (4.69%).
- CPC and CPA were nearly identical across devices.


<img width="1022" height="537" alt="image" src="https://github.com/user-attachments/assets/1248ee94-853b-422c-9414-6c7be21028fd" />

**Recommendations:**  
- Maintain cross-device budget split.
- Optimize mobile landing pages.

---

### 5.4 Keyword Analysis
*Which keywords drive the most conversions?*

- Top keywords: *Online Data Analytics, Learn Data Analytics, Data Analytics Course* (>2.8K conversions).  
- CTR healthy at ~3%.  

<img width="1005" height="532" alt="image" src="https://github.com/user-attachments/assets/f5070648-ce6b-4f01-a3d5-4be44789ea41" />

**Recommendations:**  
- Expand around top-performing keywords.  
- Pause/refine weak long-tail keywords.  
- Add negative keywords to reduce wasted clicks.  

---

### 5.5 Time Trends 
*Are there specific days with unusually high or low performance?*

- Peaks: 14th & 25th Nov (highest conversions).  
- Dips: 6th, 11th & 17th Nov.

<img width="743" height="533" alt="image" src="https://github.com/user-attachments/assets/922b66fa-85d2-442b-bb51-8e0bae6b1645" />

**Recommendations:**  
- Replicate strategies from peak dates.  
- Review issues on low days.  

---

### 5.6 Portfolio-Level Efficiency
*What is the portfolio-wide efficiency across CTR, CPC, CPA, and ROAS?*

- CTR = **3.0%**  
- CPC = **₹1.56**  
- CPA = **₹32.69**  
- ROAS = **6.85** (very profitable)  

<img width="960" height="452" alt="image" src="https://github.com/user-attachments/assets/56e95f32-cfa3-4100-97c9-e56a98c8dd45" />

**Recommendations:**  
- Continue current bidding approach.  
- Test automated bidding to push ROAS > 7.  

---


