# Sales & Demand Forecasting for Businesses
### Future Interns — Machine Learning Task 1 (2026)

A sales/demand forecasting system built on 3 years of daily retail sales data — with data
cleaning, time-based feature engineering, regression-based forecasting (Linear Regression vs
Random Forest), model evaluation, and business-friendly visualizations for the next 90 days.

**Result:** ~4.2% average forecast error (MAPE), R² = 0.85 on held-out validation.

## Contents
- `Sales_Demand_Forecasting.ipynb` — full notebook (data → cleaning → features → model → forecast → charts)
- `forecasting_pipeline.py` — same pipeline as a plain Python script
- `Business_Report.md` — non-technical summary: what the forecast means and how to use it for planning
- `data/` — cleaned sales data, 90-day forecast, model comparison metrics
- `charts/` — all visualizations

## How to run
```bash
pip install pandas numpy matplotlib scikit-learn
python forecasting_pipeline.py
# or open Sales_Demand_Forecasting.ipynb in Jupyter
```

## Using your own data
Swap the dataset-generation cell for `pd.read_csv("your_data.csv")` — the cleaning, feature
engineering, modeling, and forecasting steps work unchanged as long as you have a date column
and a sales column.

---
Built as part of the Machine Learning Fellowship Program at Future Interns.# FUTURE_ML_01
