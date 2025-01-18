# ExcelR-Internship-Project-3

# Stock Market Analysis Project

## Introduction
This project focuses on analyzing stock market trends and patterns using historical stock price data. The objective is to extract insights, generate meaningful visualizations, and build predictive models to forecast stock price movements. The chosen dataset, `ICICIBANK_NS_cleaned_data.csv`, serves as the basis for this analysis.

---

## Project Objectives
1. Perform exploratory data analysis (EDA) to identify trends, patterns, and key insights.
2. Engineer features to enhance predictive modeling.
3. Build and evaluate machine learning models for price prediction.
4. Develop visualizations to aid stakeholders in understanding market behavior.
5. Provide actionable insights to support investment strategies.

---

## Dataset Information
- **Source:** Historical stock price data for ICICI Bank.
- **Features:**
  - **Date Features:** `Date`
  - **Numerical Features:** `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`
  - **Derived Features:** `Daily Change`, `Daily Returns`, `Moving Averages`, `Volatility`, `Differenced`, `Log-transformed Close`
- **Size:** 1,500 rows and 12 columns (after feature engineering).

---

## Exploratory Data Analysis (EDA)
1. **Time Series Analysis:** 
   - Analyzed trends in closing prices and volumes over time.
   - Visualized moving averages to identify support and resistance levels.

2. **Correlations:**
   - Computed correlations between features like `Volume`, `Close`, and derived features such as `Daily Returns`.

3. **Distribution Analysis:**
   - Plotted histograms for numerical features to understand distributions.
   - Visualized volatility to assess periods of high and low market activity.

---

## Data Preprocessing
- **Steps Taken:**
  - Handled missing values by forward-filling and back-filling techniques.
  - Scaled numerical features using Min-Max Scaler for machine learning compatibility.
  - Split dataset into training (80%) and testing (20%) sets.
  - Created lagged features for time series analysis.

---

## Feature Engineering
1. **Derived Features:**
   - **Daily Change:** Difference between `High` and `Low`.
   - **Daily Returns:** Percentage change in `Close` prices.
   - **Moving Averages:** Computed 7-day and 30-day moving averages.
   - **Volatility:** Standard deviation of returns over a 7-day window.
   - **Log-transformed Close Prices:** To normalize data distribution.

2. **Lags and Differencing:**
   - Created lagged features to account for autocorrelation in time series data.
   - Differenced the `Close` price to ensure stationarity for certain models.

---

## Machine Learning Models
The following predictive models were trained and evaluated to forecast closing prices:
1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. XGBoost Regressor
5. ARIMA (for time series forecasting)
6. LSTM (Long Short-Term Memory networks for sequential data)

---

## Model Evaluation
- **Metrics Used:** 
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R-squared (R²)

---

## Findings and Insights
1. The stock exhibited seasonality and trends that could be leveraged for trading strategies.
2. Moving averages provided reliable indicators for identifying buy and sell signals.
3. High volatility periods aligned with significant market events, offering opportunities for high-risk, high-reward strategies.

---

## Deployment
- **Framework:** Streamlit.
- **Process:**
  1. Exported the trained `Random Forest` and `ARIMA` models as pickle files.
  2. Built a Streamlit application to:
     - Allow users to input stock-related parameters.
     - Visualize historical trends and forecast future stock prices.
  3. Deployed the app locally using Ngrok for external access.

---

## Conclusion
This project demonstrates the potential of using machine learning and time series models to analyze stock market data and generate actionable insights. Future work could involve:
- Extending the analysis to multiple stocks or indices.
- Using advanced deep learning techniques like transformers for better forecasting.
- Incorporating fundamental and sentiment analysis for a holistic approach.

---

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/Ompreeth17/stock-market-analysis.git

Files in the Repository
- app.py: Streamlit application for deployment.
- rf_model.pkl: Pickled Random Forest Regressor.
- arima_model.pkl: Pickled ARIMA model.
- ICICIBANK_NS_cleaned_data.csv: Dataset used for the project.
- README.md: Project documentation.

  Technologies Used
- Programming Language: Python
- Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Statsmodels, TensorFlow/Keras (for LSTM), Streamlit
- Deployment Tool: Streamlit
