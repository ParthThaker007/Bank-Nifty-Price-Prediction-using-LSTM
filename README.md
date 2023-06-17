# Bank-Nifty-Price-Prediction-using-LSTM


The provided code implements a time series forecasting task using an LSTM model to predict Bank Nifty values. Here's a review of the code:

1. Data Acquisition and Preprocessing:
   - The code utilizes the `yfinance` library to download historical Bank Nifty data and saves it to a CSV file for further processing.
   - The data is then loaded from the CSV file using `pandas`, and the 'Close' prices are extracted for analysis.
   - The data is normalized using `MinMaxScaler` to scale the values between 0 and 1.

2. LSTM Model:
   - The code defines an LSTM model using the `Sequential` API from Keras.
   - The model architecture consists of one LSTM layer followed by a Dense layer.
   - The model is compiled with the mean squared error (MSE) loss function and the Adam optimizer.

3. Data Preparation:
   - The data is split into training and testing sets, with the first 800 data points used for training and the remaining data points for testing.
   - The `create_dataset` function is used to create input-output pairs with a given lookback window.

4. Model Training and Prediction:
   - The model is trained using the training data, with a batch size of 1 and 10 epochs.
   - The trained model is then used to make predictions on both the training and testing data.
   - The predictions are inverse-transformed to obtain the actual predicted Bank Nifty values.

5. Evaluation and Visualization:
   - The code plots the actual and predicted Bank Nifty values for both the training and testing periods using `matplotlib`.
   - The plot shows how well the model predicts the Bank Nifty values over time.

6. Evaluation Metrics:
   - The code calculates the coefficient of determination (R-squared) as an evaluation metric using `r2_score` from `sklearn.metrics`.
   - The R-squared value measures the proportion of the variance in the target variable that is predictable from the independent variable.

Overall, the code demonstrates a solid implementation of LSTM-based time series forecasting using historical Bank Nifty data. It provides a visualization of the predicted values and calculates the R-squared value to evaluate the model's performance.

To further improve the project, you could consider the following enhancements:
- Implement cross-validation techniques for more robust evaluation.
- Explore hyperparameter tuning to optimize the LSTM model's performance.
- Incorporate additional evaluation metrics such as mean absolute error (MAE) or root mean squared error (RMSE) to provide a comprehensive assessment.
- Document the project by adding comments throughout the code and providing a detailed explanation of the code's functionality and the chosen model architecture.

# Output:
<img width="624" alt="Screenshot 2023-06-17 183843" src="https://github.com/ParthThaker007/Bank-Nifty-Price-Prediction-using-LSTM/assets/101121538/58774e21-084c-4e5c-a7c0-1a0cf4f7e244">
