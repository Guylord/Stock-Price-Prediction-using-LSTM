# Stock Price Prediction using LSTM

This project implements a Long Short-Term Memory (LSTM) model to predict stock prices based on historical data.

## Overview
The LSTM model is trained to predict future stock prices based on past closing prices. The dataset is preprocessed, normalized, and split into training and test sets. The model is then trained and evaluated, with results visualized by comparing the predicted prices to the actual prices.

## Key Steps:
1. **Data Collection**:
   - Stock data is fetched using the `yfinance` library for a specified symbol (e.g., 'AAPL') over a defined date range.
   
2. **Data Preprocessing**:
   - The 'Close' prices are used for prediction.
   - Data is scaled using `MinMaxScaler` to normalize values between 0 and 1.
   - A rolling window of 60 days is used to predict the next day's stock price.

3. **Model Building**:
   - An LSTM model is created with two LSTM layers, followed by Dropout layers for regularization and a Dense layer for output.
   - The model is compiled using the Adam optimizer and Mean Squared Error loss function.

4. **Training**:
   - The model is trained for 50 epochs using the training set, with 80% of the data for training and 20% for testing.

5. **Prediction & Evaluation**:
   - The trained model makes predictions on the test set.
   - The predicted stock prices are compared with actual values, and the results are visualized using `matplotlib`.

## Requirements:
- `yfinance` for fetching stock data
- `numpy`, `pandas`, `matplotlib` for data manipulation and visualization
- `sklearn` for data scaling
- `tensorflow` for building and training the LSTM model

## Usage:

Install required libraries:
   ```bash
   pip install yfinance numpy pandas matplotlib scikit-learn tensorflow
