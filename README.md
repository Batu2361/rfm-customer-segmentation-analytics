# 📊 E-Commerce RFM Customer Segmentation & Revenue Analysis

An end-to-end data analytics project categorizing over 5,800 e-commerce customers into actionable segments using **RFM (Recency, Frequency, Monetary)** modeling. The analysis combines Python data cleaning, SQL query-based segmentation, and an interactive Tableau Public dashboard.

🔗 **[View Live Interactive Tableau Dashboard]([DEIN_TABLEAU_PUBLIC_LINK_HIER_EINFUEGEN](https://public.tableau.com/app/profile/batuhan.coglan/viz/E-CommerceRFMCustomerSegmentationRevenueAnalysis/Dashboard1?publish=yes))**

---

## 🎯 Business Problem & Objective
Retaining existing customers and mitigating churn is critical for e-commerce growth. The goal of this project is to:
1. Identify high-value customers (*Champions*) to maximize loyalty programs.
2. Detect churn risk early (*At Risk*) to enable targeted retention campaigns.
3. Track historical revenue trends across distinct customer segments from 2009 to 2011.

---

## 🛠️ Tech Stack & Methodology

- **Python (Pandas)**: Data cleaning, handling missing values, filtering canceled transactions, and feature engineering (`TotalSum`).
- **SQL (SQLite)**: Data aggregation using CTEs and statistical window functions (`NTILE(5)`) to compute RFM scores.
- **Tableau Public**: Executive dashboard design with dynamic interactive filtering.

### Data Pipeline Architecture
1. **Raw Data Ingestion**: Sourced from Kaggle (`Online Retail II`).
2. **Preprocessing**: Removed missing `CustomerID`s and handled returns/cancellations.
3. **SQL RFM Scoring**: Calculated Recency (days since last purchase), Frequency (distinct invoice count), and Monetary value (total spend). Segments assigned via `NTILE(5)` partitioning.
4. **Visualization**: Joined transaction-level cleaned data with RFM customer profiles in Tableau.

---

## 📈 Key Insights & Business Recommendations

- **Champions Drive Revenue**: *Champions* represent the majority of seasonal peaks, reaching nearly **€1M in monthly spend** during Q4 holiday seasons.
- **Proactive Churn Mitigation**: Over **800 customers** belong to the *At Risk / Retention Needed* segment. These customers previously generated significant revenue but show extended periods of inactivity (>200 days).
- **Targeted Action**: An embedded, dynamically filtered table provides marketing managers with specific `CustomerID` lists for automated re-engagement email campaigns.

---

## 🖼️ Dashboard Preview

<img width="1422" height="844" alt="dashboard_screenshot" src="https://github.com/user-attachments/assets/f33b6ae1-9c38-48a4-80ff-f8b63d1bb73e" />


---

## 📂 Repository Structure

├── cleaned_online_retail_II.csv.zip
├── rfm_customer_segments.csv
├── rfm_analysis.ipynb
├── dashboard_screenshot.png
└── README.md
