# AQI Forecasting with ARIMA and SARIMA Models

This repository contains a Jupyter Notebook designed to predict the Air Quality Index (AQI) for the next six months using ARIMA and SARIMA time series forecasting models.

## Project Overview

Air Quality Index (AQI) is a vital metric that helps monitor air pollution and its potential health impacts. In this notebook, we forecast AQI values for the next 183 days (approximately 6 months) using two statistical models: ARIMA and SARIMA. The data spans from 2016 to 2024, and the forecast begins from September 2024.

## Contents

- `air_quality_forecasting.ipynb`: The Jupyter Notebook containing code for data preprocessing, model building, forecasting, and visualization.
- `AQI_forecast_arima.csv`: Output file containing the 6-month AQI forecast using the ARIMA model.
- `AQI_forecast_sarima.csv`: Output file containing the 6-month AQI forecast using the SARIMA model.

## Models Used

### ARIMA (AutoRegressive Integrated Moving Average)
- **ARIMA** is a statistical model that combines autoregressive (AR), differencing (I), and moving average (MA) components to model time series data and forecast future points.
- In this notebook, we use ARIMA to forecast AQI values for the next 183 days.
- The model parameters `(p=1, d=1, q=1)` are used to capture the trend and noise in the AQI data.

### SARIMA (Seasonal ARIMA)
- **SARIMA** extends the ARIMA model by accounting for seasonal patterns. It adds seasonal differencing, autoregression, and moving average components, making it ideal for data with repeating patterns (e.g., yearly or monthly cycles).
- The seasonal order `(P=1, D=1, Q=1, s=365)` accounts for yearly seasonality in the AQI data.

## How to Use

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/aqi-forecasting.git
    cd aqi-forecasting
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Open and run the Jupyter Notebook to train the models and generate forecasts:
    ```bash
    jupyter notebook air_quality_forecasting.ipynb
    ```

4. The forecasted results will be saved as CSV files:
    - `AQI_forecast_arima.csv` for ARIMA model predictions.
    - `AQI_forecast_sarima.csv` for SARIMA model predictions.

## Data

- The AQI data used spans from **01-01-2016** to **31-08-2024**, with daily records.
- The target variable is AQI (`aqi`), and the date index is used for time series forecasting.
- Preprocessing includes handling missing values, transforming the date index, and splitting the data for model training.

## Results

- **ARIMA** and **SARIMA** models are used to predict AQI for the next 6 months.
- Predictions are stored in CSV files with forecasted AQI values, and plots of the forecasted AQI vs. the historical data are provided in the notebook.

## Requirements

You’ll need the following Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `statsmodels`

You can install all required dependencies using:
```bash
pip install -r requirements.txt
```

## Future Enhancements

- Further fine-tuning of the **ARIMA** and **SARIMA** models.
- Consider more advanced time series forecasting techniques like **Auto ARIMA** or **LSTM** for better accuracy.
- Include external features (such as temperature, humidity, etc.) that may affect AQI.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### Customization
- Replace `Abdoo50` with your GitHub username.
- Modify the "Future Enhancements" section if you plan to add more features.
