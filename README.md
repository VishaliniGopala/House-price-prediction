# House Price Prediction — Regression Project

## Objective

Build a machine learning regression model to predict house prices using housing features.

---

## Dataset

House Price Prediction Dataset

Target Variable:

price

---

## Features Used

- date
- bedrooms
- bathrooms
- sqft_living
- sqft_lot
- floors
- waterfront
- view
- condition
- sqft_above
- sqft_basement
- yr_built
- yr_renovated
- street
- city
- statezip
- country

---

## Project Workflow

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Missing Value Handling
4. Feature Engineering
5. Log Transformation
6. Encoding Categorical Features
7. Feature Scaling
8. Model Training
9. Evaluation
10. Residual Analysis
11. Model Saving
12. Prediction Example

---

## Models Compared

- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor

---

## Evaluation Metrics

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score
- Residual Analysis

---

## Package Versions

Python == 3.10

pandas == 2.2.3

numpy == 2.2.5

matplotlib == 3.10.1

seaborn == 0.13.2

scikit-learn == 1.6.1

joblib == 1.5.0

---

## Installation Commands

Create virtual environment (optional):

```bash
python -m venv venv
```

Activate environment.

Windows:

```bash
venv\Scripts\activate
```

Linux / Mac:

```bash
source venv/bin/activate
```

Install packages:

```bash
pip install pandas==2.2.3 numpy==2.2.5 matplotlib==3.10.1 seaborn==0.13.2 scikit-learn==1.6.1 joblib==1.5.0
```

Alternative:

```bash
pip install -r requirements.txt
```

---

## Exact Commands to Reproduce Results

### Run Notebook

Jupyter:

```bash
jupyter notebook
```

OR

```bash
jupyter lab
```

Open:

House_Price_Prediction.ipynb

Run all cells.

---

## Save Model

```python
joblib.dump(rf_model,'house_price_model.joblib')
```

---

## Run Prediction

```python
import joblib
import pandas as pd
import numpy as np

model=joblib.load('house_price_model.joblib')

sample=pd.DataFrame({

'bedrooms':[3],
'bathrooms':[2],
'sqft_living':[1800],
'sqft_lot':[5000],
'floors':[2],
'waterfront':[0],
'view':[1],
'condition':[3],
'sqft_above':[1500],
'sqft_basement':[300],
'yr_built':[2005],
'yr_renovated':[0],
'street':['123 Main Street'],
'city':['Seattle'],
'statezip':['WA98178'],
'country':['USA'],
'year':[2014],
'month':[5]

})

prediction=model.predict(sample)

print(np.expm1(prediction[0]))
```

---

## Project Files

```plaintext
House_Price_Prediction.ipynb
house_price_model.joblib
README.md
dataset.csv
```

---

## Expected Output

Model predicts estimated house price from input features.

Example:

```plaintext
Predicted Price: 450000.35
```