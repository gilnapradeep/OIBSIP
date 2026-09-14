# Task 2: Unemployment Analysis with Python

## Project Overview
This project performs an in-depth Exploratory Data Analysis (EDA) on unemployment data across Indian states, examining regional trends, labor participation metrics, and the acute impact of the COVID-19 lockdown restrictions during 2020.

## Dataset
* **Source:** Kaggle (Unemployment in India Dataset)
* **File Used:** `Unemployment_Rate_upto_11_2020.csv`
* **Features:**
  * `State`: Indian states/territories
  * `Date`: Monthly reporting dates across 2020
  * `Unemployment_Rate`: Estimated Unemployment Rate (%)
  * `Employed`: Estimated number of employed persons
  * `Labour_Participation_Rate`: Estimated Labour Participation Rate (%)
  * `Region`: Geographic zone (North, South, East, West, North-East)

## Key Findings & Visualizations
* **State-Level Impact:** States like Haryana, Tripura, and Jharkhand registered the highest average unemployment rates during peak disrupted months.
* **National Trend:** A severe spike in national unemployment occurred during April–May 2020 following the nationwide lockdown implementation in late March 2020.
* **Pre- vs. Post-COVID Analysis:** Mean unemployment surged noticeably during the immediate post-lockdown window compared to the pre-lockdown baseline period (January–March 2020).
* **Correlation:** Correlation analysis indicates an inverse relationship between unemployment spikes and overall labor force engagement metrics across multiple regions.

## How to Run
1. Install requirements:
   ```bash
   pip install numpy pandas matplotlib seaborn