# Marketing Data Cleaning & Decision Trees

A data-cleaning-heavy project on a deliberately messy marketing export, followed
by linear and tree-based modeling.

## Highlights

- **Data cleaning** on a realistic, dirty Google Ads export: typos, inconsistent
  formats, type conversions (`Cost`, `Sale_Amount` to float, `Ad_Date` to date),
  and **KNN imputation** of missing values.
- **EDA**: distributions, boxplots, outlier checks, standardization, correlation
  heatmap, scatter plots vs `Sale_Amount`.
- **Modeling**:
  - Linear regression baseline on sales.
  - **Decision Tree** regression (Google Ads) and classification (Iris).

## Datasets

| Dataset | Use | Source |
|---|---|---|
| Google Ads – Data Analytics Sales (uncleaned) | cleaning + regression | Kaggle, mirrored in [`Data_set_home`](https://github.com/gildasedenakpo-sketch/Data_set_home) |
| Iris | decision tree classification | `sklearn.datasets.load_iris()` |

```python
import pandas as pd
ads = pd.read_csv(
    "https://raw.githubusercontent.com/gildasedenakpo-sketch/Data_set_home/refs/heads/main/GoogleAds_DataAnalytics_Sales_Uncleaned.csv"
)
```

2,600 raw advertising records (Ad_ID, Campaign_Name, Clicks, Impressions, Cost,
Leads, Conversions, Conversion Rate, Sale_Amount, Ad_Date, Location, Device,
Keyword).

## Setup

```bash
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

## Author

Gildas Edenakpo — M2 Econometrics & Data Science, Aix-Marseille School of Economics.
