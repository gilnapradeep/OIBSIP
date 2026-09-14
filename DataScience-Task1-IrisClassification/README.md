# Task 1: Iris Flower Classification

## Project Overview
This project trains supervised machine learning models to classify iris flowers into one of three species (*Setosa*, *Versicolor*, or *Virginica*) based on physical measurements of their sepals and petals.

## Dataset
* **Source:** `sklearn.datasets.load_iris()`
* **Number of Samples:** 150 (50 per class)
* **Features:**
  * Sepal Length (cm)
  * Sepal Width (cm)
  * Petal Length (cm)
  * Petal Width (cm)
* **Target Classes:** Setosa (0), Versicolor (1), Virginica (2)

## Exploratory Data Analysis & Insights
* **Petal Dimensions:** Petal length and petal width provide the highest discriminative power. *Iris-setosa* is linearly separable from the other two species purely based on petal measurements.
* **Overlap:** *Iris-versicolor* and *Iris-virginica* show minor overlap in sepal dimensions but can be distinguished effectively when all four dimensions are considered.

## Models Evaluated
1. **Logistic Regression:** Serves as the linear baseline classifier.
2. **Random Forest Classifier:** An ensemble tree-based classifier to capture non-linear relationships.

## Evaluation Results
* Evaluated on an 80/20 stratified train-test split.
* Performance measured using Accuracy, Precision, Recall, F1-score, and Confusion Matrices.
* Both models achieve high accuracy (>95%), with the Petal measurements identified as the most critical features for accurate classification.

## How to Run
1. Install requirements:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn