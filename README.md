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

| Variable        | Source         | Type    | Frequency | Missing % | Notes / Leakage Risk              |
|-----------------|----------------|---------|-----------|-----------|-----------------------------------|
| USDINR          | Yahoo Finance  | float64 | Daily     | 0%        | Used to create target              |
| VIX             | Yahoo Finance  | float64 | Daily     | 0%        | No leakage                         |
| OIL_WTI         | Yahoo Finance  | float64 | Daily     | 0%        | No leakage                         |
| SP500           | Yahoo Finance  | float64 | Daily     | 0%        | No leakage                         |
| US_10Y_YIELD    | FRED           | float64 | Daily     | 0%        | ffill used for holidays            |
| US_CPI          | FRED           | float64 | Monthly   | 0%        | Forward-filled to daily            |
| RV_d            | Self-Calculated| float64 | Daily     | 0%        | Lagged; no leakage                 |
| …               | …              | …       | …         | …         | …                                  |


---

## Data Split

| Split       | Date Range             | % of Data     | Notes                                 |
|-------------|------------------------|---------------|----------------------------------------|
| Train       | 2003-XX-XX → YYYY-XX-XX| 80%           | Chronological; no look-ahead           |
| Validation  | inside training window | 15% of train  | Used for early stopping                |
| Test        | YYYY-XX-XX → YYYY-XX-XX| 20%           | Strictly future unseen data            |



