# MAST30034 Project 1 — Individual Submission (Harjas500)

This repository contains my submission for **MAST30034 – Applied Data Science (Project 1, 2025)**.  
The project analyses **NYC Yellow Taxi trip data (2024)** with external datasets (parks events and holidays) to study demand patterns and provide recommendations.

## Repository Structure
```
notebooks/
 └── Assignment1_ADS.ipynb
data/
 ├── parks_special_events.csv
 └── nyc_all_holidays_2024.csv
nyc_yellow_2024_run/
requirements.txt
.gitignore
README.md
```

## Setup
```bash
git clone https://github.com/MAST30034-AppliedDataScience/project-1-individual-Harjas500.git
cd project-1-individual-Harjas500
python3 -m venv venv
source venv/bin/activate
# venv\Scripts\activate   # Windows
pip install -r requirements.txt
```

## Data Sources
1. **NYC Yellow Taxi Trips (2024)**  
   New York City Taxi and Limousine Commission. TLC trip record data. Accessed August 27, 2025.  
   <https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page>

2. **NYC Parks Special Events (2024)**  
   NYC Open Data. NYC parks special events dataset. Accessed August 27, 2025.  
   <https://catalog.data.gov/dataset/parks-special-events>

3. **NYC Public Holidays (2024)**  
   Office Holidays. Public holidays in New York (2024). Accessed August 27, 2025.  
   <https://www.officeholidays.com/countries/usa/new-york/2024>

## Run the Notebook
```bash
jupyter notebook notebooks/Assignment1_ADS.ipynb
```

## Reproducibility
- Yellow Taxi parquet files are downloaded automatically when the notebook runs.  
- Parks events CSV is uploaded and cleaned in the notebook.  
- Holidays CSV was created from PDF to CSV and uploaded.  
- Figures and outputs are stored in `nyc_yellow_2024_run/`.  

