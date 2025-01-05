
# PROJECT OVERVIEW
This project covers the time series forecasting techniques to predict the sales trends using the "Avocado Prices and Sales" dataset in retail sector. The main objective is to analyze the past data of avocado sales and its prices and implement the time series models to derive insights which can help in decision-making. This project uses various time series models such as ARIMA, SARIMA and Exponential Smoothing which helps in predicting the future trends of average proce and total volume columns of the given dataset.


# HOW TO RUN THE CODE
1. Download the project files.
2. Ensure you have Python and Jupyter Notebook installed.
3. Install these libraries:
    - pandas
    - numpy
    - matplotlib
    - statsmodels
    - seaborn
4. Run the Jupyter Notebook given "Avocado_Sales_Forecast.pynb" for step-by-step execution.
5. Outputs and visualizations will be displayed.


# DATA DESCRIPTION
The "Avocado Prices and Sales" dataset contains sales and pricing information across various regions. The dataset has 18249 entries and 14 columns.
The columns used in this analysis are:
1. Date - The date of the observation
2. AveragePrice - the average price of a single avocado
3. type - conventional or organic
4. year - year
5. Region - the city or region of the observation
6. Total Volume - Total of small, large and extra large bags
7. PLU 4046 - Total number of avocados with PLU 4046 sold
8. PLU 4225 - Total number of avocados with PLU 4225 sold
9. PLU 4770 - Total number of avocados with PLU 4770 sold


# DATA PREPROCESSING
Data Preprocessing steps includes:
1. Handling outliers using IQR method.
2. Segmenting the data on a weekly level.
3. Transforming data with log transformation to stabilize variance.


# METHODOLOGY
1. EXPLORATORY DATA ANALYSIS:
    - Visualizing trends, distributions and seasonal pattersn in this data.
    - Weekly segmentation and correlation analysis.

2. STATIONARITY CHECK:
    - Conducting ADF tests and visual inspections.
    - Differencing and log transformations to acheive stationarity.

3. MODEL IMPLEMENTATION:
    - ARIMA Model
    - SARIMA Model
    - ETS (Exponential Smoothing) Model

4. MODEL EVALUATION:
    - Evaluation metrics include MAE, RMSE, MAPE and R-squared.
    - Comparison of models based on evaluation metrics.


# MODEL IMPLEMENTATION
1. The data was split into training and testing sets with a split of 80% and 20%. 
2. ARIMA: 
    - Effective for non-seasonal data with short-term dependencies.
    - Evaluated using differenced and log-transformed data.
    - This has performed better for Total Volume.

3. SARIMA:
    - Adds seasonal components to ARIMA for better performance on periodic trends.

4. ETS:
    - Captures level, trend and seasonality.
    - ETS was the best model for Average Prices.


# RESULTS
1. The ETS model performed well for ARIMA and SARIMA for Average Price. But ETS struggled with Total Volume where ARIMA showed relatively better performance.
2. Average Price:
    - ETS achieved the lowest MAE (0.021) and RMSE (0.028) showing its strong fit.
    - The R-squared value of 0.687 confirms that ETS is the best fit for forecasting Average Price.
3. Total Volume: 
    - ETS had a high MAE (0.329) and RMSE (0.370) with an R-squared value of -3.73 showing poor fit.
    - ARIMA performed better with an MAE of 0.111, RMSE of 0.145 and a positive R-squared value of 0.275. Improvements are required for better predictions.
4. Forecast graph shows a stable increase in total volume and fluctuations in average price for next 15 weeks.


# FUTURE WORK
1. ARIMA was a strong fit for Total Volume but ETS was a best fit for Average Price from the three models applied. 
2. Extend the analysis to include additional features such as weather conditions or regions.
3. Implement deep learning models like LSTMs or Prophet for comparison.
