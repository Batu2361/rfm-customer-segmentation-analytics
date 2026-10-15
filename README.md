# 🇬🇧 English Version

# 📊 E-Commerce RFM Customer Segmentation & Revenue Analysis

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-Public-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

An end-to-end data analytics project categorizing over **5,800 e-commerce customers** into actionable business segments using **RFM (Recency, Frequency, Monetary)** modeling. The workflow integrates Python data preprocessing, SQL window functions, and an interactive Tableau Public executive dashboard.

🔗 **[🚀 Launch Interactive Tableau Dashboard](https://public.tableau.com/app/profile/batuhan.coglan/viz/E-CommerceRFMCustomerSegmentationRevenueAnalysis/Dashboard1?publish=yes)**

---

## 🖼️ Dashboard Preview

<div align="center">
  <img src="https://github.com/user-attachments/assets/f33b6ae1-9c38-48a4-80ff-f8b63d1bb73e" alt="E-Commerce RFM Dashboard Preview" width="100%">
</div>

---

## 🎯 Business Problem & Objectives

Retaining existing customers and mitigating churn is critical for sustainable e-commerce growth. This project addresses three primary business objectives:

1. **Maximize Customer Lifetime Value (CLV):** Identify high-value customers (*Champions*) to optimize VIP and loyalty programs.
2. **Proactive Churn Prevention:** Detect early warning signals (*At Risk / Retention Needed*) to enable targeted re-engagement campaigns.
3. **Revenue Dynamics Tracking:** Analyze historical revenue trends and seasonal patterns across customer segments from 2009 to 2011.

---

## 🛠️ Tech Stack & Methodology

| Layer | Tool / Tech | Purpose |
| :--- | :--- | :--- |
| **Data Processing** | `Python (Pandas, NumPy)` | Data cleaning, outlier handling, cancellation filtering, and metric calculation (`TotalSum`). |
| **Segmentation** | `SQL (SQLite)` | Aggregation via CTEs and quantile partitioning using `NTILE(5)` window functions. |
| **Visualization** | `Tableau Public` | Executive dashboard design with cross-filtering and action tables. |

### 🔄 Data Pipeline Architecture
1. **Raw Data Ingestion:** Sourced from Kaggle (`Online Retail II`).
2. **Preprocessing & Cleaning:** Removed missing `CustomerID`s, filtered canceled orders (`InvoiceNo` starting with 'C'), and validated total spend metrics.
3. **SQL RFM Scoring:** Calculated Recency (days since last order), Frequency (distinct invoices), and Monetary value (total spend). Assigned 1–5 scores via `NTILE(5)` and mapped scores to business segments.
4. **Dashboard Integration:** Joined transaction logs with customer profile segments in Tableau to enable multi-dimensional exploratory analysis.

---

## 📈 Key Insights & Strategic Recommendations

- **⭐ Champions Drive Top-Line Growth:** *Champions* account for the vast majority of peak revenue, reaching **~€1M in monthly spend** during Q4 holiday seasons.
- **🚨 Critical Churn Risk:** Over **800 customers** fall into the *At Risk / Retention Needed* segment. These historical big-spenders have been inactive for over 200 days.
- **🎯 Operational Actionability:** The embedded action table dynamically exposes target `CustomerID`s, enabling marketing teams to trigger automated win-back campaigns.

---

## 🚀 How to Reproduce

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/BatuhanCoglan/rfm-customer-segmentation-analytics.git](https://github.com/BatuhanCoglan/rfm-customer-segmentation-analytics.git)

```

2. **Extract Data & Run Notebook:**
* Unzip `cleaned_online_retail_II.csv.zip`.
* Open and execute `rfm_analysis.ipynb` in Jupyter Notebook or Google Colab.



---

## 📂 Repository Structure

```text
.
├── cleaned_online_retail_II.csv.zip   # Cleaned transactional data (compressed)
├── rfm_customer_segments.csv         # SQL-generated customer RFM scores & segments
├── rfm_analysis.ipynb                # End-to-end Python & SQL pipeline
├── dashboard_screenshot.png          # High-resolution dashboard preview
└── README.md                         # Project documentation

```





---

# 🇩🇪 Deutsche Version

# 📊 E-Commerce RFM Kunden-Segmentierung & Umsatzanalyse

Ein End-to-End Datenanalyse-Projekt zur Kategorisierung von über **5.800 E-Commerce-Kunden** in handlungsorientierte Geschäftssegmente mithilfe des **RFM-Modells (Recency, Frequency, Monetary)**. Der Workflow integriert die Datenaufbereitung in Python, SQL-Window-Funktionen und ein interaktives Executive-Dashboard in Tableau Public.

🔗 **[🚀 Interaktives Tableau Dashboard öffnen](https://public.tableau.com/app/profile/batuhan.coglan/viz/E-CommerceRFMCustomerSegmentationRevenueAnalysis/Dashboard1?publish=yes)**

---

## 🖼️ Dashboard Vorschau
<div align="center">
  <img src="https://github.com/user-attachments/assets/f33b6ae1-9c38-48a4-80ff-f8b63d1bb73e" alt="E-Commerce RFM Dashboard Preview" width="100%">
</div>
---

## 🎯 Geschäftsproblem & Zielsetzung

Die Bindung bestehender Kunden und die Reduzierung von Abwanderung (Churn) sind entscheidend für das e-Commerce-Wachstum. Dieses Projekt verfolgt drei zentrale Ziele:

1. **Customer Lifetime Value (CLV) maximieren:** Identifikation von Top-Kunden (*Champions*) zur Optimierung von Treueprogrammen.
2. **Proaktive Churn-Prävention:** Frühzeitiges Erkennen von Abwanderungsrisiken (*At Risk / Retention Needed*) für gezielte Reaktivierungskampagnen.
3. **Tracking der Umsatzdynamik:** Analyse historischer Umsatztrends und saisonaler Muster über verschiedene Kundensegmente hinweg (2009 bis 2011).

---

## 🛠️ Tech Stack & Methodik

| Ebene | Tool / Tech | Zweck |
| --- | --- | --- |
| **Data Processing** | `Python (Pandas, NumPy)` | Datenbereinigung, Entfernen von Ausreißern/Stornierungen und Berechnung der `TotalSum`. |
| **Segmentierung** | `SQL (SQLite)` | Aggregation via CTEs und Quantils-Klassifizierung mittels `NTILE(5)` Window-Funktionen. |
| **Visualisierung** | `Tableau Public` | Entwicklung eines Executive Dashboards mit Cross-Filtering und interaktiven Tabellen. |

### 🔄 Daten-Pipeline Architektur

1. **Rohdaten-Import:** Datensatz von Kaggle (`Online Retail II`).
2. **Preprocessing & Bereinigung:** Zeilen mit fehlenden `CustomerID`s entfernt, Stornos herausgefiltert (`InvoiceNo` beginnt mit 'C') und Umsatzmetriken validiert.
3. **SQL RFM Scoring:** Berechnung von Recency (Tage seit letztem Kauf), Frequency (Anzahl der Bestellungen) und Monetary (Gesamtumsatz). Zuweisung von 1–5 Scores via `NTILE(5)` und Mapping zu Geschäftssegmenten.
4. **Dashboard Integration:** Verknüpfung der Transaktionsdaten mit den Kundenprofilen in Tableau für die multidimensionale Analyse.

---

## 📈 Wichtige Erkenntnisse & Strategische Empfehlungen

* **⭐ Champions treiben den Umsatz:** Das Segment der *Champions* ist für den Großteil des Umsatzes verantwortlich und erreicht in der Weihnachtssaison (Q4) Peaks von **ca. 1 Mio. € Monatsumsatz**.
* **🚨 Kritisches Abwanderungsrisiko:** Über **800 Kunden** fallen in das Segment *At Risk / Retention Needed*. Diese ehemals umsatzstarken Kunden sind seit über 200 Tagen inaktiv.
* **🎯 Operative Handlungsfähigkeit:** Die integrierte Aktionstabelle liefert Marketing-Teams dynamisch die betroffenen `CustomerID`s, um sofort automatisierte Win-Back-Kampagnen (E-Mail/Rabatte) zu starten.

---

## 🚀 Reproduktion

1. **Repository klonen:**
```bash
git clone [https://github.com/BatuhanCoglan/rfm-customer-segmentation-analytics.git](https://github.com/BatuhanCoglan/rfm-customer-segmentation-analytics.git)

```


2. **Daten entpacken & Notebook ausführen:**
* Entpacke die Datei `cleaned_online_retail_II.csv.zip`.
* Öffne und starte `rfm_analysis.ipynb` in Jupyter Notebook oder Google Colab.



---

## 📂 Repository Struktur

```text
.
├── cleaned_online_retail_II.csv.zip   # Bereinigte Transaktionsdaten (komprimiert)
├── rfm_customer_segments.csv         # In SQL generierte RFM-Scores & Segmente
├── rfm_analysis.ipynb                # End-to-End Python & SQL Pipeline
├── dashboard_screenshot.png          # Hochauflösende Dashboard-Vorschau
└── README.md                         # Projekt-Dokumentation

```

---

## 👨‍💻 Autor

**Batuhan Cöglan**

* **Tableau Public:** [Profil](https://www.google.com/search?q=https://public.tableau.com/app/profile/batuhan.coglan)

```

```
