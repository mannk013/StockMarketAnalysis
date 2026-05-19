# 📈 Stock Price Analysis & Prediction

### End-to-end analysis using the OSEMN framework
**Author:** Michał Mańkowski  
**Stack:** Python, yfinance, Pandas, Scikit-learn, Matplotlib, Seaborn

---

## 📌 Project Overview
This project analyzes and predicts stock prices using 20 years of historical data from Yahoo Finance API. The analysis follows the **OSEMN framework** and compares multiple ML models for next-day price prediction across three major tech companies.

**Stocks analyzed:**
- 🍎 Apple Inc. (AAPL) ✅
- 🪟 Microsoft Corporation (MSFT) ✅
- 🔍 Google / Alphabet (GOOGL) ✅

---

## 📊 Final Results

| Stock | Model | MAE | R² |
|-------|-------|-----|----|
| 🍎 Apple (AAPL) | Linear Regression | $2.31 | 0.9935 |
| 🪟 Microsoft (MSFT) | Linear Regression | $4.24 | ~0.99 |
| 🔍 Google (GOOGL) | Linear Regression | $2.44 | 0.9974 |

**Winner across all stocks: Linear Regression** 🏆

---

## 🔍 Key Findings

### Three Stocks Comparison
| Metric | Apple (AAPL) | Microsoft (MSFT) | Google (GOOGL) |
|--------|-------------|-----------------|----------------|
| Avg daily return | +0.12% | +0.08% | +0.09% |
| Max single day gain | +15.33% | +18.60% | +19.99% |
| Max single day loss | -17.92% | -14.74% | -11.63% |
| Daily volatility | 1.79% | 1.74% | 1.87% |

### Investment Insights
- 🍎 **Apple** — most consistent daily returns, best for steady long-term growth
- 🪟 **Microsoft** — lowest volatility, best for risk-averse investors
- 🔍 **Google** — highest potential gains but most volatile

### Model Conclusion
Linear Regression outperforms all complex models (Random Forest, Gradient Boosting, KNN) across all three stocks. Stock prices follow a near-perfect linear pattern: **tomorrow's price ≈ today's price**.

---

## 🗺️ OSEMN Framework

### 🔵 O — Obtain
- Downloaded 20 years of stock data via **yfinance API**
- No manual data collection needed — fully automated

### 🧹 S — Scrub
- 0 missing values — clean datasets
- Feature engineering: Daily Returns, Moving Averages (50/200-day), Volatility

### 🔍 E — Explore
- Long-term upward trends confirmed for all three stocks
- Highest trading volume during **2008 financial crisis**
- Moving averages reveal Golden Cross and Death Cross patterns

### 🤖 M — Model
Trained and compared 4 ML models per stock:
- ✅ Linear Regression — winner
- ❌ Random Forest
- ❌ Gradient Boosting
- ❌ KNN

### 📊 N — Interpret
- Linear Regression is optimal for next-day stock price prediction
- Finding is consistent across Apple, Microsoft and Google

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
├── AppleStock.ipynb         ← Apple analysis
├── MicrosoftStock.ipynb     ← Microsoft analysis
├── GoogleStock.ipynb        ← Google analysis
└── README.md
```