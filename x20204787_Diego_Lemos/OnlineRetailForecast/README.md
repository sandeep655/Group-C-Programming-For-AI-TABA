# Programming for AI - Final Project

## Overview

This project is part of my MSc in Artificial Intelligence, focusing on **Time-Series Analysis** applied to financial data. The dataset used for this analysis is the **Online Retail Dataset**, a transactional dataset containing 12 months of sales for a UK-based online retailer.

The primary goal of this project was to perform exploratory data analysis (EDA), implement time-series forecasting using **ARIMA** and **Prophet**, and validate predictions to gain actionable insights about the retailer's revenue trends and seasonal behaviors.

## Project Objectives

- Perform comprehensive exploratory data analysis (EDA) to understand customer behavior, product performance, and seasonal trends.
- Develop and validate **Time-Series Models (ARIMA and Prophet)** to forecast future revenue.
- Use statistical methods like **ANOVA** to understand differences in revenue distribution across time periods.
- Present findings with clear visualizations and insights to aid decision-making.

## Dataset

The dataset used in this project can be accessed from the **UCI Machine Learning Repository**:  
[Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)

### Dataset Description

- **Transactions**: 541,909 rows
- **Features**:
  - `InvoiceNo`: Invoice number.
  - `StockCode`: Product code.
  - `Description`: Product name.
  - `Quantity`: Number of items purchased.
  - `InvoiceDate`: Date and time of the transaction.
  - `UnitPrice`: Price per unit.
  - `CustomerID`: Unique ID of the customer.
  - `Country`: Country of the customer.

---

## Key Features of the Project

### 1. **Exploratory Data Analysis (EDA)**

- **Top-performing products and customers**: Analysis of revenue contribution by products and customers.
- **Seasonal trends**: Monthly and quarterly revenue trends to identify peak periods.
- **Visualization**: Heatmaps, line charts, and bar plots to highlight trends and patterns.

### 2. **Time-Series Forecasting**

- **Models Used**:
  - **ARIMA (AutoRegressive Integrated Moving Average)**: Used for short-term forecasting.
  - **Prophet**: A robust model for handling seasonality and trend changes.
- **Forecasting**: Revenue prediction for three future months.
- **Validation**: Split data into training and testing sets to calculate MAPE and RMSE for both models.

### 3. **Statistical Testing**

- **ANOVA**: Tested the significance of revenue differences across quarters.

---

## Key Insights

- **Top Products**: Identified the top 5 products contributing the most to revenue.
- **Customer Insights**: Top customers were analyzed for purchasing patterns and frequency.
- **Seasonal Patterns**: Revenue peaks in November and December due to holiday season sales.
- **Forecast Validation**:
  - **ARIMA**: RMSE of approximately **311,650**, MAPE of **33.5%**.
  - **Prophet**: RMSE of approximately **329,113**, MAPE of **36.6%**.
  - **ARIMA** outperformed Prophet in terms of accuracy, likely due to the smaller dataset size and simpler seasonality.

---

## Results

1. **Forecasting Performance**:

   - ARIMA demonstrated slightly better accuracy compared to Prophet, suggesting its suitability for this dataset.
   - Both models forecasted similar trends for the upcoming months.

2. **Seasonal Trends**:

   - Sales increase significantly in Q4 due to holiday season shopping.
   - Revenue drops in the early months of the year (January and February).

3. **Practical Implications**:
   - Insights into customer purchasing trends can help tailor marketing strategies.
   - Forecasts provide useful information for inventory and supply chain planning.

---

## Instructions to Run the Project

### Requirements

Install the required Python libraries:

```bash
pip install -r requirements.txt
```

### Steps to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/DiegoAmaxmandro/Programming_for_AI_Final_Project.git
   cd Programming_for_AI_Final_Project
   ```

2. Open the Jupyter Notebook:

   ```bash
   jupyter notebook final_project.ipynb
   ```

3. Follow the steps in the notebook to reproduce the analysis and results.

---

## Visualizations

Some key visualizations include:

- **Revenue Trends Heatmap**: Year-by-month analysis of revenue.
- **Top Products and Customers**: Contribution to overall revenue.
- **ARIMA and Prophet Forecasts**: Revenue predictions for three future months.

---

## Acknowledgments

- Dataset: UCI Machine Learning Repository
- Guidance: National College of Ireland

---
