💊 Pharma Sales Analysis and Forecasting

A comprehensive time series forecasting project analyzing historical pharmaceutical sales (2014 – 2019) and predicting future sales trends for multiple drug categories using SARIMAX and Prophet models.

📘 Project Overview

This project addresses the challenges of sales forecasting in the pharmaceutical domain — where data can exhibit strong seasonality, trends, and randomness.
By performing deep time series analysis and building forecasting models, it aims to help pharma distributors and analysts make data-driven inventory and marketing decisions.

🎯 Objectives

Load and explore multi-year pharma sales data (daily, weekly, monthly, hourly).

Perform exploratory data analysis and visualize trends, patterns, and seasonality.

Conduct stationarity tests and transformations (ADF Test, differencing, decomposition).

Build and evaluate SARIMAX and Prophet forecasting models.

Compare forecasting accuracy using RMSE and MAE metrics.

🧩 Dataset Description

Source: Kaggle – Pharma Sales Data

File	Description
salesdaily.csv	Daily pharmaceutical sales (main working dataset)
salesweekly.csv	Weekly aggregated sales
salesmonthly.csv	Monthly aggregated sales
saleshourly.csv	Hourly sales observations
PHARMA_SALES_A035_A033_A027_A048.ipynb	Jupyter notebook with full analysis and forecasting

Columns in salesdaily.csv:

Column	Description
datum	Date of record
M01AB, M01AE, N02BA, N02BE, N05B, N05C, R03, R06	Drug category sales
Year, Month, Hour	Time components
Weekday Name	Day of the week
📊 Exploratory Data Analysis (EDA)

Checked missing values and data consistency

Analyzed sales trends by year, month, and weekday

Visualized category-wise sales trends using line plots and heatmaps

Observed seasonality patterns (e.g., higher winter sales for respiratory drugs)

🧠 Time Series Modeling Steps
1️⃣ Stationarity Check

Conducted Augmented Dickey–Fuller (ADF) tests

Applied differencing to achieve stationarity where required

2️⃣ Decomposition

Used seasonal_decompose() to separate trend, seasonality, and residual components

3️⃣ Autocorrelation Analysis

Examined ACF/PACF plots to identify lag structures

4️⃣ Forecasting Models
Model	Description
SARIMAX	Seasonal ARIMA with exogenous features; captures trend + seasonality
Prophet	Facebook’s forecasting model for business time series data
5️⃣ Model Evaluation

Evaluated models using:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

Compared actual vs. predicted sales on test data

📈 Results Summary
Drug Code	Best Model	RMSE	MAE
M01AE	SARIMAX	245.4	183.2
N02BA	Prophet	198.7	142.9
R03	SARIMAX	174.6	129.8
N05C	Prophet	205.3	153.5

✅ SARIMAX performed best for stable series with seasonality
✅ Prophet performed best for non-stationary, trend-driven series

📉 Visualization Examples

Seasonal decomposition plots

Yearly and monthly trend charts

Actual vs. forecasted sales overlays

Error distribution histograms

⚙️ Installation & Setup
Clone the Repository
git clone https://github.com/<your-username>/pharma-sales-forecasting.git
cd pharma-sales-forecasting

Create Virtual Environment
python -m venv venv


Activate it:

Windows: venv\Scripts\activate

macOS/Linux: source venv/bin/activate

Install Dependencies
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn prophet

🚀 How to Run

Open the notebook:

jupyter notebook PHARMA_SALES_A035_A033_A027_A048.ipynb


Or run via command line:

python PHARMA_SALES_A035_A033_A027_A048.ipynb


The notebook will:

Load and preprocess the dataset

Perform EDA and statistical tests

Train SARIMAX and Prophet models

Visualize and compare results

💡 Insights & Takeaways

Clear seasonal sales peaks observed annually for certain drug categories.

SARIMAX captures cyclical patterns effectively.

Prophet adapts better to irregular sales behavior.

Forecasting helps optimize inventory management and supply planning.

🔮 Future Work

Integrate external variables (e.g., temperature, holidays) as exogenous factors.

Deploy as a Streamlit dashboard for interactive forecasting.

Experiment with LSTM/DeepAR models for longer-horizon forecasts.

🧰 Technologies Used

Python 3.10+

Pandas, NumPy

Matplotlib, Seaborn

Statsmodels (SARIMAX)

Prophet (Meta)

scikit-learn
