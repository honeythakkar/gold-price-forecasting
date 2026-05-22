# Developing a Forecasting Model for Gold Price



## Overview

A time series analysis and forecasting project on historical gold price data, built for **ECON: Business and Economic Forecasting** at the University of Texas at Arlington on December 2024.

Applied multiple ARIMA models to 5 years of daily gold price data to identify trends, seasonality, and generate price forecasts.

---

## Key Results

- 📈 Identified strong upward trend in gold prices over the 5-year period
- 📅 Detected seasonal patterns using STL decomposition
- 🏆 Best model selected via auto.ARIMA after comparing ARIMA(1,1,1) and ARIMA(1,2,1)
- 📉 Negative correlation found between Spill Duration and Recovery Efficiency

---

## Project Structure

```
gold-price-forecasting/
│
├── TimeSeries_FinalProject_1.Rmd   # Full R Markdown analysis file
└── README.md
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| R | Primary analysis language |
| ggplot2 | Data visualization |
| forecast | ARIMA modeling and forecasting |
| lubridate | Date handling |
| gridExtra | Multi-plot layouts |

---

## Methodology

### 1. Data Preprocessing
- Loaded daily gold price data (Open, Close, High, Low, Volume)
- Handled missing values and aligned trading day sequences excluding weekends
- Converted date columns to proper datetime format

### 2. Exploratory Data Analysis
- Visualized Open, Close, High, Low price trends over time
- Analyzed trading volume patterns
- Generated pair plots and violin plots by price type

### 3. Log Transformation & Stationarity
- Applied log transformation to stabilize variance
- Tested stationarity of the time series before modeling

### 4. ARIMA Modeling
- Fitted and compared three models:
  - ARIMA(1,1,1)
  - ARIMA(1,2,1)
  - auto.ARIMA (best fit selected automatically)
- Evaluated residuals to validate model assumptions

### 5. STL Decomposition
- Separated time series into trend, seasonal, and residual components
- Used decomposition to improve forecast accuracy

### 6. Forecasting
- Generated gold price forecasts on test data
- Plotted forecasted vs actual values for model evaluation

---

## How to Run

1. Clone this repository
2. Open `TimeSeries_FinalProject_1.Rmd` in RStudio
3. Install required packages if needed:
```r
install.packages(c("ggplot2", "forecast", "lubridate", "gridExtra", "zoo"))
```
4. Click **Knit** to run the full analysis and generate the report

---

## Course Information

- **Course:** ECON 5337-02: Business and Economic Forecasting
- **Institution:** University of Texas at Arlington
- **Date:** December 2024
- **Team:** Group project (2 members)

---

## Author

**Honey Bhatt**
MS Business Analytics | UT Arlington '25
[LinkedIn](https://www.linkedin.com/in/honeythakkar)

