# Bursa Malaysia: ESG vs. Market Benchmark Performance Analysis

---

## 📊 Project Overview
This project evaluates the financial trade-offs of **ESG (Environmental, Social, and Governance)** investing within **Bursa Malaysia**. By comparing constituents of the **FTSE4Good Bursa Malaysia (F4GBM)** index against the **FBM KLCI 30** benchmark, this study identifies whether "Green" companies offer superior risk-adjusted returns.

---

## 📌 Executive Summary (Key Findings)

- ESG portfolios underperformed the FBM KLCI 30 by **-0.61%** in cumulative returns over the study period.
- Despite the performance gap, ESG constituents demonstrated **lower average volatility**, confirming their role as a **risk-mitigating investment strategy**.
- **Finance and Healthcare** sectors exhibited the strongest ESG integration, maintaining higher **Sharpe Ratios** during market fluctuations.
- Results suggest ESG investing in Malaysia currently functions more as a **defensive allocation** rather than a primary growth driver.

---

## 📊 Dashboard Walkthrough

The Power BI report consists of three analytical layers:

1. **Performance Benchmarking**
   - Compares cumulative returns of ESG vs benchmark constituents.
   - Highlights long-term growth divergence and relative underperformance.

2. **Risk-Adjusted Efficiency**
   - Visualizes Annualized Volatility and Sharpe Ratio by sector.
   - Identifies which sectors deliver the highest return per unit of risk.

3. **Strategic Insights**
   - Sector-level ESG effectiveness summary.
   - Designed for decision-makers evaluating ESG allocation trade-offs.

---

## 🚀 Key Features
- **Comprehensive Universe:** Analysis of 40+ companies across all 13 official Bursa Malaysia sectors (Financials, Energy, Tech, etc.).
- **Automated Pipeline:** Custom Python data pipeline using `yfinance` to pull 5+ years of daily historical data.
- **Financial Engineering:** Automated calculation of **Cumulative Returns** and **Annualized Volatility (Risk)** using Pandas.
- **2026 Ready:** Includes the latest January 2026 index constituent updates (e.g., Capital A Berhad, Ajinomoto).

---

## 🛠️ Tech Stack
- **Data Acquisition:** Python (`yfinance`, `pandas`)
- **Data Engineering:** Power Query / M (Merge Queries, Null Handling, Data Categorization)
- **Visualization:** Power BI, DAX (Data Analysis Expressions)
- **Source Control:** Git / GitHub (Using .pbip for text-based versioning)

---

## 📂 Project Structure
```text
bursa-malaysia-esg-analysis/
├── ESG_Bursa_Analytics.pbip           <-- Master Project Entry Point
├── ESG_Bursa_Analytics.SemanticModel/ <-- DAX Logic & Schema (model.bim)
├── ESG_Bursa_Analytics.Report/        <-- Visual Layout & Themes (report.json)
├── data/
│   ├── raw/                           <-- 5-year historical price data & company details (CSV)
│   ├── processed/                     <-- processed data (CSV)
│   └── mapping_table.csv              <-- Sector & ESG Group metadata
└── README.md                          <-- Project Documentation
```

---

## 🧠 Quantitative Implementation
To provide a true "Risk vs. Reward" comparison, the following financial engineering was implemented via DAX:
1. **Annualized Volatility (Risk)**
```math
Volatility\ Risk = STDEV.S(Daily\ Returns) * sqrt{252}
```
Used to measure the "bumpiness" of stock price movements over the study period.

2. **Sharpe Ratio (Efficiency)**
```math
Sharpe\ Ratio = \frac{Average\ Cumulative\ Return}{Volatility\ Risk}
```
Identified which sectors provided the highest return for every unit of risk taken. Finance and Tech emerged as efficiency leaders.

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

---

## ⚠️ Limitations & Future Improvements

- ESG classification is index-based and does not capture firm-level ESG scoring granularity.
- No factor regression (e.g., CAPM, Fama-French) was applied in the current phase.
- Future iterations may include:
  - Risk-free rate–adjusted Sharpe Ratio
  - Rolling volatility windows
  - ESG score weighting instead of binary classification
  - Live market data integration

---

**How to Run:**
1. Ensure you have the latest version of Power BI Desktop installed.
2. Clone this repository.
3. Open the ESG_Bursa_Analytics.pbip file to launch the project.