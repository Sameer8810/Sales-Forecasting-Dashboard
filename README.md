# 🛍️ Sales Forecasting Dashboard 📈

A comprehensive **Data Analytics & Machine Learning** project to forecast weekly retail sales using time-series and regression models. This project covers the full pipeline: from **data collection and cleaning** to **model training, evaluation**, and **forecast visualization**, culminating in business-ready outputs for dashboards.

---

## 📚 Project Summary

| Stage      | Description                                   |
|------------|-----------------------------------------------|
| 🗂️ Day 1   | Data loading, merging, and exploratory analysis |
| 🔍 Day 2   | In-depth exploratory data analysis (EDA) and time-based trend insights |
| 🧼 Day 3   | Data preprocessing, handling missing values, feature engineering |
| 🧪 Day 4   | Time-based train-test split (pre-July 2012 vs post-July 2012) |
| 🧠 Day 5   | Model training (Random Forest) and initial predictions |
| 📉 Day 6   | Visualization of Actual vs Predicted sales and saving forecast results |
| 🧪 Day 7   | Error analysis with MAE, MAPE, and diagnostic plots |
| 🧪 Day 8   | Multi-model training: Linear Regression, Random Forest, XGBoost, LightGBM |
| 📊 Day 9   | Model comparison and feature importance visualization |
| 🚀 Day 10  | Export final results for Power BI/Tableau dashboards and prepare README |

---

🔑 Features
Feature	Description
Store	Store ID
Dept	Department number
Type	Store category (encoded A, B, C)
Size	Store size (square feet)
Temperature	Weekly average temperature
Fuel_Price	Weekly fuel price
CPI	Consumer Price Index
Unemployment	Unemployment rate
IsHoliday	Boolean holiday flag
Month, Week, Year	Extracted from Date column

🧠 Modeling Approach
Target Variable: Weekly_Sales

Train-Test Split: Time-based (train < 2012-07-01, test >= 2012-07-01)

Models Used:

Linear Regression

Random Forest Regressor

XGBoost

LightGBM

Hyperparameter tuning applied to optimize Random Forest.

📈 Forecast Output & Error Analysis
Visualized actual vs predicted sales trends over time.

Calculated key error metrics:

MAE (Mean Absolute Error)

RMSE (Root Mean Squared Error)

R² Score (Coefficient of Determination)

APE (Absolute Percentage Error)

Exported results in notebook/forecast_output.csv with columns:
| Date | Store | Dept | Actual_Sales | Predicted_Sales | Absolute_Error | APE (%) |

🧠 Key Insights from EDA
Store Type A consistently leads in weekly sales performance.

Sales during holiday weeks show notable peaks or troughs, warranting special consideration.

There is strong seasonality in sales with spikes in particular months.

Macroeconomic variables like CPI and Unemployment may impact sales trends.

🖥️ Dashboard Status
Core modeling and evaluation completed successfully.

Exported CSV ready for importing into BI tools like Power BI and Tableau for advanced visualization.

Interactive dashboard (Streamlit/Plotly Dash) under development.

📁 Project Structure
kotlin
Copy
Edit
Sales Forecasting Dashboard/
│
├── data/
│   ├── features.csv
│   ├── stores.csv
│   └── train.csv
│
├── notebook/
│   ├── sales_forecasting.ipynb
│   └── forecast_output.csv
│
├── images/
│   ├── sales_predictions.png
│   ├── error_plot.png
│   └── actual_vs_predicted.png
│
├── requirements.txt
│
└── README.md
📦 Dependencies
The following packages are required (see requirements.txt):

nginx
Copy
Edit
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
lightgbm
streamlit  

🚀 Future Work & Roadmap
Add lag and rolling window features (e.g., Sales_last_week, moving averages).

Include holiday proximity effects in feature engineering.

Extend hyperparameter tuning for XGBoost and LightGBM.

Develop and deploy a Streamlit-based interactive dashboard.

Explore real-time data streaming and alerting features.

📝 License & Data Usage
Data is sourced from the Walmart Kaggle Competition.

Please adhere to Kaggle's licensing and data use policies.

📬 Contact
For questions, feedback, or collaboration, feel free to reach out:
Sameer
sameer.developer0001@gmail.com (www.linkedin.com/in/sameer-khan-621ba422b)
