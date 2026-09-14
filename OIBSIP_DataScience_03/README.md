# Task 3: Car Price Prediction with Machine Learning

## Project Overview
This project builds a machine learning regression pipeline to predict the selling price of used vehicles based on specifications such as present price, age, mileage driven, fuel type, transmission, and seller type.

## Dataset
* **Source:** Kaggle (Vehicle Dataset from CarDekho)
* **File Used:** `car data.csv`
* **Features:**
  * `Present_Price`: Ex-showroom price (in Lakhs)
  * `Kms_Driven`: Distance traveled
  * `Fuel_Type`: Petrol, Diesel, CNG
  * `Seller_Type`: Dealer, Individual
  * `Transmission`: Manual, Automatic
  * `Owner`: Number of previous owners
  * `Car_Age`: Derived feature calculated relative to the current year
  * `Brand`: Extracted manufacturer identifier

## Feature Engineering & Preprocessing
* Extracted vehicle manufacturer/brand from `Car_Name`.
* Computed vehicle age relative to the current reference year.
* Applied One-Hot Encoding to all categorical features to make them consumable for regression estimators.

## Models Evaluated
1. **Linear Regression:** Standard baseline regressor to establish linear dependency.
2. **Random Forest Regressor:** Non-linear ensemble tree model to capture complex feature interactions.

## Key Findings & Evaluation
* Evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and $R^2$ Score.
* Random Forest Regressor significantly outperforms the standard linear baseline, achieving a superior $R^2$ score and substantially lower prediction error.
* `Present_Price` and `Car_Age` emerge as the primary drivers of resale price depreciation.

## How to Run
1. Install requirements:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn