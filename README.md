# Financial Market Prediction

This project predicts stock prices using Long Short-Term Memory (LSTM) networks. The dataset used is historical stock data for Apple Inc. (AAPL) downloaded from Yahoo Finance.

## Installation

To run this project locally, install the required libraries:
z
```bash
pip install numpy pandas matplotlib seaborn tensorflow keras yfinance scikit-learn


Data Collection
The historical stock data for Apple Inc. (AAPL) is downloaded using the yfinance library. The data ranges from January 1, 2015, to January 1, 2023.

Data Preprocessing
The closing prices are extracted and normalized using the MinMaxScaler from scikit-learn. The data is then split into training and testing sets.

Model
A Long Short-Term Memory (LSTM) network is built using TensorFlow's Keras API. The model consists of:

Two LSTM layers with 50 units each
A Dense layer with 25 units
A final Dense layer with 1 unit
The model is trained to minimize the mean squared error (MSE).

Training
The model is trained on the training dataset, which consists of 80% of the historical data. The remaining 20% is used for testing. The training process involves predicting the stock prices based on the previous 60 days' closing prices.

Evaluation
The model's performance is evaluated using the test dataset. The predictions are then inverse transformed to get the actual stock prices.

Results
The model predicts stock prices with reasonable accuracy. Below is a plot showing the actual prices, training predictions, and test predictions.
