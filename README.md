# 📈 Stock Price Analysis & Prediction

### End-to-end analysis using the OSEMN framework
**Author:** Michał Mańkowski  
**Stack:** Python, yfinance, Pandas, Scikit-learn, Matplotlib, Seaborn

---

## 📌 Project Overview
This project analyzes and predicts stock prices using 20 years of historical data from Yahoo Finance API. The analysis follows the **OSEMN framework** and compares multiple ML models for next-day price prediction.

**Stocks analyzed:**
- 🍎 Apple Inc. (AAPL) — complete analysis
- 🪟 Microsoft (MSFT) — coming soon
- 🔍 Google (GOOGL) — coming soon

---

## 🗺️ OSEMN Framework

### 🔵 O — Obtain
- Downloaded 20 years of stock data via **yfinance API**
- No manual data collection needed — fully automated

### 🧹 S — Scrub
- 0 missing values — clean dataset
- Feature engineering: Daily Returns, Moving Averages, Volatility

### 🔍 E — Explore
- Long-term upward trend confirmed
- Highest trading volume during **2008 financial crisis**
- Average daily return: **+0.12%**
- Max single day gain: **+15.33%** | Max loss: **-17.92%**

### 🤖 M — Model
Trained and compared 4 ML models:

| Model | MAE | R² |
|-------|-----|----|
| **Linear Regression** | **$2.31** | **0.9935** |
| Random Forest | $36.67 | -0.50 |
| Gradient Boosting | $38.73 | -0.63 |
| KNN | $109.32 | -7.23 |

### 📊 N — Interpret
- **Linear Regression wins** — stock prices follow near-perfect linear pattern
- Complex models overfit to noise rather than learning the trend
- Apple is one of the most predictable and consistently growing assets

---

## 💡 Key Findings
- Apple stock grew consistently over 20 years with cyclical dips
- Tomorrow's price ≈ today's price — simple models outperform complex ones
- Highest volatility during **2008 crisis** and **COVID-2020**

---

## 🛠️ Tech Stack
- **Python 3.13**
- **yfinance** — stock data API
- **Pandas, NumPy** — data manipulation
- **Matplotlib, Seaborn** — visualizations
- **Scikit-learn** — ML models

---

## 🚀 How to Run

```bash
git clone https://github.com/YOUR_USERNAME/stock_analysis
cd stock_analysis
pip install pandas numpy matplotlib seaborn scikit-learn yfinance
jupyter notebook
```

---

## 📁 Project Structure
```
stock_analysis/
│
├── apple_analysis.ipynb      ← Complete analysis
├── microsoft_analysis.ipynb  ← Coming soon
├── google_analysis.ipynb     ← Coming soon
└── README.md
```