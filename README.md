# Forecasting USD/INR Volatility with a Stacked LSTM-Attention Model

This repository contains the data and code for our research paper comparing econometric and deep learning models for forecasting the realized volatility of the Indian Rupee (USD/INR).

The models in this analysis are reproducible. The script uses a fixed random seed (`seed_value = 42`) to ensure identical results on every run.

## File Structure

* `main_analysis.ipynb`: The main Colab/Jupyter notebook containing all data loading, preprocessing, model training, and evaluation.
* `final_predictors_2003_onwards.csv`: The final, cleaned dataset used in the analysis.
* `requirements.txt`: A list of all Python packages required to run the code.

## How to Reproduce Results

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/jayarammovva9/Forecasting-Exchange-Rate-Volatility.git
cd Forecasting-Exchange-Rate-Volatility

    ```

2.  **Set Up the Environment:**
    ```bash
    cd Forecasting-Exchange-Rate-Volatility
    pip install -r requirements.txt
    ```

3.  **Run the Analysis:**
    Open the `main_analysis.ipynb` notebook in Google Colab or a local Jupyter environment. Run all cells from top to bottom. The code will load the local CSV file and generate all tables and figures from the paper.

---
## Data Card

The table below details the variables, sources, and processing for the dataset.

[... PASTE THE "DATA CARD" MARKDOWN TABLE HERE ...]

---
## Data Split

We use a fixed, chronological 80/20 train-test split to ensure the model is always forecasting on unseen future data. The training data itself is further split (85/15) to create a validation set for the LSTM's early stopping.

[... PASTE THE "DATA SPLIT TABLE" MARKDOWN TABLE HERE ...]
