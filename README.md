# Forecasting USD/INR Volatility
*A Multivariate Stacked LSTM + Attention benchmarked against HAR-RV and GARCH family*

---

## Overview
This repository contains code, data, and notebooks to forecast **USD/INR realized volatility** using a **Stacked LSTM with an Attention layer**. We benchmark deep learning against **HAR-RV**, **GARCH(1,1)**, and **GJR-GARCH(1,1)** and assess both **statistical** and **economic** significance (via a hedging simulation).

**Highlights**
- Multivariate inputs: USD/INR, VIX, WTI crude, gold, S&P 500, U.S. Treasury yields (3M/1Y/10Y), and India CPI  
- Target: 21-day annualized realized volatility of USD/INR log returns  
- Evaluation: chronological 80/20 split **plus** 14-fold **walk-forward validation** (≈66 trading days/fold)  
- Results (test): HAR-RV RMSE **0.0048**, Stacked LSTM+Attn **0.0053** (statistically comparable), both outperform GARCH family  
- Hedging simulation: **≥83% decision accuracy** for HAR-RV and Stacked LSTM+Attn

---

## Repository Structure
