# Portfolio Performance Reporting Tool

This project provides an automated reporting tool designed to give clients a clear, reliable, and digestible overview of their portfolio performance. The report, generated as a multi-page PDF document, pulls real-time financial data from Yahoo Finance, integrates quantitative analysis, and delivers professional-grade visualizations.

## 🔍 Project Objectives

- Help users, regardless of their financial expertise, understand their portfolio's evolution and risk exposure.
- Provide key industry metrics such as:
  - Absolute and relative returns (YTD, 1Y, 5Y)
  - Annualized volatility
  - Sharpe ratio
  - Tracking error
  - Value at Risk (95% VaR)
  - Max drawdown
  - Asset correlation matrices
- Enable benchmark comparisons using both numerical data and intuitive visuals (e.g., Risk vs Return with SML).

---

## 📁 Project Contents

- `projet_luca_hugo.py` – Main Python script
- `donnees_portefeuille.xlsx` – Excel input file (to be uploaded)
- `README.md` – Project documentation

---

## 🧠 Technical Approach

### Code Structure
The code is modular, with clearly separated responsibilities:
- Portfolio management
- PDF report generation
- Chart rendering
- GUI (Graphical User Interface)

A local cache system (`self.breakdown_cache`) helps optimize performance and readability.

### Documentation
Each function includes descriptive docstrings and follows consistent styling (snake_case, PEP8). Complex methods (e.g. for charts and risk metrics) include inline comments to aid understanding.

### Data Storage
Data is handled entirely in memory using `pandas` DataFrames and Python dictionaries. It’s optimized for small-to-medium portfolios. Future scaling could consider SQLite/PostgreSQL integration.

### Visualization Design
Charts include clear titles, legends, and intuitive layouts:
- Risk vs Return with SML
- Pie charts for sector/country allocation
- Cumulative return curves
- Correlation heatmaps

### Technical Challenges
- Managing incomplete/missing data from Yahoo Finance
- Dynamic multi-page PDF generation
- Robust handling of optional benchmark inputs

---

## 🖥️ Graphical Interface – User Guide

### Dashboard Tab
Displays:
- Asset list with quantity, buy/current price, return, and weight
- Optional benchmark input (e.g. `^GSPC`)
- Real-time position tracking

### Charts Tab
Includes:
- Asset/country/sector pie charts
- Cumulative return curves
- Sector allocation over time
- Risk vs Return with SML
- Correlation heatmaps and Sharpe ratio plots

### Transactions Tab
Features:
- Full transaction history (buy/sell)
- Manual entry form for new trades
- Automatic market price fetch via ticker

### Performance Tab
Displays:
- Key indicators: return, volatility, Sharpe, tracking error
- Benchmark-relative results
- Multi-period performance (YTD, 1Y, 5Y)

### Settings Tab
Lets users:
- Import a CSV portfolio file
- Set a benchmark
- Configure data refresh rate

### PDF Generation
Via the “Generate PDF” button (in Charts tab), users can export a 9-page report including:
- Portfolio summary
- Absolute and relative returns
- Risk metrics
- Allocation analysis
- Correlation charts
- Benchmark comparison

---

## 📌 Notes

- The Excel input file (`donnees_portefeuille.xlsx`) must be placed in the same folder as the Python script.
- Ensure a stable internet connection for real-time data via `yfinance`.

---

## ✅ Ready to Use

Once uploaded, your GitHub repository will serve as a complete project directory: code + input + documentation. Perfect for sharing with recruiters, collaborators, or using as a personal portfolio project.

