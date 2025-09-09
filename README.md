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
- **Device Insights** → Assess Desktop vs. Mobile efficiency to guide optimization.  
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
In **November 2024**, simulated Google Ads data (2,600 ad records) was analyzed.  

**Portfolio results:**  
- ROAS = **6.85** (profitable)  
- Impressions = **11.5M**, Clicks = **345K**, CTR = **3.0%**  

**Highlights:**  
- **Campaigns** → *Beginners & Certification* campaigns drove ~₹750K each; Advanced & Training slightly lower.  
- **Locations** → *Gurgaon (ROAS 7.07)* led; Bengaluru & Mumbai stable (6.83); Hyderabad underperformed (6.67).  
- **Devices** → *Desktop (4.83% CR)* slightly ahead of Mobile (4.77%).  
- **Keywords** → *“Online Data Analytics”* & *“Learn Data Analytics”* delivered >2.8K conversions each.  
- **Time Trends** → Peaks on *Nov 14 & 18* (highest conversions); dips on *Nov 11 & 17*.  

**Key takeaways:**  
- Campaigns are profitable overall (ROAS 6.85).  
- Beginners & Certification = key revenue drivers.  
- Gurgaon = most efficient market.  
- Desktop slightly outperforms Mobile.  
- Top keywords drive majority of conversions.  
- **Next Steps**: Shift budget to Gurgaon + high-performing campaigns/keywords, optimize Hyderabad, and improve Mobile UX.  

<img width="975" height="475" alt="image" src="https://github.com/user-attachments/assets/37fb2235-f04e-412e-a23e-4f9936f41728" />

<img width="975" height="445" alt="image" src="https://github.com/user-attachments/assets/e8928964-f42c-4756-98eb-6f5796f90b66" />

<img width="975" height="454" alt="image" src="https://github.com/user-attachments/assets/44dcfe87-020e-404c-a1fd-87febd337c0f" />

---

## 5. Insights Deep Dive & Recommendations  

### 5.1 Campaign Performance 
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
- Desktop CR = 4.83%, Mobile CR = 4.77%.  
- CPC & CPA stable across both.  

<img width="1022" height="537" alt="image" src="https://github.com/user-attachments/assets/1248ee94-853b-422c-9414-6c7be21028fd" />

**Recommendations:**  
- Maintain cross-device budget split.
- Optimize mobile landing pages.

---

### 5.4 Keyword Analysis
- Top keywords: *Online Data Analytics, Learn Data Analytics, Data Analytics Course* (>2.8K conversions).  
- CTR healthy at ~3%.  

<img width="1005" height="532" alt="image" src="https://github.com/user-attachments/assets/f5070648-ce6b-4f01-a3d5-4be44789ea41" />

**Recommendations:**  
- Expand around top-performing keywords.  
- Pause/refine weak long-tail keywords.  
- Add negative keywords to reduce wasted clicks.  

---

### 5.5 Time Trends 
- Peaks: Nov 14 & Nov 18 (highest conversions).  
- Dips: Nov 11 & Nov 17.  

<img width="669" height="537" alt="image" src="https://github.com/user-attachments/assets/31e7d9c5-39e1-42b2-a677-a40fa4489a16" />

**Recommendations:**  
- Replicate strategies from peak dates.  
- Review issues on low days.  

---

### 5.6 Portfolio-Level Efficiency
- CTR = **3.0%**  
- CPC = **₹1.56**  
- CPA = **₹32.69**  
- ROAS = **6.85** (very profitable)  

<img width="960" height="452" alt="image" src="https://github.com/user-attachments/assets/56e95f32-cfa3-4100-97c9-e56a98c8dd45" />

**Recommendations:**  
- Continue current bidding approach.  
- Test automated bidding to push ROAS > 7.  

---


