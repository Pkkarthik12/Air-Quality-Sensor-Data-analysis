Air Quality Sensor Data Analysis
This project analyzes real-world air quality sensor data from the UCI Air Quality dataset to identify pollution patterns, detect anomalous readings, and build visual summaries that could help city planners understand urban air conditions.

Project Story
"I analyzed real-world air quality sensor data to identify pollution patterns, detect anomalies, and build a dashboard for city planners."

This project is especially useful for an Electronics and Instrumentation Engineering student because the dataset comes from gas sensor outputs. Alongside data analysis, you can discuss sensor drift, calibration limits, noise, and why anomaly detection matters in real monitoring systems.

Dataset
Source: Kaggle search for Air Quality UCI

Expected input file:

data/AirQualityUCI.csv
The dataset contains hourly sensor measurements such as:

CO
NOx
Benzene
Temperature
Relative humidity
What This Project Does
Cleans the raw sensor data
Replaces -200 placeholder values with missing values
Combines date and time into a proper timestamp
Renames columns for easier analysis
Explores hourly pollution behavior
Measures correlation between pollutants
Flags anomalies using a 2 standard deviation rule
Produces charts for daily and weekly trends
Folder Structure
.
|-- README.md
|-- requirements.txt
|-- src/
|   `-- air_quality_analysis.py
|-- data/
|   `-- AirQualityUCI.csv   # add this manually after download
`-- outputs/
    `-- generated plots and summary csv files
