# Uber-Lyft-Ride-Sharing
# 🚖 Ride Price Prediction Using Weather and Temporal Data

This project utilizes ride-hailing and weather data to develop a predictive model that estimates the price of a ride based on various factors, including distance, time of day, weather conditions, and ride type.

## 📌 Project Objectives

- Predict ride prices using real-world weather and ride data
- Analyze key features influencing price (distance, surge, ride type)
- Evaluate model performance and explain predictions using SHAP
- Create a deployable and interactive tool via Streamlit

## 📊 Dataset Overview

The dataset includes ~690,000 rides with features such as:

- **Ride Info**: `cab_type`, `name`, `distance`, `surge_multiplier`
- **Location**: `source`, `destination`
- **Time**: `hour`, `day`, `month`, `day_of_week`, `is_peak_hour`
- **Weather**: `temperature`, `humidity`, `windSpeed`, `visibility`, `short_summary`, etc.
- **Target**: `price`

## 🔍 Exploratory Data Analysis (EDA)

Key insights:
- Surge multiplier and ride type (`name`) are highly correlated with price
- Distance remains the strongest price driver
- Weather and time-of-day features add marginal but consistent value

## 🤖 Model Development

### ✅ Models Used:
- **Random Forest Regressor** (Baseline)
- **XGBoost Regressor** (Tuned with GridSearchCV)

### 🔧 Best Model Performance:
| Metric     | Value   |
|------------|---------|
| MAE        | 1.06    |
| RMSE       | 1.62    |
| R² Score   | 0.970   |

### ✅ Feature Importance (via SHAP):

- `distance`
- `surge_multiplier`
- `name` (ride type)
- `cab_type`
- `temperature`, `humidity`, and `cloudCover`

## 📈 SHAP Explainability

SHAP plots were used to interpret both global and individual ride predictions.

## 💻 Streamlit App (Coming Soon)

An interactive web app will allow users to:
- Input ride details (type, time, weather, distance)
- Get instant price predictions
- Visualize feature impact

## 🧰 Tech Stack

- Python (pandas, numpy, seaborn, matplotlib)
- scikit-learn, XGBoost, SHAP
- Streamlit (for app deployment)
- Jupyter Notebook

