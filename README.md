# 📈 Tesla Stock Price Prediction using LSTM

## 📌 Project Overview

This project implements a **Long Short-Term Memory (LSTM) neural network** to predict **Tesla (TSLA) stock closing prices** using historical market data. The model is built using **Python, TensorFlow/Keras**, and executed in a **Jupyter Notebook environment**.

The goal is to explore **time series forecasting**, sequence learning, and deep learning applications in financial data analysis.

---

## 📊 Dataset Information

* **Source**: Yahoo Finance (via `yfinance`)
* **Stock Symbol**: TSLA (Tesla Inc.)
* **Date Range**: 2015–01–01 to 2024–01–01

### Features:

* Date
* Open
* High
* Low
* Close (Target)
* Volume

✔ Only the **Closing Price** is used for prediction.

---

## ⚙️ Technologies Used

* Python 3.11
* Jupyter Notebook
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* TensorFlow / Keras
* yfinance

---

## 🧹 Data Preprocessing Pipeline

1. Collected historical stock data using `yfinance`
2. Cleaned dataset (handled missing values using `dropna()`)
3. Selected only **Close price** as target variable
4. Converted data into numeric format
5. Applied **MinMaxScaler normalization**
6. Created time-series sequences for LSTM input:

   * Input shape: `(samples, timesteps, 1)`

---

## 🧠 Model Architecture (LSTM)

* Sequential Neural Network
* LSTM Layer (sequence learning)
* Dropout Layer (overfitting control)
* Dense Output Layer (final prediction)
* Optimizer: Adam
* Loss Function: Mean Squared Error (MSE)
* Early Stopping applied during training

---

## 🏋️ Model Training

* Time-based train-test split (no shuffling)
* Model trained on historical price sequences
* Validation performed on unseen test data
* Early stopping used to prevent overfitting

---

## 📈 Evaluation Metrics

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

---

## 📊 Results & Visualization

* Predicted vs Actual Tesla stock prices plotted using Matplotlib
* Model captures **overall trend direction** effectively
* Performance decreases during **sudden market volatility spikes**

---

## 🔍 Key Observations

* LSTM is effective for **long-term trend forecasting**
* Struggles with **high volatility and sudden market shifts**
* Performance improves with:

  * More training data
  * Hyperparameter tuning
  * Additional market indicators (feature engineering)

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repo-link>
cd tesla-lstm-prediction
```

### 2. Install Dependencies

```bash
pip install numpy pandas matplotlib tensorflow scikit-learn yfinance
```

### 3. Run Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```
Tesla_Stock_Price_Prediction_LSTM.ipynb
```

---

## 📁 Project Structure

```
├── Tesla_Stock_Price_Prediction_LSTM.ipynb
├── data/ (optional cached dataset)
├── models/ (saved LSTM model)
├── plots/ (prediction visualizations)
├── README.md
```

---

## 📌 Future Improvements

* Add additional features (RSI, MACD, moving averages)
* Use Bidirectional LSTM
* Compare with GRU and Transformer models
* Deploy as a Flask or Streamlit web app
* Add live stock prediction dashboard

---
