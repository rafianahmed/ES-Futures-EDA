# 📊 S&P 500 Futures (ES) Predictive Modeling Project

## 📌 Overview
This project develops a predictive modeling pipeline to analyze and forecast short-term price movements in S&P 500 E-mini Futures (ES=F).

The objective is to:
- Understand market predictability
- Evaluate linear regression performance
- Extract insights from engineered features

---

## 📂 Data Source
- Source: Yahoo Finance
- Instrument: ES=F (E-mini S&P 500 Futures)
- Data: Open, High, Low, Close, Volume

Collected using Python (yfinance).

---

## ⚙️ Methodology

### Feature Engineering
- Lagged returns (lag1, lag2, lag3)
- Price features (range %, open-close %)
- Volatility (5-day, 10-day)
- Trend (SMA gap)
- Volume change
- Weekday effect

### Target
Next-day return prediction:
(P_t+1 - P_t) / P_t

### Model
- Multiple Linear Regression (OLS)
- Implemented using scikit-learn

---

## 📊 Key Findings

### 1. Low Predictability
Short-term returns are highly noisy and difficult to predict.

### 2. Weak Lag Effects
Lagged returns show minimal predictive power with slight mean reversion.

### 3. Volatility Matters
Model performance degrades during high volatility regimes.

### 4. Trend Signals Help
SMA-based features provide relatively stronger signals.

### 5. Volume is Noisy
Volume features introduce instability and weak predictive value.

### 6. Minor Weekday Effects
Small behavioral patterns exist but are not strong predictors.

---

## 🚨 Key Insight
Linear models fail to capture nonlinear dependencies in financial markets.

---

## 📉 Limitations
- Linear assumptions
- No regime detection
- No nonlinear modeling


## 🧠 Conclusion
Financial markets are near-efficient at short horizons, requiring advanced models for meaningful prediction.
