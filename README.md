## How to Reproduce Results







1. **Clone the Repository**



    ```bash



    git clone https://github.com/jayarammovva9/Forecasting-Exchange-Rate-Volatility.git



    cd Forecasting-Exchange-Rate-Volatility



    ```







2. **Set Up the Environment**



    ```bash



    pip install -r requirements.txt



    ```







3. **Run the Analysis**



    Open `main_analysis.ipynb` in Google Colab or a local Jupyter environment.  



    Run all cells from top to bottom. The notebook loads the dataset and generates all figures/tables.



## Data Card

| Variable        | Source                 | Type    | Frequency                         | Missing % | Notes / Leakage Risk     |
|-----------------|------------------------|---------|------------------------------------|-----------|--------------------------|
| CPI             | FRED (guess)           | float64 | Monthly (likely ffilled to daily)  | 0.00      | Forward-filled daily     |
| OIL_WTI         | Yahoo Finance (guess)  | float64 | Daily                              | 0.00      | No leakage               |
| RV_d            | Self-Calculated (guess)| float64 | Daily                              | 0.00      | Lagged; no leakage risk  |
| SP500           | Yahoo Finance (guess)  | float64 | Daily                              | 0.00      | No leakage               |
| US_10Y_YIELD    | FRED (guess)           | float64 | Daily                              | 0.00      | ffill used for holidays  |
| USDINR          | Yahoo Finance (guess)  | float64 | Daily                              | 0.00      | Used to create target    |
| VIX             | Yahoo Finance (guess)  | float64 | Daily                              | 0.00      | No leakage               |

---

## Data Split

| Split       | Date Range                | Rows | % of Data     | Notes                             |
|-------------|---------------------------|------|---------------|-----------------------------------|
| Train       | 2007-09-17 → ~2023-??-??  | 3765 | 80%           | Chronological; no leakage         |
| Validation  | Inside Train              | ~565 | 15% of Train  | Used for early stopping           |
| Test        | ~2023-??-?? → 2025-10-01  | 942  | 20%           | Strictly future unseen data       |


now give me like this code for the entire readme
