#  Retail Sales Forecasting using Machine Learning

##  Project Overview

This project develops an end-to-end machine learning pipeline to forecast daily retail sales using historical sales data. The objective is to predict future sales accurately while comparing multiple machine learning algorithms and identifying the most effective model.

The project covers the complete data science workflow, including data preprocessing, feature engineering, exploratory data analysis, model development, evaluation, and business insights.

---

##  Objectives

- Forecast daily retail sales using historical data.
- Engineer meaningful time-series features.
- Compare multiple machine learning algorithms.
- Select the best-performing model.
- Extract business insights from the results.

---

## Dataset

The project uses the **Store Item Demand Forecasting Challenge** dataset.

Each record contains:

- Date
- Store ID
- Item ID
- Daily Sales

Target variable:

- **Sales**

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- Joblib

---

##  Exploratory Data Analysis

The following analyses were performed:

- Data exploration
- Missing value analysis
- Daily sales trend visualization
- Monthly sales analysis
- Feature importance analysis
- Residual analysis

---

##  Feature Engineering

Several predictive features were created from the original dataset.

### Time Features

- Year
- Month
- Day
- Day of Week
- Quarter

### Time-Series Features

- Previous day's sales (Lag 1)
- 7-Day Rolling Mean
- 7-Day Rolling Standard Deviation

These features allow the models to capture historical sales behaviour and seasonal trends.

---

##  Machine Learning Models

Three regression models were trained and evaluated.

### 1. Linear Regression

Used as a baseline model.

### 2. Random Forest Regressor

Used to capture non-linear relationships and interactions between variables.

### 3. XGBoost Regressor

Gradient boosting model used to improve prediction accuracy by sequentially correcting previous errors.

---

## 📈 Model Performance

| Model | MAE | RMSE | R² |
|------|------:|------:|------:|
| Linear Regression | 6.78 | 8.79 | 0.9067 |
| Random Forest | 6.15 | 7.99 | 0.9229 |
| **XGBoost** | **5.97** | **7.74** | **0.9275** |

### Best Model

 **XGBoost**

The XGBoost model achieved the highest predictive accuracy with an R² score of approximately **92.8%**, outperforming both Linear Regression and Random Forest.

---

##  Feature Importance

Feature importance analysis showed that historical sales behaviour was the strongest predictor.

Top features included:

- 7-Day Rolling Mean
- Day of Week
- 7-Day Rolling Standard Deviation
- Previous Day Sales

This indicates that recent sales trends are highly informative when forecasting future demand.

---

## Business Insights

The analysis produced several business insights:

- Retail sales exhibit strong seasonal behaviour.
- Recent sales history is the most important predictor of future sales.
- Weekly purchasing patterns significantly influence demand.
- Ensemble models outperform traditional linear models.
- Accurate forecasting can support inventory planning and operational decision-making.

---

##  Limitations

Although the model performed well, several limitations remain.

- Holiday effects were not included.
- Promotional campaigns were unavailable.
- Weather data was not available.
- Future demand may change due to external market conditions.

---

##  Future Improvements

Potential improvements include:

- Hyperparameter tuning using GridSearchCV.
- Adding holiday and promotional features.
- Incorporating weather information.
- Deploying the model using Streamlit or Flask.
- Evaluating deep learning approaches such as LSTM for time-series forecasting.

---

##  Project Structure

```
Retail-Sales-Forecasting-ML/
│
├── data/
│   └── train.csv
│
├── notebooks/
│   └── Retail_Sales_Forecasting.ipynb
│
├── models/
│   └── xgboost_revenue_forecasting_model.pkl
│
├── README.md
└── requirements.txt
```

---

##  Visualisations

The project includes:

- Daily Sales Trend
- Average Monthly Sales
- Feature Importance
- Residual Plot
- Actual vs Predicted Sales

---

## Author

**Ueda Shehu**

MSc Applied Artificial Intelligence and Data Analytics

University of Bradford

GitHub: https://github.com/Wedashehu12

---

## Summary

This project demonstrates a complete machine learning workflow for retail sales forecasting, from raw data to model deployment preparation. By comparing Linear Regression, Random Forest, and XGBoost, the project identifies XGBoost as the most accurate forecasting model while providing actionable business insights from historical sales data.
