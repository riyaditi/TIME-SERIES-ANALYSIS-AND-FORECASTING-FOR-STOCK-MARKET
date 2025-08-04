# TIME-SERIES-ANALYSIS-AND-FORECASTING-FOR-STOCK-MARKET
This project aims to analyze and forecast stock market trends using time series analysis techniques. Here  i have studied various time series models to understand historical patterns, identify trends and  seasonality, and make short-term or long-term predictions. 
# Stock Market Prediction Project

## Introduction

This project aims to forecast stock market prices using various time-series models. The primary goal is to predict the closing price of a stock, using historical data. This project explores the application of Long Short-Term Memory (LSTM) and Facebook's Prophet models for this purpose. The implementation is done in a Jupyter Notebook, providing a step-by-step process of data collection, preprocessing, model building, and evaluation.

---

## Data Collection and Preprocessing

The historical stock market data for **Apple (AAPL)** is collected for this project.

-   **Data Source**: The data is fetched using the `yfinance` library.
-   **Time Period**: The dataset spans from **January 1, 2020, to January 8, 2025**.
-   **Feature**: The **'Close'** price of the stock is used as the target variable for forecasting.
-   **Preprocessing**:
    -   The 'Close' price data is scaled using the `MinMaxScaler` from the scikit-learn library to normalize the data between 0 and 1. This helps in improving the performance of the LSTM model.
    -   The data is split into training (80%) and testing (20%) sets to train the model and evaluate its performance on unseen data.

---

## Models Implemented

### LSTM (Long Short-Term Memory)

-   **Reasoning**: LSTMs are a type of recurrent neural network (RNN) that are well-suited for time-series forecasting tasks. They are capable of learning long-term dependencies in sequential data, which is a key characteristic of stock market prices.
-   **Implementation**: A sequential LSTM model is built using the Keras library. The model consists of two LSTM layers followed by two Dense layers.
-   **Accuracy**:
    -   **Mean Squared Error (MSE)**: 8.01
    -   **Root Mean Squared Error (RMSE)**: 2.83

### Prophet

-   **Reasoning**: Facebook's Prophet is a powerful and easy-to-use forecasting tool that is robust to seasonality and trend changes. It is included in this project for comparison and to demonstrate an alternative approach to time-series forecasting.
-   **Implementation**: The Prophet model is implemented by creating a dataframe with 'ds' (datestamp) and 'y' (target value) columns and then fitting the model to this data.

**Note**: This notebook primarily focuses on the implementation of LSTM and Prophet models. ARIMA and SARIMA models are not implemented in this version.

---

## Visualization

The project includes visualizations to gain insights from the data and to evaluate the model's performance.

-   **Historical Price and Moving Averages**: The notebook plots the historical closing prices of Apple stock along with 10, 20, 30, and 40-day moving averages to visualize the trend.
-   **LSTM Model Predictions**: The training data, validation data, and the predictions from the LSTM model are plotted on a single graph to visually inspect the accuracy of the forecast.
-   **Prophet Forecast**: The Prophet model's forecast is visualized using its built-in plotting capabilities, which show the trend, seasonality, and the predicted values.

---

## How to Use

To run this project, you will need to have a Python environment with the following libraries installed:

-   pandas
-   numpy
-   yfinance
-   scikit-learn
-   keras
-   tensorflow
-   matplotlib
-   prophet

You can then open and run the `Zidio_Development_Stock_Market_Prediction_Project.ipynb` Jupyter Notebook.

---

## Conclusion

This project demonstrates the use of LSTM and Prophet models for stock market prediction. The LSTM model shows a good performance with a low RMSE, and the visualizations confirm that the model's predictions are close to the actual stock prices. The inclusion of the Prophet model provides a comparison with a different forecasting approach. This project serves as a good starting point for anyone interested in time-series analysis and stock market forecasting.
