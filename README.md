# Linear Regression to Predict the Nifty50

## 1. Introduction
This project aims to predict stock prices using historical closing prices from the National Stock Exchange of India (NSE) data retrieved from Yahoo Finance. I utilized linear regression to model the relationship between time (represented by an integer index) and stock prices. This README provides an overview of the methodology, exploratory data analysis (EDA), results, and conclusions drawn from the analysis.

## 2. Methodology
We collected stock price data for the NSE using the Yahoo Finance library, focusing on the historical closing prices for analysis. The choice of closing prices as the independent feature is justified by their significance in financial analysis, reflecting the final consensus price of the stock for the trading day. Closing prices are commonly used in technical analysis due to their perceived stability and reliability, making them suitable for predictive modeling.

## 3. Exploratory Data Analysis (EDA)
Several EDA techniques were employed to better understand the dataset, including:
- **Descriptive Statistics**: Summarizing key metrics such as mean, median, and standard deviation of the closing prices.
- **Time Series Visualization**: Plotting the closing prices over time to identify trends, seasonal patterns, or anomalies.
  - **Close Price Plot**:
    ![Close Price Plot](path/to/close_price_plot.png)
    - *Inference*: The plot shows the trend of Nifty50 closing prices over the 5-year period. We observe a general upward trend with some periods of high volatility.
  
- **Correlation Analysis**: Examining the relationship between the closing price and potential influencing factors, confirming the independence of our feature.
- **Residual Analysis**: Assessing the residuals of our model to check for patterns that might indicate model inadequacies.

## 4. Approach
The approach to modeling included using linear regression, where the independent variable \(X\) is represented by the integer index of the dates, and the dependent variable \(Y\) is the predicted closing stock price. The linear regression model can be mathematically expressed as:

Equation:  **Y = β₀ + β₁X + ε**

- **Y** = Predicted Closing Price  
- **X** = Integer Date Index  
- **β₀** = Intercept  
- **β₁** = Slope (coefficient)  
- **ε** = Error term  

## 5. Results
The model's evaluation yielded several important metrics. The coefficient and intercept provide insights into the relationship between time and stock prices. The coefficient indicates how much the stock price is expected to change for each unit increase in time, while the intercept indicates the expected price when the time index is zero.

### Inferences from the Train Set Graph
- **Train Set Graph**:
  ![Train Set Graph](path/to/train_set_graph.png)
  - *Inference*: The graph illustrates how well the linear regression line fits the training data. The predicted prices closely follow the actual closing prices with minor deviations.

### Inferences from Model Evaluation
- **Model Evaluation**:
  - *Inference*: Evaluation metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared value were used to assess the model’s performance. The R-squared value of 0.89 suggests a strong correlation between the predicted and actual prices, indicating the model’s effectiveness.

### Inferences from Subplots
- **Subplots**:
  ![Subplots](path/to/subplots.png)
  - *Inference*: The subplot analysis helps compare actual vs. predicted prices across various data points. It indicates that the model works well on most of the test data, with slight deviations in certain points.

### Inferences from Predicted vs Actual Prices
- **Predicted vs Actual Prices**:
  ![Predicted vs Actual Prices](path/to/predicted_vs_actual.png)
  - *Inference*: This scatter plot shows a close correlation between the predicted and actual prices. The tight clustering of points around the diagonal line suggests that the model accurately predicts the stock price for the most part.

### Inferences from Residuals Histogram
- **Residuals Histogram**:
  ![Residuals Histogram](path/to/residuals_histogram.png)
  - *Inference*: The histogram of residuals and its fit to a normal distribution indicates that the errors are randomly distributed, with no discernible pattern, confirming that the assumptions of linear regression are met.

## 6. Error Evaluation Metrics
The following error evaluation metrics were calculated to assess model performance:
- **Mean Absolute Error (MAE)**:  
  ![MAE Formula](https://latex.codecogs.com/svg.latex?%5Ccolor%7Bwhite%7DMAE%20%3D%20%5Cfrac%7B1%7D%7Bn%7D%20%5Csum%20%7Cy_i%20-%20%5Chat%7By_i%7D%7C)

- **Mean Squared Error (MSE)**:  
  ![MSE Formula](https://latex.codecogs.com/svg.latex?%5Ccolor%7Bwhite%7DMSE%20%3D%20%5Cfrac%7B1%7D%7Bn%7D%20%5Csum%20%28y_i%20-%20%5Chat%7By_i%7D%29%5E2)

- **Root Mean Squared Error (RMSE)**:<br>
  ![RMSE Formula](https://latex.codecogs.com/svg.latex?%5Ccolor%7Bwhite%7DRMSE%20%3D%20%5Csqrt%7B%5Cfrac%7B1%7D%7Bn%7D%20%5Csum%20%28y_i%20-%20%5Chat%7By_i%7D%29%5E2%7D)

## 7. Accuracy Evaluation Metrics
The accuracy of the model was assessed using:
- **R-squared (R²)**: 
  ![R-squared formula](https://latex.codecogs.com/png.latex?%5Cbg_white%20R%5E2%20%3D%201%20-%20%5Cfrac%7BSS_%7Bres%7D%7D%7BSS_%7Btot%7D%7D)
  <br>Where:
  - **\( SS_res \)** = Residual Sum of Squares
  - **\( SS_tot \)** = Total Sum of Squares

## 8. Limitations and Future Scope
While the model provides reasonable predictions, it has limitations, such as:
- Dependence on historical data, which may not account for future market anomalies or events.
- Potential for overfitting, especially with more complex models.
Future work may explore incorporating additional features, such as economic indicators, trading volumes, or even sentiment analysis from financial news, to enhance predictive power.

## 9. Conclusions
In conclusion, this project demonstrates the application of linear regression for stock price prediction using closing prices from NSE. The EDA and model evaluation provided insights into the effectiveness of the model and highlighted areas for improvement. This foundational work sets the stage for future research and development in financial modeling.
