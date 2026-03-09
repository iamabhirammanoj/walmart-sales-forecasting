# Walmart Sales Forecasting (Machine Learning)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Random%20Forest-green)
![Status](https://img.shields.io/badge/Project-Completed-success)

## Project Overview

This project builds a **Machine Learning model to forecast Walmart weekly sales** using historical retail data.  
The model uses **Random Forest Regression with time-series feature engineering** to capture temporal patterns, store-level differences, and economic indicators affecting sales.

The project demonstrates a **complete end-to-end machine learning workflow**, including:

- Data preprocessing  
- Feature engineering  
- Time-series forecasting  
- Model training  
- Performance evaluation  
- Model interpretation  
- Example prediction using the latest available data  

---

# Dataset

The dataset contains **Walmart weekly sales data** along with additional variables that influence retail demand.

### Main Columns

| Column | Description |
|------|-------------|
| Store | Store identification number |
| Date | Weekly sales date |
| Weekly_Sales | Total weekly sales |
| Holiday_Flag | Indicates holiday week |
| Temperature | Average temperature |
| Fuel_Price | Fuel price in the region |
| CPI | Consumer Price Index |
| Unemployment | Regional unemployment rate |

These variables allow the model to learn **seasonal trends, economic influence, and store-level sales patterns**.

---

# Feature Engineering

To improve forecasting performance, multiple **time-series features** were created.

## Lag Features

Lag variables allow the model to learn from past sales patterns.

- `lag_1` → sales from previous week  
- `lag_4` → sales from 4 weeks ago  
- `lag_12` → sales from 12 weeks ago  

## Rolling Statistics

Rolling averages capture short-term trends.

- `rolling_mean_4` → average sales of previous 4 weeks  

## Date Features

Time-based features help capture seasonal patterns.

- `month`
- `year`
- `week_of_year`

---

# Machine Learning Model

The forecasting model used in this project:

## Random Forest Regressor

### Reasons for choosing Random Forest

- Handles **nonlinear relationships** well  
- Robust to **noisy data**  
- Performs strongly on **tabular datasets**  
- Captures **complex interactions between features**

### Model Configuration
-n_estimators = 400
-max_depth = None
-min_samples_leaf = 2


---

# Model Evaluation

The model performance is evaluated using the following metrics:

- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**
- **R² Score**

### Additional Diagnostics

- Actual vs Predicted scatter plot  
- Residual analysis  
- Error distribution visualization  
- Feature importance analysis  

---

# Key Insights

Important observations from the trained model:

- **Store identity** is a strong predictor of weekly sales.
- **Economic indicators** such as CPI and unemployment influence retail demand.
- **Time-series lag features** capture weekly sales behavior effectively.
- Random Forest successfully models **nonlinear retail demand patterns**.

---

# Example Forecast

The project includes a final step demonstrating how to use the trained model to predict future sales using the latest available features.

Example output:
Predicted Sales: ~768,000
Actual Sales: ~760,000


This shows the model can generate **reasonably accurate short-term forecasts**.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib

---

# Project Workflow

1. Data loading and inspection  
2. Data cleaning and preprocessing  
3. Feature engineering  
4. Lag feature creation  
5. Time-based train/test split  
6. Random Forest model training  
7. Model evaluation  
8. Visualization and diagnostics  
9. Feature importance analysis  
10. Forecasting using latest data  

---

# How to Run the Project

## 1. Clone the Repository
git clone https://github.com/iamabhirammanoj/walmart-sales-forecasting-ml.git

cd walmart-sales-forecasting-ml


## 2. Install Dependencies

```bash
pip install -r requirements.txt
```

## 3. Run the Project

```bash
python walmart_sales_forecasting.py
```

---

# Project Structure

```
walmart-sales-forecasting-ml/
│
├── walmart_sales_forecasting.py
├── Walmart.csv
├── README.md
├── requirements.txt
└── .gitignore
```

---

# Future Improvements

Possible improvements to this project include:

- Using advanced models such as **XGBoost or LightGBM**
- Training **store-specific forecasting models**
- Adding **promotional or event-based features**
- Building an **interactive forecasting dashboard**

---

# Author

**Abhiram**  
Machine Learning & Data Science Enthusiast
