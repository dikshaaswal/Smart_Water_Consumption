# 💧 Smart Water Consumption Analysis & Prediction

This project tackles the growing issue of urban water wastage by using machine learning to analyze and predict household water consumption. It leverages advanced data exploration, feature engineering, and model tuning techniques to help design intelligent water monitoring systems.
## 📁 Dataset Overview

The dataset contains household-level water usage and metadata:

| Column Name               | Description                                      |
|---------------------------|--------------------------------------------------|
| Timestamp                 | Date and time of the observation                 |
| Residents                 | Number of people in the household                |
| Apartment_Type            | Type of apartment (e.g., 1BHK, Detached)         |
| Temperature               | Ambient temperature (°C)                         |
| Humidity                  | Relative humidity (%)                            |
| Water_Price               | Price of water at the time                       |
| Period_Consumption_Index  | Relative usage intensity in 8-hour periods       |
| Income_Level              | Economic classification of the household         |
| Guests                   | Number of guests during the period               |
| Amenities                 | Available amenities (e.g., Pool, Garden)         |
| Appliance_Usage           | Whether water-consuming appliances were used     |
| Water_Consumption         | 💡 **Target variable** — actual water usage       |


## 🔍 Exploratory Data Analysis

Key visual insights include:
- Correlation heatmaps of `Water_Consumption` with other features
- Impact of `Apartment_Type`, `Income_Level`, and `Amenities` on usage
- Scatter plots and PDPs to explore relationships like:
  - `Residents` vs. `Water_Consumption`
  - `Temperature` vs. `Humidity`
  - Appliance usage behavior
 
Models used:
- ✅ **RandomForestRegressor**
- ✅ **XGBoostRegressor**
- ✅ **LightGBM**
- Feature selection based on correlation and PDP insights
- Hyperparameter tuning via `RandomizedSearchCV`
- Evaluation metric:  
  Score = max(0, 100 - RMSE)
