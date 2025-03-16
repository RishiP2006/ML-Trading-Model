# ML-Trading-Model
In this model I created a trading model to use data of NIFTY 50 from 2015 to 2022 to get predictions for 2024 using algorithms like Random Forest Classifiers. I made this entire model on google collab so it would be better if you run it on that

1️Project Description & ML Model Explanation

This project focuses on developing an algorithmic trading strategy for Nifty50 using a machine learning model. The goal is to maximize risk-adjusted returns while minimizing drawdowns through predictive modeling and backtesting.

  Dataset Source & Preprocessing Pipeline

Data Source: Historical daily data of Nifty50 (Adj Close, Open, High, Low, Volume)

Preprocessing Steps:

Feature Engineering (SMA, EMA, RSI, MACD, Bollinger Bands)

Handling Missing Data (Forward Fill & Interpolation)

Normalization & Scaling

Creating Target Labels based on future returns

Model Architecture & Training Overview

Model Used: XGBoost (Gradient Boosting Decision Trees)

Feature Selection: Price action indicators & statistical metrics

Training:

Train-test split: 80%-20%

Hyperparameter tuning using GridSearchCV

Evaluation metrics: Accuracy, F1-score, ROC-AUC

Risk Management Techniques

Position Sizing: Uses only 20% of capital per trade instead of going all-in.

Stop-Loss Protection: Exits trade if price drops 1% below buy price.

Take-Profit Mechanism: Exits trade if price rises 5% above buy price.

Max Drawdown Protection: Stops trading if capital falls 25% below peak.

2️Backtesting Results on Nifty50 (2024 Data)

Performance Metrics:

Sharpe Ratio: 1.71 (Higher is better)

Max Drawdown: 4.51 % (Lower is better)

Total Returns: 1.14 %



Trade Logs Summary

Final Capital: 101136.45
Number of Trades: 22
Trade Log:
('Buy', '2024-01-02', 21665.80)
('Sell', '2024-01-17', 21571.94)
('Buy', '2024-02-07', 21930.5)
...
('Final Sell', '2024-12-30', 23644.90)

3️How to Run the Code (Using Conda)

Step-by-Step Setup

1️Clone the Repository

git clone https://github.com/your-repo-name.git
cd your-repo-name

2️Create a Conda Environment

conda create --name trading_env python=3.9 -y
conda activate trading_env

3️Install Dependencies

pip install -r requirements.txt

4️Download Nifty50 Data

Ensure you have historical data saved as nifty50_data.csv in the project folder.

5️Run the Training Script

python train_model.py

6️Run Backtesting

python backtest.py

7️Analyze Results

Check the output logs for final capital, trades, and performance metrics.

View the equity curve by opening equity_curve.png
