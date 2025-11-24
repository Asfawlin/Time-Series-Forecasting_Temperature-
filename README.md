Time Series Forecasting of Monthly Temperature
1. Project Introduction
In this project, I focused on forecasting monthly temperature data using historical patterns. The main objective was to build and compare multiple time series models to determine which one provides the most accurate future temperature predictions.
The following models were implemented and compared:
•	ARIMA (Autoregressive Integrated Moving Average)
•	SARIMA (Seasonal ARIMA)
•	Exponential Smoothing

2. Dataset Overview
The dataset contains monthly average temperature values from 1900 to approximately 2017. Each row represents the average temperature for a specific month.
Data preprocessing steps:
•	Combined the Year and Month columns into a single Date column
•	Set the Date column as the index
•	Kept only the temperature column for modeling
•	Split the data into 80% for training and 20% for testing to evaluate model performance on unseen data
3. Methodology
Before building the models, the data was checked for stationarity. The dataset was already stationary, so no differencing was required.
Each model followed the same process:
1.	Trained the model on the training dataset
2.	Generated predictions for the test dataset
3.	Evaluated the performance using the following metrics:
•	RMSE (Root Mean Squared Error)
•	MAE (Mean Absolute Error)
•	MAPE (Mean Absolute Percentage Error)
4.	Analyzed the residuals (prediction errors) to assess model quality and accuracy
4. Results
ARIMA Results
•	RMSE: 4.28
•	MAE: 3.59
•	MAPE: 21.76%
The prediction plot showed significant divergence from the actual data. The residuals were larger and less centered around zero, indicating weaker performance.

SARIMA Results
•	RMSE: 1.13
•	MAE: 0.86
•	MAPE: 4.88%
SARIMA predictions matched closely with the actual test data. The residuals were smaller and more normally distributed around zero.

Exponential Smoothing Results
•	RMSE: 1.07
•	MAE: 0.81
•	MAPE: 4.68%
This model performed very similarly to SARIMA but slightly better overall. The residuals were small and well-centered around zero.

5. Conclusions
•	Both SARIMA and Exponential Smoothing performed significantly better than ARIMA for this dataset.
•	Exponential Smoothing achieved the lowest RMSE, MAE, and MAPE values, making it the best performing model.
•	This project demonstrates that models designed to handle seasonality tend to perform better when working with seasonal time series data such as monthly temperature.
