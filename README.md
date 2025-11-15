#  Air Quality Analysis

This project focuses on analyzing air quality data to uncover patterns, relationships, and anomalies in various air pollutant levels. It includes thorough data cleaning, exploratory data analysis (EDA), and visualizations to better understand the environmental conditions affecting air quality.

---

##  Project Structure

- `air_quality_analysis.ipynb`: Jupyter Notebook containing all data analysis, cleaning, visualizations, and insights.
- `air_quality_dataset.csv`: The dataset used for this project (not included if too large).
- `README.md`: Project documentation.

---

##  Dataset Overview

The dataset contains air quality measurements such as:
- PM2.5
- PM10
- NO2
- SO2
- CO
- O3
- AQI (Air Quality Index)

Each record includes a timestamp and location for contextual analysis.

---

##  What We Did

-  **Data Cleaning**  
  - Removed missing/null values  
  - Handled duplicate entries  
  - Formatted dates and standardized column names

-  **Exploratory Data Analysis (EDA)**  
  - Summary statistics and distribution of key pollutants  
  - Correlation matrix to detect relationships  
  - Outlier detection using statistical and visual methods

-  **Visualizations**  
  - Line plots of pollutant trends over time  
  - Histograms and boxplots to analyze distributions  
  - Heatmaps to show correlations  
  - Scatter plots for feature comparisons

---

##  Insights

- Identified strong correlations between certain pollutants (e.g., PM2.5 and AQI)
- Spotted seasonal spikes in pollution levels
- Outliers often linked with specific events or locations

---

##  Requirements

To run the notebook, install the following:

```bash
pip install pandas numpy matplotlib seaborn
