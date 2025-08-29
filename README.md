# ✈️ Flight Price — EDA & Feature Engineering

This repository contains a Jupyter notebook focused on **Exploratory Data Analysis (EDA)** and **Feature Engineering (FE)** for a flight price dataset.  
The goal is to understand price drivers (airline, route, stops, time-of-day, duration, etc.), clean the data, and produce model-ready features.

> Notebook: `2.0-EDA+And+FE+Flight+Price.ipynb`

---

## 🗂️ Dataset
Use the public flight price dataset from Kaggle:

- **Source:** https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction 

## 🧭 What’s inside

- **Data understanding & cleaning**
  - Inspect schema, missing values, duplicates, outliers
  - Normalize mixed types (e.g., `Duration`, date/time fields)
  - Handle rare categories & inconsistent labels

- **Exploratory visualizations**
  - Target distribution and skew
  - Price by **airline, source/destination, route, total stops**
  - Time patterns (month, weekday, hour, red-eye flags)
  - Duration vs Price relationships

- **Feature engineering**
  - Parse dates: `year`, `month`, `day`, `weekday`, `is_weekend`
  - Parse times: `dep_hour`, `arr_hour`, `is_red_eye`
  - Convert `Duration` to total minutes
  - Map `Total_Stops` to numeric (e.g., 0, 1, 2+)
  - Encode categoricals (one-hot / target-safe encodings)
  - Optional interaction features (e.g., `route_simplified`, `airline×stops`)

## ⚙️ Environment & requirements

Create and activate a virtual environment, then install libraries (Python **3.10+** recommended):

```bash
# Windows PowerShell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -U pip
pip install jupyter pandas numpy matplotlib seaborn scikit-learn openpyxl

# macOS/Linux
# python -m venv .venv
# source .venv/bin/activate
# pip install -U pip
# pip install jupyter pandas numpy matplotlib seaborn scikit-learn openpyxl
```

