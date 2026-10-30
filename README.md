# Air Quality Monitoring & Trend Analysis 🌍

## About the Project

Air pollution is a major problem in many cities. I developed this project to understand air pollution levels in different Indian cities and study how they change over time.

In this project, I used Python to analyze air-quality data, find pollution patterns, compare different cities, and study the relationship between pollutants.

I also built Machine Learning models to estimate PM2.5 values when the actual measurements are missing.

## Project Objectives

- Analyze air quality in different Indian cities.
- Find which cities have higher pollution levels.
- Study seasonal changes in pollution.
- Understand the relationship between different pollutants.
- Clean the dataset and handle missing values.
- Build Machine Learning models to estimate PM2.5.

## Dataset

I used the **Air Quality Data in India** dataset from Kaggle.

**Dataset Link:** [Air Quality Data in India](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)

- Time period: 2015–2020
- Number of cities: 26
- Total records: 29,531
- Data type: Daily air-quality measurements

### Important Columns

| Column | Description |
|---|---|
| City | Name of the city |
| Date | Date of observation |
| PM2.5 | Fine particles in the air |
| PM10 | Larger particles in the air |
| NO | Nitric Oxide |
| NO2 | Nitrogen Dioxide |
| NOx | Nitrogen Oxides |
| NH3 | Ammonia |
| CO | Carbon Monoxide |
| SO2 | Sulphur Dioxide |
| O3 | Ozone |
| AQI | Air Quality Index |

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Steps

### 1. Data Cleaning

- Loaded the dataset using Pandas.
- Checked missing values and duplicate records.
- Corrected the date format.
- Sorted the data based on dates.
- Extracted month and year.
- Created seasons for seasonal analysis.
- Used median imputation for missing numerical input values during model training.

### 2. Exploratory Data Analysis (EDA)

I performed data analysis and created graphs to understand pollution patterns.

Some of the analysis includes:

- PM2.5 distribution.
- City-wise pollution comparison.
- Seasonal pollution analysis.
- Correlation between different pollutants.

### 3. Machine Learning

I used two regression algorithms to estimate PM2.5 values.

**Linear Regression:** Used as a basic model for comparison.

**Random Forest Regressor:** Used to understand more complex relationships between different pollutants and estimate PM2.5.

**Input Features:**
- City
- Month
- PM10
- NO
- NO2
- NOx
- NH3
- CO
- SO2
- O3

**Target:** PM2.5

I used a chronological train-test split to train the models on earlier records and test them on later records.

### 4. Model Evaluation

I compared both models using three evaluation metrics:

- **MAE:** Measures the average prediction error.
- **RMSE:** Measures prediction error and gives more importance to larger errors.
- **R² Score:** Shows how well the model explains the changes in PM2.5 values.

### Model Results

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 22.28 | 35.61 | 0.234 |
| Random Forest | 13.92 | 24.74 | 0.630 |

**Result:** Random Forest performed better than Linear Regression, with an R² score of 0.630.

## Practical Use

The model can estimate PM2.5 values when the actual PM2.5 measurement is missing but other pollutant measurements are available.

For example, if a monitoring station has PM10, NO2, and CO readings but no PM2.5 reading for that day, the model can estimate the missing PM2.5 value.

## Limitations

- Prediction accuracy depends on the quality of the input data.
- Unusual weather conditions, such as cyclones and dust storms, may affect model performance.
- The current model estimates same-day PM2.5 values. It does not predict tomorrow's pollution levels.
- Model estimates cannot replace actual sensor measurements.

## Project Structure

```text
airqualityanalysis/
│
├── AirQualityAnalysis.ipynb
├── AirQualityAnalysis.pdf
├── README.md
│
└── data/
    └── city_day.csv
```

## How to Run the Project

**1. Clone the repository**

```bash
git clone https://github.com/siddharda1/airqualityanalysis.git
```

**2. Open the project folder**

```bash
cd airqualityanalysis
```

**3. Install the required libraries**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

**4. Download the dataset**

Download `city_day.csv` from the Kaggle dataset link and place it inside the `data` folder.

**5. Open Jupyter Notebook**

```bash
jupyter notebook
```

Open `AirQualityAnalysis.ipynb` and run the cells one by one.

## Future Improvements

- Include weather information such as temperature, rainfall, and wind speed.
- Try time-series models to predict future pollution levels.
- Test more Machine Learning algorithms.
- Improve model accuracy with more recent data.

## Author

**Siddharda**

B.Tech – Computer Science and Engineering


*This project helped me improve my skills in Python, data cleaning, data visualization, Exploratory Data Analysis, and Machine Learning.*
