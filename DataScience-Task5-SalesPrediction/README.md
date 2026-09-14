# Task 5: Sales Prediction Using Python

## Project Overview
This project develops predictive regression models to forecast product sales based on advertising expenditure across three distinct media channels: Television (`TV`), `Radio`, and `Newspaper`.

## Dataset
* **Source:** Advertising Dataset
* **File Used:** `Advertising.csv`
* **Features:**
  * `TV`: Advertising budget spent on TV (in thousands of dollars)
  * `Radio`: Advertising budget spent on Radio (in thousands of dollars)
  * `Newspaper`: Advertising budget spent on Newspaper (in thousands of dollars)
  * `Sales` (Target): Total units sold (in thousands)

## Exploratory Data Analysis & Key Insights
* **TV Advertising:** Demonstrates the strongest positive linear correlation with product sales, serving as the primary volume driver.
* **Radio Advertising:** Shows moderate-to-strong positive correlation and functions effectively as a supplementary multiplier channel.
* **Newspaper Advertising:** Displays weak correlation with sales, indicating diminishing returns relative to direct budget allocation.

## Models Evaluated
1. **Multiple Linear Regression:** Serves as the interpretable baseline model to quantify channel coefficients and budget elasticity.
2. **Ridge Regression:** Employs L2 regularization to evaluate coefficient shrinkage and prevent potential multi-collinearity inflation.
3. **Random Forest Regressor:** Non-linear ensemble model capturing non-linear interactions and cross-channel synergy effects.

## Performance Benchmark
* Evaluated across Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and $R^2$ Score.
* Both Linear Regression and Random Forest achieve strong predictive accuracy ($R^2 > 0.90$), with Random Forest effectively capturing non-linear media mix interactions.

## How to Run
1. Install requirements:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn