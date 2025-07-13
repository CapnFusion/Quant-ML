# Quant-ML-Profnitt
# Volatility Prediction 

This repository contains my submission for the **Phase 2 task** of the **Quant domain** for ProfNITT Club, NIT Trichy.

---

## Objective

Predict the **future 5-day volatility** of a stock/index (NIFTY 50 in this case), using historical price data and engineered features like technical indicators, volume trends, and past volatility.

---

##  Dataset

- Pulled using `yfinance` API
- Stock index used: **NIFTY 50 (`^NSEI`)**
- Time range: **2020-01-01 to 2024-12-31**

---

##  Features Engineered

- **Technical Indicators**:
  - SMA (Simple Moving Average)
  - EMA (Exponential Moving Average)
  - RSI (Relative Strength Index)
  - MACD and Signal Line
  - Bollinger Band Width

- **Volume-based / Custom Features**:
  - Volume
  - Log Returns
  - Previous 5-day rolling volatility
  - 5-day future volatility (used as target)

---

## Approach

1. **Cleaned** the dataset (missing values handled using forward fill)
2. Created **multiple features** (technical indicators + lagged values)
3. Split into train-test without shuffling (because it’s time series)
4. Trained 3 models:
   - Linear Regression using sklearn
   - Random Forest Regressor
   -  **Linear Regression from scratch** (Normal Equation) (Bonus Task)
5. Compared model performance using R² score and visual plots

---

##  Results

| Model | R² Score |
|-------|----------|
| Linear Regression (sklearn) | -0.31 |
| Random Forest | ~0.62 |
| Scratch Linear Regression | **0.76**

---

##  Plots & Analysis

- RSI, MACD, Bollinger Band Width charts
- Feature Importance plot (Random Forest)
- Actual vs Predicted plot for scratch model

Key insight:  
- Volatility is **autocorrelated**, and even simple models can perform well with clean features.

---

##  Files

| File | Description |
|------|-------------|
| `QuantML` | Final Colab notebook |
| `Google Colab Link` | Link for the colab itself |
| `README` | You’re reading it  |

---



