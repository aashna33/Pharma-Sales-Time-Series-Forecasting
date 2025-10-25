💊 Pharma Sales Analysis and Forecasting

A comprehensive time series forecasting project analyzing historical pharmaceutical sales (2014 – 2019) and predicting future sales trends for multiple drug categories using SARIMAX and Prophet models.

📘 Project Overview

This project addresses the challenges of sales forecasting in the pharmaceutical domain — where data can exhibit strong seasonality, trends, and randomness.
By performing deep time series analysis and building forecasting models, it aims to help pharma distributors and analysts make data-driven inventory and marketing decisions.



Forecasting Models used:

Model	Description

SARIMAX	Seasonal ARIMA with exogenous features; captures trend + seasonality

Prophet	Facebook’s forecasting model for business time series data

✅ SARIMAX performed best for stable series with seasonality
✅ Prophet performed best for non-stationary, trend-driven series

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

jupyter notebook main.ipynb

Or run via command line:

python main.ipynb


💡 Insights & Takeaways

Clear seasonal sales peaks observed annually for certain drug categories.

SARIMAX captures cyclical patterns effectively.

Prophet adapts better to irregular sales behavior.

Forecasting helps optimize inventory management and supply planning.


🧰 Technologies Used

Python 3.10+

Pandas, NumPy

Matplotlib, Seaborn

Statsmodels (SARIMAX)

Prophet (Meta)

scikit-learn
