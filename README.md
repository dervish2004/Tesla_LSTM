# 📈 Tesla Stock Price Prediction using LSTM

## 📌 Project Overview
This project implements a **Long Short-Term Memory (LSTM)** neural network to predict **Tesla (TSLA) stock closing prices** using historical stock market data.  
The model is developed in **Python** using **TensorFlow/Keras** and executed in a **Jupyter Notebook**.

The objective of this project is to apply time series forecasting concepts learned from the Tesla Stock Price Forecasting using LSTM tutorial.

---

---

## 📊 Dataset Information
- **Source**: Yahoo Finance (using `yfinance`)
- **Stock Symbol**: TSLA (Tesla Inc.)
- **Date Range**: 2015-01-01 to 2024-01-01
- **Columns**:
  - Date
  - Open
  - High
  - Low
  - Close
  - Volume

Only the **Closing Price** is used for prediction.

---

## 🔧 Technologies & Libraries Used
- Python 3.11
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- yfinance

---

## 🧹 Data Preprocessing
1. Downloaded historical Tesla stock data using `yfinance`.
2. Removed duplicate columns and ensured correct column names.
3. Converted the `Close` column from string to numeric format.
4. Handled missing values using `dropna()`.
5. Selected `Close` price as the target feature.
6. Normalized data using `MinMaxScaler`.
7. Created time-series sequences for LSTM input.

---

## 🧠 LSTM Model Architecture
- Sequential model
- LSTM layer
- Dropout layer to reduce overfitting
- Dense output layer
- Optimizer: Adam
- Loss function: Mean Squared Error (MSE)
- Early Stopping used during training

---

## 🏋️ Model Training
- Data split into training and testing sets (time-based split).
- Model trained on historical closing prices.
- Validation performed on unseen test data.

---

## 📈 Model Evaluation
The model performance was evaluated using:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

---

## 📊 Results & Visualization
- Visualized actual vs predicted Tesla closing prices using Matplotlib.
- The model captures overall trend but may lag during sharp price fluctuations.

---

## 🔍 Key Observations
- LSTM performs well for long-term trends.
- Sudden market changes are harder to predict.
- Increasing data and tuning hyperparameters can improve results.

---

## 🚀 How to Run the Project
1. Clone the repository or extract the ZIP file.
2. Install required libraries:
   ```bash
   pip install numpy pandas matplotlib tensorflow scikit-learn yfinance
