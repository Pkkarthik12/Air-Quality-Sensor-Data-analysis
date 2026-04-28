# Air Quality Sensor Data Analysis

> Analyzing real-world air quality sensor data to identify pollution patterns, detect anomalous readings, and build visual summaries for urban planning insights.

---

## Project Story

This project analyzes hourly gas sensor outputs from the **UCI Air Quality dataset** to uncover pollution trends, detect anomalies, and present findings in a dashboard-ready format — making it highly relevant for Electronics and Instrumentation Engineering students. Beyond data analysis, it covers practical sensor concepts like **drift**, **calibration limits**, **noise**, and **why anomaly detection matters** in real-world monitoring systems.

---

## Dataset

**Source:** [Kaggle — Air Quality UCI](https://www.kaggle.com/search?q=Air+Quality+UCI)

**Expected input file:** `data/AirQualityUCI.csv`

The dataset contains hourly sensor measurements including:

- Carbon Monoxide (CO)
- Nitrogen Oxides (NOx)
- Benzene
- Temperature
- Relative Humidity

---

## What This Project Does

1. Cleans raw sensor data
2. Replaces `-200` placeholder values with proper missing values (`NaN`)
3. Combines date and time columns into a unified timestamp
4. Renames columns for easier analysis
5. Explores hourly pollution behavior across the day
6. Measures correlation between pollutants and environmental factors
7. Flags anomalies using a **2 standard deviation** rule
8. Produces charts for daily and weekly trends

---

## Key Visualizations

### 1. Average Hourly Pollutant Concentration

This chart shows how CO, NOx, and Benzene concentrations vary across a 24-hour period. NOx exhibits two prominent peaks — a **morning rush hour spike (around 9:00)** and an **evening peak (around 19:00–20:00)** — consistent with urban traffic patterns. CO and Benzene remain relatively low throughout the day.



---

### 2. Correlation: Gas Sensors vs. Temperature & Humidity

The heatmap reveals strong inter-pollutant correlations. Notably:
- **CO sensor and Benzene reference** show a high positive correlation (0.89), suggesting a common emission source.
- **CO sensor and NOx sensor** are strongly negatively correlated (−0.77), which may reflect sensor cross-sensitivity or differing emission dynamics.
- **Temperature and Humidity** show moderate negative correlation (−0.58), as expected.
- Gas sensors are largely **independent of temperature and humidity**, indicating stable sensor behavior under varying environmental conditions.

![Correlation: Gas Sensors vs Temperature and Humidity](outputs/Temperature_and_humidity.png)

---

### 3. CO Sensor Anomaly Detection

Anomalies are flagged when a CO sensor reading exceeds **2 standard deviations** above the mean (threshold: **1538.9**). The chart highlights frequent spikes in the period of March 10–27, 2004, pointing to real pollution events or possible sensor instability.

![CO Sensor Anomaly Detection](outputs/Co2_sensor.png)

---

## Folder Structure

```
.
├── README.md
├── requirements.txt
├── data/
│   └── AirQualityUCI.csv        # Download manually from Kaggle
└── outputs/
    ├── Pollutant_data.png
    ├── Temperature_and_humidity.png
    ├── Co2_sensor.png
    └── summary.csv
```

---

## Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
```
## License

This project uses the [UCI Air Quality Dataset](https://archive.ics.uci.edu/ml/datasets/Air+Quality), which is publicly available for research and educational use.
