# 📈 Stock Price Analysis & Prediction

### End-to-end analysis using the OSEMN framework
**Author:** Michał Mańkowski  
**Stack:** Python, yfinance, Pandas, Scikit-learn, Matplotlib, Seaborn

---

## 📌 Project Overview
This project analyzes and predicts stock prices using 20 years of historical data from Yahoo Finance API. The analysis follows the **OSEMN framework** and compares multiple ML models for next-day price prediction.

**Stocks analyzed:**
- 🍎 Apple Inc. (AAPL) — complete analysis
- 🪟 Microsoft Corporation (MSFT) — complete analysis
- 🔍 Google (GOOGL) — coming soon

---

## 📊 Results Summary

| Stock | Model | MAE | R² |
|-------|-------|-----|----|
| 🍎 Apple (AAPL) | Linear Regression | $2.31 | 0.9935 |
| 🪟 Microsoft (MSFT) | Linear Regression | $4.24 | ~0.99 |

---

## 🔍 Key Findings

### Apple vs Microsoft Comparison
| Metric | Apple (AAPL) | Microsoft (MSFT) |
|--------|-------------|-----------------|
| Avg daily return | +0.12% | +0.08% |
| Max single day gain | +15.33% | +18.60% |
| Max single day loss | -17.92% | -14.74% |
| Daily volatility | 1.79% | 1.74% |

### Model Findings
- **Linear Regression wins** across both stocks — stock prices follow a near-perfect linear pattern
- Complex models (Random Forest, KNN, Gradient Boosting) fail badly due to extrapolation issues
- This finding is **consistent across different companies** — confirming the pattern

### Stock Insights
- **Apple** — consistent growth since 2005, acceleration post-2020
- **Microsoft** — flat 2005-2015 under Ballmer, explosive growth post-2015 under Nadella's cloud strategy

---

## 🗺️ OSEMN Framework

### 🔵 O — Obtain
- Downloaded 20 years of stock data via **yfinance API**
- No manual data collection needed — fully automated

### 🧹 S — Scrub
- 0 missing values — clean datasets
- Feature engineering: Daily Returns, Moving Averages (50/200-day), Volatility

### 🔍 E — Explore
- Long-term upward trends confirmed for both stocks
- Highest trading volume during **2008 financial crisis**
- Moving averages reveal Golden Cross and Death Cross patterns

### 🤖 M — Model
Trained and compared 4 ML models per stock:
- Linear Regression ✅
- Random Forest ❌
- Gradient Boosting ❌
- KNN ❌

### 📊 N — Interpret
- Linear Regression is optimal for next-day stock price prediction
- Tomorrow's price ≈ today's price — simple models outperform complex ones

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