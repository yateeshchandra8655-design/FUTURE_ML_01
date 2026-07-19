# Sales & Demand Forecast — Business Summary

**Prepared for:** Retail business owner / manager
**Prepared by:** Upputuri Yateesh Chandra Bharani — Future Interns ML Fellowship, Task 1
**Data window:** 3 years of daily sales history · **Forecast horizon:** next 90 days

## What was built
A machine learning model that studies 3 years of daily sales — across regions and product
categories — and predicts what sales will look like over the next 90 days. It automatically
picks up on the patterns that matter to a business: which days of the week sell more, which
months are seasonally stronger, and the overall growth trend.

## How accurate is it?
On the most recent 90 real days (data the model never trained on), the forecast was off by an
average of **~4.2%** per day (MAPE), and explained **~85%** of the day-to-day variation in sales
(R² = 0.85). For daily-level retail forecasting, that's a strong, usable result — accurate enough
to plan against, while still leaving room for real-world surprises.

## What the forecast shows
- **Trend:** the business is on a steady, gradual growth path.
- **Weekly pattern:** weekends consistently outsell weekdays.
- **Seasonality:** sales dip slightly over summer and build toward a clear peak around
  November–December (holiday season).
- **Next 90 days:** total forecasted sales of roughly **$540K**, averaging about **$6,000/day**,
  with a ±10% planning band to account for normal demand fluctuation.

## How to use this for planning
| Business need | How the forecast helps |
|---|---|
| **Inventory** | Order more stock ahead of forecasted high-demand weeks instead of reacting to a stockout after the fact. |
| **Cash flow** | Anticipate slower periods (e.g. summer) and plan spending/credit needs around them. |
| **Staffing** | Schedule extra staff on days/weeks the model flags as high-traffic (weekends, holiday run-up). |
| **Promotions** | If actual sales start tracking below the forecast band, that's an early warning sign to launch a promotion rather than waiting for month-end numbers. |

## Files in this project
- `Sales_Demand_Forecasting.ipynb` — full notebook: data cleaning → features → model → forecast → charts
- `forecasting_pipeline.py` — same pipeline as a plain Python script
- `data/clean_daily_sales.csv` — cleaned historical daily sales
- `data/future_90day_forecast.csv` — the 90-day forecast
- `data/model_results.csv` — model comparison (MAE / RMSE / MAPE / R²)
- `charts/` — all visualizations, ready to drop into a slide deck

## Notes on the data
This project uses a simulated dataset built to mirror the structure of real retail datasets
(comparable to Kaggle's Superstore / Store Sales Time-Series Forecasting datasets) — same kind of
fields (date, region, category, sales), same kinds of real-world messiness (missing values,
duplicates, bad entries), and realistic trend/seasonality patterns. **To use this on your own
business**, swap the dataset-generation cell in the notebook for `pd.read_csv("your_data.csv")` —
the cleaning, feature engineering, modeling, and forecasting steps all work unchanged as long as
you have a date column and a sales column.
