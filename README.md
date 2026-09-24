# 🏠 Home Sales Analytics Dashboard | Excel

> **Interactive real-estate sales analytics dashboard built in Microsoft Excel using data cleaning, formula-driven analysis, KPI reporting, and executive-style visual storytelling.**

 ## Dashboard Preview 
 <img width="644" height="365" alt="Screenshot 2026-09-24 113019" src="https://github.com/user-attachments/assets/bf5c2c00-c16a-4c4a-b0c0-b5e6571c2405" />




## 📌 Project Overview

This project analyzes **250 residential property sales** across multiple neighborhoods, property types, conditions, bedroom categories, and monthly periods.

The workbook was designed as an end-to-end Excel analytics solution covering:

- Data preparation and cleaning
- Formula-driven KPI calculations
- Neighborhood and property-type analysis
- Monthly sales and pricing trends
- Price distribution analysis
- Size vs. price relationship
- Property-condition analysis
- Bedroom-level analysis
- Negotiation / sale-to-list analysis
- Outlier detection
- Correlation analysis
- Simple linear regression
- Executive dashboard storytelling

The dashboard is built so that the summary tables and visualizations are driven from the cleaned dataset rather than manually typed results.

---

## 🎯 Business Objective

The objective is to answer practical real-estate business questions such as:

1. How many homes were sold and what was the total sales volume?
2. What is the typical sale price?
3. Which neighborhoods command higher or lower prices?
4. Which property types contribute most to sales volume?
5. How quickly are homes selling?
6. How close are final sale prices to listing prices?
7. How does living area relate to sale price?
8. How does property condition relate to price and selling speed?
9. How is the market distributed across price bands?
10. Which observations should be treated cautiously as analytical outliers?

---

## 📊 Executive KPI Snapshot

| KPI | Result |
|---|---:|
| Homes Sold | **250** |
| Total Sales Volume | **$97.6M** |
| Median Sale Price | **$366,000** |
| Average Price / Sq Ft | **$226** |
| Average Days on Market | **57.4 days** |
| Average Sale-to-List | **97.5%** |
| Analysis Period | **1 Jan 2025 – 23 Aug 2026** |

---

## 🔎 Key Findings

### 1. Neighborhood pricing

| Neighborhood | Sales | Average Sale Price |
|---|---:|---:|
| Cedar Park | 39 | $285,641 |
| Downtown | 36 | $429,972 |
| Maple Heights | 51 | $336,588 |
| Oak Hill | 58 | $492,621 |
| Riverside | 62 | $383,145 |

Oak Hill has the highest average sale price in the dataset, while Cedar Park has the lowest among the named neighborhoods.

### 2. Property type mix

| Property Type | Sales | Share |
|---|---:|---:|
| Single Family | 146 | 58.4% |
| Condo | 57 | 22.8% |
| Townhouse | 47 | 18.8% |

Single-family homes account for the largest share of observed transactions.

### 3. Size and price relationship

Living area has a **strong positive correlation** with sale price in this dataset:

- Pearson correlation: **r ≈ 0.80**
- The workbook explicitly notes that correlation does **not** establish causation.
- After excluding rule-based analytical outliers, the simple linear model estimates roughly **$184 per additional sq ft**.
- Outlier-free model R²: **≈ 0.59**

This is a descriptive model for portfolio analysis, not a property valuation model.

### 4. Negotiation / sale-to-list behavior

- Average sale-to-list ratio: **97.5%**
- Approximately **19.2%** of sales closed above list
- Approximately **2.0%** closed exactly at list
- Approximately **78.8%** closed below list
- Average discount among below-list sales: approximately **$14.8K**

### 5. Property condition

Average sale prices vary meaningfully by condition:

| Condition | Sales | Average Sale Price |
|---|---:|---:|
| Excellent | 62 | $458,952 |
| Good | 105 | $372,629 |
| Fair | 60 | $360,083 |
| Poor | 11 | $317,818 |
| Unknown | 12 | $409,833 |

These are descriptive differences. They should not be interpreted as causal effects because other property characteristics can vary between groups.

---

## 🧮 Analytical Methodology

### Data preparation

The workbook contains both `Data_Raw` and `Data_Clean` layers.

The cleaned layer adds analytical fields including:

- Sale month
- Price per square foot
- Sale-to-list ratio
- Price difference vs. list
- Commission value
- Home age at sale
- Price band
- Outlier flag
- Cleaning notes

### Outlier detection

The workbook uses a **Tukey-style 1.5 × IQR rule** for:

- Sale price
- Days on market
- Price per square foot

Flagged records are **retained** in the dataset and labeled rather than deleted. This preserves traceability while allowing analytical comparisons with and without flagged observations.

### Statistical analysis

The `Analysis` sheet includes:

- Descriptive statistics
- Quartiles and IQR
- Outlier fences
- Pearson correlations
- Simple linear regression
- R²
- Standard error
- Price estimator
- Sale-to-list analysis
- Time-on-market segmentation

---

## 📈 Dashboard Pages

### Main Dashboard
Executive-level view containing:

- KPI cards
- Market insights
- Monthly trend
- Neighborhood performance
- Market mix
- Price distribution

### Drill-down 1 — Monthly Trend
Analyzes sales volume, average price, median price, and rolling trends over time.

### Drill-down 2 — Neighborhood Pricing
Compares neighborhood-level pricing, median vs. average, premium/discount, and price per square foot.

### Drill-down 3 — Speed & Negotiation
Explores days on market and sale-to-list performance by neighborhood.

### Drill-down 4 — Property Type
Compares condos, single-family homes, and townhouses across pricing, size, speed, and negotiation.

### Drill-down 5 — Price Distribution
Shows the number of transactions across sale-price bands and highlights distribution characteristics.

### Drill-down 6 — Size vs. Price
Uses scatter/regression analysis to explore the relationship between living area and sale price.

### Drill-down 7 — Condition
Compares price, size, selling speed, and negotiation metrics by property condition.

### Drill-down 8 — Bedrooms
Analyzes transaction volume, pricing, living area, and price per square foot by bedroom count.

---

## 🗂️ Workbook Architecture

```text
Home_Sales_Dashboard.xlsx
│
├── Dashboard
│   └── Executive dashboard and KPI cards
│
├── Pivots
│   └── Formula-driven summary tables
│
├── D1_Trend
├── D2_Neighborhood
├── D3_Speed_Negotiation
├── D4_Property_Type
├── D5_Price_Distribution
├── D6_Size_vs_Price
├── D7_Condition
├── D8_Bedrooms
│   └── Drill-down analysis pages
│
├── Analysis
│   └── Statistical analysis and regression
│
├── Cleaning_Log
│   └── Before/after data-quality documentation
│
├── Data_Clean
│   └── Analytics-ready dataset
│
└── Data_Raw
    └── Original raw dataset
```

---

## 🧰 Tools & Skills Demonstrated

**Excel**

- Advanced formulas
- SUMIFS / COUNTIFS
- AVERAGEIFS
- MEDIAN
- CORREL
- SLOPE / INTERCEPT
- RSQ
- STEYX
- QUARTILE
- INDEX / MATCH
- LOOKUP
- IF / IFERROR
- Dynamic dashboard text
- Named ranges
- Data validation
- Conditional formatting
- KPI design
- Interactive dashboard navigation
- Executive data storytelling

**Analytics**

- Descriptive statistics
- Segmentation
- Trend analysis
- Correlation analysis
- Regression
- Outlier detection
- Distribution analysis
- Pricing analysis
- Negotiation analysis

---

## 📁 Repository Structure

```text
home-sales-analytics-excel-dashboard/
│
├── Home_Sales_Dashboard.xlsx
│
├── assets/
│   └── dashboard-preview.png
│
├── data/
│   ├── home_sales_raw.csv
│   └── home_sales_clean.csv
│
├── docs/
│   └── data_dictionary.csv
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🚀 How to Use

### Option 1 — Explore the Excel dashboard

1. Download `Home_Sales_Dashboard.xlsx`.
2. Open it in Microsoft Excel.
3. Start from the `Dashboard` sheet.
4. Use the neighborhood and property-type selectors.
5. Navigate through the drill-down pages.
6. Review `Analysis` for statistical methodology.
7. Review `Cleaning_Log` to understand the data preparation process.

### Option 2 — Explore the data

The repository also contains:

- `data/home_sales_raw.csv`
- `data/home_sales_clean.csv`
- `docs/data_dictionary.csv`

These files make the project easier to inspect outside Excel.

---

## ⚠️ Important Notes

- The dataset is **synthetic**, created for analytics/dashboard demonstration.
- It should not be interpreted as a representation of a real housing market.
- The workbook retains analytical outliers rather than deleting them.
- Correlation does not imply causation.
- The regression model is a simple portfolio-analysis example and is **not** a professional property valuation model.
- The final August 2026 period is partial, with data ending on **23 Aug 2026**, so month-to-month comparisons involving August should be interpreted carefully.

---

## 💼 Portfolio Value

This project demonstrates an end-to-end workflow expected in practical Data Analyst / Business Analyst work:

**Raw Data → Cleaning → Data Quality → KPI Modeling → Statistical Analysis → Visualization → Dashboard → Business Insights**

It is particularly relevant for portfolios targeting:

- Data Analyst
- Business Analyst
- Reporting Analyst
- MIS Analyst
- BI Analyst
- Operations Analyst

---

## 👤 Author

**Aditya Kalyan**  
Data Analyst | Analytics Mentor

- LinkedIn: [Aditya Kalyan](https://www.linkedin.com/in/adityaakalyan/)
- GitHub: [Kalyan4636](https://github.com/Kalyan4636)
- Portfolio: [Data Science Portfolio](https://www.datascienceportfol.io/adityakalyanbscc)
- Mentorship: [Topmate](https://topmate.io/aditya_kalyan/)

---

## ⭐ If this project helps you

Consider starring the repository and sharing it with other aspiring Data Analysts.

**Built with Excel • Data Analytics • Statistical Thinking • Business Storytelling**
