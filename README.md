# Forecasting Exchange Rate Volatility: A Multivariate Stacked LSTM with Attention

This repository contains the complete codebase and resources for the final project report, **"Forecasting Exchange Rate Volatility: A Multivariate Stacked LSTM model with Attention mechanism"**.

The project implements a deep learning approach to forecast the **21-day annualized realized volatility ($RV_d$)** of the USD/INR exchange rate, benchmarking its performance against classical econometric models, including GARCH(1,1), GJR-GARCH(1,1), and the Heterogeneous Autoregressive Realized Volatility (HAR-RV) model.

---

## 🚀 How to Reproduce Results

To fully reproduce the empirical findings, figures, and tables presented in the accompanying project report, follow these steps:

1. **Clone the Repository**
    ```bash
    git clone [https://github.com/jayarammovva9/Forecasting-Exchange-Rate-Volatility.git](https://github.com/jayarammovva9/Forecasting-Exchange-Rate-Volatility.git)
    cd Forecasting-Exchange-Rate-Volatility
    ```

2. **Set Up the Environment**
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Analysis**
    Open `main_analysis.ipynb` in Google Colab or a local Jupyter environment.  
    Run all cells from top to bottom. The notebook loads the dataset and generates all figures/tables.

---

## 📊 Data Card

The models are trained on a multivariate time series dataset combining daily market data with macroeconomic indicators from 2007 to 2025.

| Variable | Source | Type | Frequency | Missing % | Notes / Leakage Risk |
| :--- | :--- | :--- | :--- | :--- | :--- |
| CPI | FRED (guess) | float64 | Monthly (likely ffilled to daily)| 0.00 | Forward-filled daily. |
| OIL\_WTI | Yahoo Finance (guess)| float64 | Daily | 0.00 | No leakage. |
| RV\_d | Self-Calculated (guess) | float64 | Daily | 0.00 | Lagged, no leakage risk. |
| SP500 | Yahoo Finance (guess) | float64 | Daily | 0.00 | No leakage. |
| US\_10Y\_YIELD | FRED (guess) | float64 | Daily | 0.00 | ffill used for holidays. |
| USDINR | Yahoo Finance (guess)| float64 | Daily | 0.00 | Used to create target. |
| VIX | Yahoo Finance (guess)| float64 | Daily | 0.00 | No leakage. |

---

## 🗓️ Data Split

The study employs a rigorous **Walk-Forward Validation** scheme to ensure temporal robustness.

| Split | Date Range | Rows | % of Data | Notes |
| :--- | :--- | :--- | :--- | :--- |
| Train | 2007-09-17 $\to$ $\sim$2023-??-?? | 3765 | 80\% | Chronological; no leakage |
| Validation | inside Train | $\sim$565 | 15\% of Train | Used for early stopping |
| Test | $\sim$2023-??-?? $\to$ 2025-10-01 | 942 | 20\% | Strictly future unseen data |

---

## 🛠️ Modeling Approach

The core model is a **Multivariate Stacked LSTM network integrated with an Attention Mechanism**. This architecture is designed to capture non-linear, hierarchical temporal dependencies in volatility data and dynamically weigh the importance of past time steps.

The model's performance is rigorously benchmarked against established econometric models, including GARCH(1,1), GJR-GARCH(1,1), and the HAR-RV model.

---

## 📄 Contact

For any questions or detailed documentation regarding the methodology or results, please contact the authors:

* **Email:** \{chaganty.saianirudh25b, gaurav.nautiyal25b, jayaram.movva25b\}@gim.ac.in
