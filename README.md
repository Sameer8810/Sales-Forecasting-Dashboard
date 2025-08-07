# 🛍️ Sales Forecasting Dashboard 📈

A complete **Data Analytics & Machine Learning** project to forecast weekly retail sales using time-series and regression models. This project demonstrates a practical data science pipeline: from **data collection and cleaning** to **modeling, visualization, and evaluation**, culminating in a business-ready forecast dashboard.

---

## 📚 Project Summary

| Stage | Description |
|-------|-------------|
| 🗂️ Day 1 | Data loading, merging, and exploratory analysis |
| 🔍 Day 2 | In-depth EDA and time-based trend insights |
| 🧼 Day 3 | Data preprocessing, missing value handling, and feature extraction |
| 🧪 Day 4 | Time-based train-test split (pre-July 2012 vs post-July 2012) |
| 🧠 Day 5 | Model training (Random Forest) and basic predictions |
| 📉 Day 6 | Actual vs Predicted graphing, saving forecast results |
| 🧪 Day 7 | Error analysis using MAE, MAPE, visual diagnostics |

---

## 🔧 Tools & Technologies

- **Language**: Python  
- **Libraries**: `pandas`, `matplotlib`, `seaborn`, `scikit-learn`  
- **Model**: `RandomForestRegressor`  
- **Development**: Jupyter Notebook  
- **Data Source**: Walmart Kaggle Dataset  

---

## 🗃️ Datasets Used

- `train.csv`: Weekly sales of departments across stores  
- `features.csv`: Includes macroeconomic and holiday information  
- `stores.csv`: Metadata about store type and size  

---

## 🔑 Features Used

| Feature         | Description                             |
|----------------|-----------------------------------------|
| `Store`         | Store ID                                |
| `Dept`          | Department number                       |
| `Type`          | Store category (A, B, C)                |
| `Size`          | Store size in square feet              |
| `Temperature`   | Weekly average temperature              |
| `Fuel_Price`    | Weekly fuel price                       |
| `CPI`           | Consumer Price Index                    |
| `Unemployment`  | Unemployment rate                       |
| `IsHoliday`     | Boolean flag for holidays               |
| `Month`, `Week`, `Year` | Extracted from `Date` column   |

---

## 🧠 Modeling Approach

- **Target Variable**: `Weekly_Sales`  
- **Train-Test Split**: Based on time (`train < 2012-07-01`, `test >= 2012-07-01`)  
- **Model**: `RandomForestRegressor(n_estimators=100, random_state=42)`  

---

## 📈 Forecast Output

After model training, we generate forecasts and save them to:

**Actual vs Predicted Sales (Visualization):**
A time-series line graph compares true vs forecasted sales, helping visually assess accuracy.

---

## 🧮 Error Analysis

Metrics used:
- **MAE (Mean Absolute Error)**
- **MAPE (Mean Absolute Percentage Error)**
- **Absolute Error distribution**
- **Graphical analysis over time**

**Sample Forecast Table:**

| Date       | Actual | Predicted | Error | APE (%) |
|------------|--------|-----------|-------|---------|
| 2012-07-01 | 20000  | 19800     | 200   | 1.00    |
| 2012-07-08 | 22000  | 21500     | 500   | 2.27    |
| ...        | ...    | ...       | ...   | ...     |

---

## 🧠 Key Insights from EDA

- **Store Type A** consistently performs better in terms of weekly sales.
- **Holiday weeks** show either high peaks or sharp drops — needs special treatment.
- **Sales trends are seasonal**, with visible spikes during certain months.
- **Economic indicators like CPI and Unemployment** vary, but their predictive power can be explored further.

---

## 📁 Project Structure

Sales Forecasting Dashboard/
│
├── data/
│ ├── features.csv
│ ├── stores.csv
│ └── train.csv
│
├── notebook/
│ ├── sales_forecasting.ipynb
│ └── forecast_output.csv
│
├── images/
│ ├── sales_predictions.png
│ ├── error_plot.png
│ └── actual_vs_predicted.png
│
└── README.md

yaml
Copy
Edit

---

## 🚀 What's Next?

### ✅ Planned for Upcoming Days:

- [ ] Add **lag features** (e.g., `Sales_last_week`, `Sales_last_month`)
- [ ] Engineer **rolling averages** (e.g., 3-week/5-week moving average)
- [ ] Incorporate **holiday proximity** effects
- [ ] Try **XGBoost** or **LightGBM**
- [ ] Perform **hyperparameter tuning**
- [ ] Deploy a **Streamlit dashboard** or use **Plotly Dash** for interactivity

---

## 🎯 Final Goal

Build a fully deployable **Sales Forecasting Dashboard** that:
- Forecasts sales per department
- Visualizes trends and errors
- Informs inventory and staffing decisions
