# London City Bike Demand Forecasting 🚲

## 📌 Project Overview

This repository contains the code and data for my postgraduate thesis: **"Forecasting demand for London city bikes using regression models"**, completed as part of the *Data Science in Business* postgraduate studies at the **Warsaw School of Economics (SGH)**.

The main objective of this project is to predict the daily demand for city bikes at specific stations in London. Accurate forecasting can help system operators optimize bike redistribution, reduce maintenance costs, and ensure higher user satisfaction by preventing empty or completely full stations.

## 📊 Data Sources

The final dataset spans the years **2016 - 2018** and was created by joining three distinct data sources using SQL in Google BigQuery:

1. **London Bicycles Data**: Public dataset available in [Google BigQuery](https://console.cloud.google.com/bigquery?ws=!1m4!1m3!3m2!1sbigquery-public-data!2slondon_bicycles) containing historical bike trips.

2. **London Cycling Safety**: Dataset from [Kaggle](https://www.kaggle.com/datasets/dtuthill/london-cycling-safety) detailing bicycle accidents (fatal, serious, slight).

3. **London Weather Data**: Historical weather data downloaded from [Visual Crossing](https://www.visualcrossing.com/weather-query-builder/#) (temperature, humidity, wind speed, weather type).

## 🛠️ Technologies & Libraries

* **Language:** Python

* **Data Manipulation:** `pandas`, `numpy`

* **Data Visualization:** `matplotlib`, `seaborn`

* **Machine Learning:** `scikit-learn` (Random Forest), `xgboost` (XGBoost)

## ⚙️ Methodology

1. **Data Preprocessing & Feature Engineering:**

   * Extraction of time-based features (year, month, day of week, season, weekend indicator).

   * Integration of public holiday flags.

   * **Lagging:** Introduction of lagged variables (e.g., trip counts from the previous 1-7 days) to capture time-series dependencies.

2. **Exploratory Data Analysis (EDA):**

   * Analysis of demand patterns across different seasons, days of the week, and weather conditions.

   * Correlation analysis between meteorological factors and bike rentals.

3. **Modeling:**

   * Baseline and advanced regression modeling.

   * Evaluated algorithms: **Random Forest Regressor** and **XGBoost Regressor**.

4. **Evaluation Metrics:**

   * Mean Absolute Error (MAE)

   * Root Mean Squared Error (RMSE)

   * R-squared (R²)

## 📈 Key Findings

* **Temporal Patterns:** Demand is highly seasonal, peaking during summer months and dropping significantly in winter. Weekdays show different usage patterns compared to weekends, indicating strong commuter usage.

* **Weather Impact:** Temperature has a strong positive correlation with bike rentals, while high humidity and severe weather negatively impact demand.

* **Model Performance:** Both Random Forest and XGBoost performed well, with the inclusion of lagged features significantly improving predictive accuracy for individual stations.

## 📁 Repository Structure

To keep the project organized, the repository follows this structure:

    ├── data/
    │   └── london_bikes.csv       # Processed dataset ready for modeling
    ├── notebooks/
    │   └── lonbikes_20250605.ipynb # Main Jupyter Notebook with EDA, Feature Engineering, and Modeling
    ├── docs/
    │   └── thesis_PL.pdf    # PDF version of the original thesis in Polish
    ├── README.md                  # Project overview


## 🚀 How to Run the Project

1. Clone the repository:

    git clone https://github.com/your-username/london-bike-demand.git
   

2. Navigate to the project directory:

    cd london-bike-demand
   

3. Install the required dependencies:

    pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter
   

4. Launch Jupyter Notebook and open the main analysis file:

    jupyter notebook notebooks/lonbikes_20250605.ipynb
   

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ✍️ Author

**Małgorzata Ciępka**

* Data Science in Business, Warsaw School of Economics (SGH)

* [LinkedIn Profile]([https://www.linkedin.com/in/your-profile](https://www.linkedin.com/in/malgocie/))
