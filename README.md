# Sales-Forecasting-Project

📌 Overview
This project focuses on building an end-to-end sales forecasting pipeline using time series models. The goal was to clean and analyze raw sales transaction data, explore patterns, and forecast future sales using ARIMA and Prophet models.

🔎 What Was Done
1. Data Preprocessing & Cleaning
* Imported raw sales transaction data (CSV).
* Removed outliers using the IQR method.
* Aggregated data into daily and monthly sales.
* Exported cleaned datasets:
- cleaned_sales_data.csv
- monthly_sales_data.csv
- forecasted_sales.csv
- sales_forecasting.db (SQLite database for reusability).

2. Exploratory Data Analysis (EDA)
* Conducted trend analysis with line plots and bar charts.
* Summarized sales distribution with descriptive statistics.
* Performed seasonal decomposition into trend, seasonality, and residuals.

3. Forecasting Models
* Implemented ARIMA model as a baseline.
* Conducted grid search for ARIMA hyperparameters (p,d,q) to optimize performance.
* Built Facebook Prophet model to capture seasonality and trend shifts.
* Compared model accuracy using Mean Absolute Error (MAE):
- Baseline ARIMA: ≈ 19,134
- Optimized ARIMA: ≈ 18,825
- Prophet: ≈ 13,720 (best performing model)

4. Model Evaluation & Visualization
* Plotted actual vs forecasted sales for all models.
* Analyzed residuals to validate error distribution.
* Visualized future forecasts with Prophet’s uncertainty intervals.

5. Storage & Reusability
* Exported cleaned, monthly, and forecasted results to CSV & SQL database.
* Built a structured pipeline for reproducibility and future reporting.

🛠️ Tech Stack & Libraries
* Programming Language: Python
* Libraries: Pandas, Matplotlib, Statsmodels, Scikit-learn, Prophet, NumPy
* Database: SQLite

📈 Results
* Prophet achieved the lowest MAE (13,720), making it the most reliable for capturing seasonality and trends in sales.
* The project outputs multiple datasets and forecasts for further business intelligence integration.

📌 Key Takeaways
* Built a full pipeline: data cleaning → EDA → modeling → evaluation → storage.
* Compared statistical and machine learning approaches to time series forecasting.
* Achieved best performance with Prophet, useful for business planning and decision-making.
