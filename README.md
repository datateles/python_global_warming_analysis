# **Global Warming Data Analysis: Climate Trends & Insights**
🌍 *Analyzing global climate trends using descriptive analytics and data visualization.*

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Dataset Description](#dataset-description)
3. [Analysis Steps](#analysis-steps)
4. [Pyhton Code](#python-code)
5. [Key Findings](#key-findings)

---

## **1. Project Overview**
This project focuses on analyzing global warming patterns using data visualization and descriptive analytics. The dataset used contains various environmental and socio-economic indicators for different countries over several years. The goal is to understand trends, correlations, and patterns related to global warming.

---

## **2. Dataset Description**
The dataset consists of **100,000 records** across **26 columns**, covering multiple **countries and years** in a time range between 1900 and 2023.

| Feature                         | Description |
|----------------------------------|-------------|
| **Country**                        | Name of the country |
| **Year**                           | Year of observation |
| **Temperature_Anomaly**            | Deviation from global average temperature (°C) |
| **CO2_Emissions**                  | Total CO2 emissions (metric tons) |
| **Population**                     | Total population |
| **Forest_Area**                    | Percentage of land covered by forests |
| **GDP**                            | Gross Domestic Product (USD) |
| **Renewable_Energy_Usage**         | % of total energy from renewable sources |
| **Methane_Emissions**             | Annual methane emissions (metric tons) |
| **Sea_Level_Rise**                 | Rise in sea level (cm) |
| **Arctic_Ice_Extent**             | Arctic ice extent (million km²) |
| **Urbanization**                   | % of population in urban areas |
| **Deforestation_Rate**            | Annual deforestation rate (%) |
| **Extreme_Weather_Events**        | Number of extreme weather events per year |
| **Average_Rainfall**              | Annual average rainfall (mm) |
| **Solar_Energy_Potential**        | Solar energy production potential (kWh/m²/day) |
| **Waste_Management**              | Waste management index (0-100) |
| **Per_Capita_Emissions**         | CO2 emissions per person (metric tons) |
| **Industrial_Activity**           | Industrial development index (0-100) |
| **Air_Pollution_Index**           | Air pollution index (higher = worse) |
| **Biodiversity_Index**            | Biodiversity health index (0-100) |
| **Ocean_Acidification**           | Ocean pH changes (lower = more acidic) |
| **Fossil_Fuel_Usage**             | % of energy from fossil fuels |
| **Energy_Consumption_Per_Capita** | kWh consumed per person |
| **Policy_Score**                  | Environmental policy effectiveness (0-100) |
| **Average_Temperature**           | Average global temperature (°C) |

---

## **3. Analysis Steps**
Data was analyzed using **Python (Pandas, NumPy, Seaborn, Matplotlib)**.

✅ **Step 1: Data Collection**  
➡ Load the dataset and perform an initial inspection to understand its structure and identify any missing values or anomalies.

✅ **Step 2: Descriptive Statistics**  
➡ Calculate basic descriptive statistics to summarize the data.

✅ **Step 3: Data Visualization**  
➡ Create visualizations to explore relationships between variables and identify patterns.  

✅ **Step 4: Correlation Analysis**  
➡ Analyze the correlation between different variables to understand their relationships.

---

## **4. Python Code**
### Data Collection
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
data = pd.read_csv('global_warming.csv')

# Display the first few rows of the dataset
print(df.head())

# Check for missing values
print(df.isnull().sum())

# Basic information about the dataset
print(df.info())

# Handle missing values
# Good for time-series data
data.ffill(inplace=True)

# Normalize numerical data
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()
numerical_columns = data.select_dtypes(include=[np.number]).columns
data[numerical_columns] = scaler.fit_transform(data[numerical_columns])

# Display the first few rows of the dataset
print(data.head())
```

### Descriptive Statistics
```python
# Descriptive Statistics
print("Mean Values:")
print(data.mean(numeric_only=True))

print("\nMedian Values:")
print(data.median(numeric_only=True))

print("\nStandard Deviation:")
print(data.std(numeric_only=True))

# Descriptive statistics for numerical columns
print(data.describe())
```
