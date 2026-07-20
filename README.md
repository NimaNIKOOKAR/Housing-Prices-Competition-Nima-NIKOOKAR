# House Prices Prediction

## Overview

This project is based on the Kaggle **Housing Prices Competition for Kaggle Learn Users**.

The goal is to predict the sale price of houses in Ames, Iowa.  
The dataset contains many features about each house, such as:

- Number of rooms
- House size
- Neighborhood
- Garage information
- Basement information
- Year built
- Overall quality
- Other house characteristics

This is a **regression problem** because we are predicting a continuous numerical value: the house price.

---

## Objective

The objective is to build a machine learning model that predicts the value of:

```text
SalePrice
```

For each house in the test dataset, the model should predict the final sale price.

---

## Dataset

The dataset contains three main files:

```text
train.csv
test.csv
sample_submission.csv
```

### train.csv

This file contains the training data.  
It includes the house features and the target column `SalePrice`.

### test.csv

This file contains the test data.  
It includes the house features but does not include `SalePrice`.

### sample_submission.csv

This file shows the correct format for the final Kaggle submission.

---

## Submission Format

The final submission file must contain two columns:

```csv
Id,SalePrice
1461,169000.1
1462,187724.1233
1463,175221
```

---

## Evaluation Metric

Kaggle evaluates the predictions using RMSE between the logarithm of the predicted price and the logarithm of the real price.

```text
RMSE(log(predicted price), log(actual price))
```

This means that the model is evaluated based on relative prediction error.  
Using logarithms helps treat errors on cheap and expensive houses more equally.

---

## Skills Practiced

This project helps practice:

- Data cleaning
- Exploratory Data Analysis
- Handling missing values
- Feature engineering
- Encoding categorical variables
- Regression models
- Cross-validation
- Model evaluation and residual diagnostics
- Model stacking / ensembling
- Creating a Kaggle submission file

---

## Basic Workflow

The project follows these steps:

1. Load the data
2. Explore the dataset (distributions, missingness, correlations, neighborhood price levels, multicollinearity)
3. Clean missing values
4. Engineer and prepare numerical and categorical features
5. Train and cross-validate several regression models (linear + tree-based)
6. Stack the best models into an ensemble
7. Diagnose model errors (predicted vs actual, residuals, permutation importance, learning curve, worst predictions)
8. Make predictions on the test data
9. Create the submission file

---

## Possible Models

Some models that can be used are:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost
- LightGBM
- CatBoost

---


---

## Project Structure

```text
house-prices-prediction/
│
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
│
├── notebook.ipynb
├── submission.csv
├── README.md
└── requirements.txt
```

---

## Requirements

```text
numpy
pandas
scikit-learn
matplotlib
seaborn
jupyter
```

Optional libraries for more advanced models:

```text
xgboost
lightgbm
catboost
```

---

## How to Run

Install the required libraries:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

Or run the Python script if the project uses scripts:

```bash
python main.py
```

---

## Citation

```bibtex
@misc{home-data-for-ml-course,
    author = {DanB},
    title = {Housing Prices Competition for Kaggle Learn Users},
    year = {2018},
    howpublished = {\url{https://kaggle.com/competitions/home-data-for-ml-course}},
    note = {Kaggle}
}
```

---

## Acknowledgment

The dataset comes from the Kaggle Housing Prices competition for machine learning learners.  
It is used here for educational purposes and machine learning practice.
