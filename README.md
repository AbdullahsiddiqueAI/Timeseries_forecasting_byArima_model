# Time Series Analysis and Forecasting with ARIMA

## Dataset

The dataset used in this project is the Mauna Loa Daily Temperatures dataset, which contains daily average temperature readings.
https://github.com/gupta24789/Machine-Learning-Datasets/blob/master/MaunaLoaDailyTemps.csv

## Steps and Implementation

### 1. Loading and Preprocessing Data
   - The dataset is loaded from the CSV file using Pandas.
   - Missing values are dropped, and the 'AvgTemp' column is selected for analysis.
   - The time series plot of average temperatures is visualized using Matplotlib.

### 2. Stationarity Check
   - The stationarity of the time series is checked using the Dickey-Fuller test (`adfuller` function from `statsmodels.tsa.stattools`).
   - The test confirms the non-stationarity of the dataset based on the p-value.

### 3. ARIMA Model Selection
   - The `auto_arima` function from `pmdarima` library is used to automatically select the best ARIMA model parameters (`p`, `d`, `q`).
   - The function performs an exhaustive search over multiple combinations and selects the model with the lowest AIC (Akaike Information Criterion).

### 4. Model Training and Evaluation
   - The dataset is split into training and test sets.
   - An ARIMA model with selected parameters is trained using `statsmodels.api`.
   - The model is evaluated on the test set using RMSE (Root Mean Squared Error) to measure forecast accuracy.

### 5. Forecasting
   - After training on the entire dataset, the model is used to forecast future temperatures.
   - Future dates are generated, and predictions are made for the next 30 days.

### 6. Visualization
   - Predictions are plotted against actual temperatures to visualize the model's performance.
   - The plot includes historical data, test set predictions, and future forecasts.

## Conclusion

This project showcases the application of ARIMA for time series forecasting on temperature data. By leveraging statistical methods and Python libraries, such as `statsmodels` and `pmdarima`, accurate predictions can be made on temporal datasets. For detailed implementation and code, please refer to the provided Python script.

## Requirements

Ensure you have the following Python packages installed:

```bash
pip install pandas matplotlib statsmodels pmdarima
