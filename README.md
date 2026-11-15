# Time Series Analysis of the EUR/DZD Exchange Rate

This project analyzes and forecasts the EUR/DZD exchange rate using weekly observations from August 2011 to March 2026. It was prepared for the **Time Series Analysis and Classification** course at ENSIA.

## Project objectives

- Explore the long-term behavior and trend of the EUR/DZD exchange rate.
- Prepare and split the data chronologically to avoid data leakage.
- Test stationarity using transformations and statistical tests.
- Identify and fit an ARIMA model using ACF/PACF analysis and information criteria.
- Diagnose the fitted model and evaluate rolling and multi-step forecasts.

## Main result

The analysis selects an **ARIMA(1,1,1)** model. The rolling one-step-ahead forecast achieves approximately:

- **MAPE:** 0.32%
- **RMSE:** 0.49 DZD

These results describe short-term forecasting performance. The notebook also discusses the model's limitations, including its inability to incorporate external factors such as oil prices, interest rates, inflation, and other macroeconomic variables.

## Repository contents

| Path | Description |
| --- | --- |
| `Analysis.ipynb` | Main R-based analysis notebook |
| `notebook.ipynb` | Additional project notebook |
| `DZDEURSPOT_2026-03-23.txt` | Source EUR/DZD exchange-rate data |
| `data/processed_data.csv` | Processed weekly exchange-rate series |
| `data/train_set.csv` | Chronological training set |
| `data/test_set.csv` | Chronological test set |

## Requirements

- R
- Jupyter Notebook or Google Colab with an R kernel
- R packages: `readr`, `dplyr`, `tidyr`, `ggplot2`, `gridExtra`, `forecast`, `tseries`, and `nortest`

The notebook includes setup code that installs missing R packages from CRAN.

## Running the analysis

1. Open `Analysis.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
2. Select an R kernel.
3. Run the cells from top to bottom.
4. If running outside Google Colab, update the data path in the data-loading cell if necessary.

The analysis covers data preparation, visualization, stationarity testing, model identification, fitting, diagnostics, forecasting, and conclusions.

## Data note

The exchange-rate observations are weekly EUR/DZD spot-rate data sourced from Boursorama, covering August 2011 to March 2026. The processed files contain the date, exchange-rate value, and, where applicable, the log-transformed value.
