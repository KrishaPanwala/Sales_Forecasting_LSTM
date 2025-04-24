Sales Forecasting with LSTM
This project demonstrates how to forecast monthly sales using historical retail data and a Long Short-Term Memory (LSTM) neural network.

1.Dataset
-Source: sales_data.csv
-Columns: date, store, item, sales
-~913,000 rows of daily sales data
-Transformed into monthly aggregated sales for modeling

2.Data Preprocessing
-Converted date to datetime, grouped sales monthly
-Differenced the sales values to make the series stationary
-Created lag features (up to 12 months)

3.Exploratory Analysis
Visualized raw monthly sales and differenced series using plotly

4.Baseline Modeling
-Implemented linear regression on lagged features
-Achieved adjusted R² ≈ 0.98 with 12 lags

5.LSTM Model
-Input: 12 previous monthly differences
-Output: Predicted difference in sales

6.Model architecture:
  1 LSTM layer with 4 units (stateful)
  1 Dense output layer
  Trained using Mean Squared Error and Adam optimizer

Libraries Used: pandas, numpy, matplotlib, plotly, sklearn, keras, tensorflow, statsmodels

📌 Key Insight
LSTM effectively captures seasonal sales trends when given past differences in sales with sufficient lag features.

