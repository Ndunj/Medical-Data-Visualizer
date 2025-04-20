# Medical Data Visualizer  

![Example Visualizations](catplot.png) ![Example Visualizations](heatmap.png)  

A Python tool for analyzing and visualizing medical examination data using Pandas, Seaborn, and Matplotlib.  

## Features  

- **BMI Classification**: Identifies overweight patients (BMI ≥ 25)  
- **Health Metric Normalization**: Standardizes cholesterol and glucose values  
- **Interactive Visualizations**:  
  - Categorical plot showing distributions of 6 health indicators  
  - Correlation heatmap of medical features  
- **Data Cleaning**: Automatically filters outliers (2.5th-97.5th percentiles)  

## Installation  

1. Clone the repository:  
   ```bash  
   git clone https://github.com/your-username/medical-data-visualizer.git

Install dependencies:
   pip install pandas seaborn matplotlib numpy  

   Usage
from medical_visualizer import draw_cat_plot, draw_heat_map  

# Generate and save visualizations  
draw_cat_plot()  # Saves as 'catplot.png'  
draw_heat_map()  # Saves as 'heatmap.png'  

Data Processing
Overweight Calculation
df['overweight'] = (df['weight']/((df['height']/100)**2)).apply(lambda x: 0 if x < 25 else 1)  

Metric Normalization
df['cholesterol'] = df['cholesterol'].apply(lambda x: 0 if x == 1 else 1)  
df['gluc'] = df['gluc'].apply(lambda x: 0 if x == 1 else 1)  

Visualization Examples
Categorical Plot (catplot.png)
Compares prevalence of 6 health factors between cardiovascular patients vs healthy individuals
Features: Cholesterol, Glucose, Smoking, Alcohol Intake, Activity, Overweight status
Correlation Heatmap (heatmap.png)
Shows relationships between medical indicators
Uses triangular mask to avoid redundancy
Data Requirements
CSV file with columns:

height (cm)
weight (kg)
cholesterol (1: normal, 2-3: elevated)
gluc (1: normal, 2-3: elevated)
cardio (0: no CVD, 1: has CVD)
Additional lifestyle columns: smoke, alco, active

License
MIT


### Recommended Repository Structure  

medical-data-visualizer/
├── medical_visualizer.py # Your main code
├── README.md
├── catplot.png # Sample output
├── heatmap.png # Sample output
└── requirements.txt # With: pandas, seaborn, matplotlib, numpy

   
