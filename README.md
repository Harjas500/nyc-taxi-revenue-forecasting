# NYC Taxi Revenue Forecasting

An end-to-end data science project analysing 2024 New York City Yellow Taxi trip data to identify revenue patterns, understand the influence of external events, and forecast taxi revenue using machine learning.

## Project Overview

This project explores NYC Yellow Taxi trip data from 2024, combining trip records with public holiday and NYC Parks special event datasets to investigate factors influencing taxi revenue.

The workflow covers data preprocessing, exploratory data analysis (EDA), feature engineering, and predictive modelling. Linear Regression and Random Forest models are developed and evaluated to compare their ability to forecast taxi revenue.

## Objectives

- Analyse taxi revenue patterns across different hours, days, and months.
- Investigate the relationship between public holidays, special events, and taxi revenue.
- Explore spatial and temporal patterns in taxi activity.
- Develop and evaluate machine learning models for revenue forecasting.

## Repository Structure

```text
nyc-taxi-revenue-forecasting/
│
├── notebooks/
│   └── Assignment1_ADS.ipynb
│
├── data/
│   ├── Parks_Special_Events.csv
│   └── nyc_all_holidays_2024.csv
│
├── nyc_yellow_2024_run/
│   ├── figures/
│   ├── logs/
│   ├── tables/
│   ├── taxi_zones_shp/
│   └── metrics_summary.txt
│
├── requirements.txt
├── .gitignore
└── README.md
```

## Data Sources

The analysis uses the following datasets:

1. **NYC Yellow Taxi Trip Records (2024)**  
   New York City Taxi and Limousine Commission (TLC).  
   [TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

2. **NYC Parks Special Events**  
   NYC Open Data.  
   [NYC Parks Special Events Dataset](https://catalog.data.gov/dataset/parks-special-events)

3. **NYC Public Holidays (2024)**  
   Office Holidays.  
   [New York Public Holidays 2024](https://www.officeholidays.com/countries/usa/new-york/2024)

## Methodology

### 1. Data Preprocessing
- Processed NYC Yellow Taxi trip records using PySpark.
- Cleaned and prepared external parks events and public holiday datasets.
- Integrated relevant datasets to support further analysis.

### 2. Exploratory Data Analysis
- Examined revenue distributions and temporal trends.
- Analysed hourly and daily revenue patterns.
- Investigated holiday and special event effects.
- Explored spatial patterns across taxi zones.

### 3. Feature Engineering
Developed features including:
- Hour, day, and month of trip.
- Trip duration and tip percentage.
- Public holiday indicators.
- Special event indicators.

### 4. Machine Learning Models
Developed and evaluated two regression models:

- **Linear Regression** – used as a baseline predictive model.
- **Random Forest Regressor** – used to capture more complex relationships in the data.

The training data covered January–October 2024, with November–December 2024 used for testing.

## Model Performance

The following results are reported in the project evaluation:

| Model | RMSE | MAE | R² |
|---|---:|---:|---:|
| Linear Regression | 25,480 | 16,070 | 0.672 |
| Random Forest | 11,533 | 4,443 | 0.933 |

The Random Forest model achieved stronger performance across all three reported evaluation metrics, indicating a better fit to the test data than the Linear Regression baseline.

## Technologies Used

- **Programming:** Python
- **Big Data Processing:** PySpark
- **Data Analysis:** Pandas, NumPy
- **Visualisation:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Development:** Jupyter Notebook

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Harjas500/nyc-taxi-revenue-forecasting.git
cd nyc-taxi-revenue-forecasting
```

### 2. Create and activate a virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

For Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the notebook

```bash
jupyter notebook notebooks/Assignment1_ADS.ipynb
```

## Reproducibility

- NYC Yellow Taxi Parquet files are downloaded automatically when the notebook runs.
- The parks events dataset is loaded and cleaned during notebook execution.
- The 2024 public holidays dataset is provided in the `data/` directory.
- Generated figures, tables, logs, and evaluation summaries are stored in `nyc_yellow_2024_run/`.

---

**Author:** Harjas Singh  
**GitHub:** [Harjas500](https://github.com/Harjas500)
