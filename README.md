# VigilAI
VigilAI is a real-time crime analysis and prediction system that detects patterns, connects possibly related crimes, and identifies emerging hotspots using data-driven intelligence.



## Problem Statement
Crime systems are reactive, not predictive → action starts after damage is done
Rising urban crime is worsened by delayed detection and manual analysis
Emerging hotspots go unnoticed until they escalate
No real-time intelligence → slow response, poor resource use
Dashboards show data, not connections → patterns stay hidden
Missed patterns today become crimes tomorrow



## Proposed Solution
Analyzes crime data as interconnected signals rather than isolated incidents
Detects key indicators: crime spikes, pattern clusters, and hotspot intensity
Identifies trends, emerging threats, and hidden connections in real time
Provides a dynamic, continuously updating view for faster and smarter decision-making



## Features
| Tab            | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| Weekly Spikes  | Z-score–based anomaly detection on weekly crime volumes                    |
| District Map   | Interactive Folium map with pulse-ring animations and "crime web" lines    |
| Breakdown      | Category, day-of-week, and hour-level crime breakdowns                     |
| Clusters       | KMeans geographical hotspot clustering                                     |
| Explainer      | Actionable intelligence panel with recommended patrol actions              |


- Crime hotspots represented as dynamic nodes (dots) Size = intensity of crime Green = Low Risk Yellow = Medium Risk Red = High Risk
- Pattern-based connections between similar crimes
- Web-like visualization on real geographic maps
- Identification of connected crime networks
- Real-time crime surge detection with pulse/vibration effect
- Alerts for nearby at-risk zones

## Setup

### 1. Clone the repo
```bash
git clone https://github.com/ariguchi/VigilAI.git
cd VigilAI
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add the dataset
Download the **San Francisco Crime Classification** dataset from [Kaggle](https://www.kaggle.com/competitions/sf-crime/data) and place `train.csv` in the `data/` folder:
```
data/
  train.csv
```

> ⚠️ The data files are **not included** in this repo due to their large size (~200 MB).

### 4. Run the app
```bash
streamlit run app.py
```

---

## Project Structure
_
```
VigilAI/
├── app.py                          # Main Streamlit dashboard
├── requirements.txt                # Python dependencies
├── notebooks/
│   ├── VigilAI_Crime_Analysis.ipynb   # Full EDA notebook
│   ├── ArachneX_analysis.ipynb          # Supplementary analysis
│   ├── cluster_map.png
│   ├── district_ranking.png
│   ├── heatmap_day_hour.png
│   ├── weekly_crime_dashboard.png
│   └── ...
└── data/                           # (not tracked — add your CSVs here)
    └── train.csv
```

---

## Tech Stack

- **Streamlit** — Dashboard framework
- **Pandas / NumPy** — Data wrangling
- **Matplotlib / Seaborn** — Static charting
- **Folium + streamlit-folium** — Interactive maps
- **scikit-learn** — KMeans clustering
- **SciPy** — Z-score statistical anomaly detection

---

## Dataset

[SF Crime Classification — Kaggle](https://www.kaggle.com/competitions/sf-crime/data)  
San Francisco Police Department incident records from 2003–2015.

---

