# 📈 Forecasting TSMC Stock Prices with LSTM and ARIMA

This project applies time-series modeling techniques to forecast the stock price of Taiwan Semiconductor Manufacturing Company (TSMC), a key player in the global semiconductor and AI hardware industry. Leveraging both machine learning and statistical models—LSTM and ARIMA—the project aims to compare the strengths of each approach in capturing financial market dynamics.

---

## 🧠 Background

TSMC is the world’s largest contract chipmaker, supplying advanced chips for high-growth industries including AI and high-performance computing. Understanding its stock movements offers meaningful insights into broader market trends, particularly in the technology sector. 

This project explores the predictive relationship between TSMC's stock price and other financial indicators including:
- **Nvidia (NVDA)** — TSMC’s major customer and AI leader
- **TAIEX** — Taiwan Stock Exchange Index
- **S&P 500** — A key benchmark for the U.S. market

Data was sourced from Yahoo Finance and analyzed from 2014 to 2024.

---

## 📊 Exploratory Data Analysis (EDA)

EDA was performed to:
- Visualize adjusted close prices over time
- Scale values for direct comparison
- Analyze percentage growth and volatility
- Identify correlations between variables
- Support feature selection using correlation matrices and GenAI insights

Key insights included Nvidia’s rapid post-2020 growth, TSMC’s steady upward trend, and significant pandemic-related market fluctuations.

---

## 🤖 Model Selection and Training

Two models were implemented and compared:

- **ARIMA**: Ideal for modeling linear trends and seasonality in financial time series.
- **LSTM**: A type of recurrent neural network suited for capturing nonlinear and long-term dependencies.

### Inputs and Assumptions:
- TSMC served as the target variable
- Predictors included Nvidia, TAIEX, S&P 500, and lagged TSMC prices
- Data was scaled and transformed for time-series modeling
- A single-step sampler was used to generate input-output sequences for LSTM
- Data was split using an 85:15 ratio for training and testing

---

## 📈 Performance Evaluation

Models were evaluated using:
- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**
- **R² Score**

The LSTM model showed promising results in capturing complex market behavior and long-term trends. ARIMA performed well on linear dependencies but was less responsive to sharp nonlinear changes.

Forecast visualizations highlight the predictive alignment between actual and forecasted TSMC prices, with the final LSTM output plotted alongside real market prices.

---

## 🚀 Tools & Technologies

- **Python Libraries**: `pandas`, `numpy`, `yfinance`, `matplotlib`, `seaborn`, `statsmodels`, `tensorflow`, `keras`, `scikit-learn`
- **Models**: LSTM (Keras), ARIMA (statsmodels)
- **Scaling & Feature Engineering**: MinMaxScaler, percentage growth calculations

---

## 🔮 Conclusion

This project demonstrates how combining deep learning and classical statistical models can provide actionable insights in financial forecasting. The inclusion of macro and micro-level predictors allows for more nuanced stock price prediction, particularly in rapidly evolving sectors like AI.
