# Bursa Malaysia: ESG vs. Market Benchmark Performance Analysis

---

## 📊 Project Overview
This project is a data analytics study exploring the relationship between **ESG (Environmental, Social, and Governance)** compliance and financial performance within the Malaysian stock market (**Bursa Malaysia**). 

The goal is to determine if companies recognized for high sustainability standards (constituents of the **FTSE4Good Bursa Malaysia Index**) exhibit better returns or lower volatility compared to the broader market benchmark (**FBM KLCI 30**).

---

## 🚀 Key Features
- **Comprehensive Universe:** Analysis of 40+ companies across all 13 official Bursa Malaysia sectors (Financials, Energy, Tech, etc.).
- **Automated Pipeline:** Custom Python data pipeline using `yfinance` to pull 5+ years of daily historical data.
- **Financial Engineering:** Automated calculation of **Cumulative Returns** and **Annualized Volatility (Risk)** using Pandas.
- **2026 Ready:** Includes the latest January 2026 index constituent updates (e.g., Capital A Berhad, Ajinomoto).

---

## 🛠️ Tech Stack
- **Data Acquisition:** Python (`yfinance`, `pandas`)
- **Data Engineering:** Python (`numpy`)
- **Visualization:** [Power BI / Tableau] - *In Progress*
- **Source Control:** Git / GitHub

---

## 📂 Project Structure
```text
bursa-malaysia-esg-analysis/
├── data/
│   ├── raw/            <-- Original 5-year historical price data (CSV)
│   └── processed/      <-- Cleaned "Long-Format" data with return/risk metrics
├── scripts/
│   ├── data_pull.py    <-- Script for automated data acquisition
│   └── data_cleaning.py <-- Script for "Melting" and metric calculations
├── README.md           <-- Project Documentation
└── .pbix    <-- Power BI Dashboard (Upcoming)
```

---

## 📈 Data Dictionary (Processed Data)

| Column | Description |
| :--- | :--- |
| **Date** | Trading date (YYYY-MM-DD) |
| **Ticker** | Official Bursa Malaysia code (e.g., 1155.KL) |
| **Cumulative_Return** | % Change in stock price since January 2021 |
| **Sector** | One of the 13 official Bursa industry classifications |
| **ESG_Group** | Flag identifying if the company is in the F4GBM Index |
| **Benchmark_Group** | Flag identifying if the company is in the KLCI 30 Index |
| **Volatility_Risk** | Annualized standard deviation of daily returns |

## 🧠 Key Insights (Phase 2 Results)
* **Data Transformation**: Successfully "unpivoted" 40 columns of stock prices into a 50,000+ row "Long-Format" dataset optimized for BI tool performance.

* **Sector Diversification**: Mapped a balanced portfolio representing the entire Malaysian corporate landscape.

* **Risk Metrics**: Implemented annualized volatility calculations to compare the "safety" of ESG stocks versus traditional giants.

---

**Next Steps**: Developing the interactive dashboard to visualize these trends and identify "Green Alpha" in the Malaysian market.