# Stock Sentiment Analysis using LSTM

This project applies **Long Short-Term Memory (LSTM)** models and sentiment analysis to predict stock price movements based on news headlines. Using historical data and sentiment scores, the project generates buy/sell signals and evaluates the effectiveness of a simple trading algorithm built around these predictions.

## Project Overview

- **Data Sources**: 
  - **News Headlines**: Scraped from Market Insider.
  - **Stock Prices**: Retrieved via Yahoo Finance API (2020–2024).

- **Sentiment Analysis**: 
  - Uses the **FinBERT model** to classify sentiment (Positive, Negative, Neutral) and assign a weighted sentiment score to each headline.
  - Daily sentiment features are derived as inputs to the LSTM model.

- **Model**:
  - **LSTM Regression Model**: Predicts the next day's close price using a 5-day sequence of features, including stock prices and sentiment scores.
  - **Evaluation Metrics**: MAE, MSE, RMSE, and R-squared.

- **Trading Algorithm**:
  - Buy and sell signals based on predicted price changes.
  - Portfolio management strategy starting with a $100,000 initial investment, with performance measured by metrics like Sharpe Ratio and Maximum Drawdown.

## Key Results

- **Prediction Accuracy**: R-squared = 0.9431
- **Trading Performance**: 
  - Sharpe Ratio = 1.8151
  - Maximum Drawdown = -0.0810
  - Win Ratio = 0.3202

## Future Improvements

- Enhanced data collection for improved model reliability.
- Advanced pre-processing techniques and more complex LSTM architectures.
- Optimized trading strategy incorporating risk factors, stop-loss mechanisms, and diversified portfolio management.

