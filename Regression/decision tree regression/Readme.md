# 🌤 Weather Temperature Prediction using Decision Tree Regression

## 📘 Project Overview
This project focuses on predicting the **temperature** based on various **weather attributes** such as humidity, wind speed, visibility, and atmospheric pressure.  
Using a **Decision Tree Regressor**, we build a model to capture the relationships between weather features and temperature variations over time.

### 🔍 Key Highlights
- Data preprocessing and encoding  
- Statistical and visual analysis of relationships  
- Feature correlation studies  
- Predictive modeling using **Decision Tree Regression**

---

## 🧩 About the Dataset

### 📂 Dataset Name
**Weather History Dataset** — commonly available on Kaggle for regression and time-series analysis.

### 🧠 Objective
To predict the **Temperature (°C)** using other weather-related features like humidity, wind, pressure, and visibility.

### 📊 Attribute Description

| Column Name | Description |
|-------------|-------------|
| **Formatted Date** | Timestamp of the weather record |
| **Summary** | Short description of weather conditions |
| **Precip Type** | Type of precipitation (rain/snow) |
| **Temperature (C)** | Actual temperature in Celsius (**target variable**) |
| **Apparent Temperature (C)** | “Feels like” temperature in Celsius |
| **Humidity** | Relative humidity (0-1 scale) |
| **Wind Speed (km/h)** | Wind speed in kilometers per hour |
| **Wind Bearing (degrees)** | Wind direction in degrees |
| **Visibility (km)** | Visibility distance in kilometers |
| **Loud Cover** | Cloud coverage metric |
| **Pressure (millibars)** | Atmospheric pressure in millibars |
| **Daily Summary** | Detailed weather description |

---

## 🧹 Data Cleaning and Preparation

- **Missing Values:**  
  Checked for missing values and forward-filled the `Precip Type` column.  

- **Encoding Categorical Data:**  
  Categorical columns (`Summary`, `Precip Type`, `Daily Summary`, `Formatted Date`) were encoded using `LabelEncoder` to convert text labels into numeric form.  

- **Date Conversion:**  
  Converted the `Formatted Date` column into `datetime` format for time-series visualizations.  

- **Feature Selection:**  
  Excluded the target `Temperature (C)` and date column when training the model.  

- **Train-Test Split:**  
  Divided the dataset into **70% training** and **30% testing** sets for model evaluation.

---

## 📈 Data Analysis Summary

- **Correlation Heatmap:** Identified relationships between numeric features and temperature.  
- **Histograms:** Visualized the distribution of numeric features like humidity, wind speed, and pressure.  
- **Scatter Plots & Pairplots:** Explored how features such as wind bearing and apparent temperature relate to the actual temperature.  
- **Time-Series Plots:** Tracked temperature and apparent temperature over time to observe trends.

---

## 🔬 Model Summary

A **Decision Tree Regression** model was trained to predict **Temperature (°C)** based on weather features.

### ⚙️ Model Steps
1. Prepared the feature set (`X`) and target (`y`).  
2. Split the data into training and testing sets.  
3. Initialized a **Decision Tree Regressor** with `max_depth=10`.  
4. Trained the model on the training dataset.  
5. Predicted temperatures on the test set.  
6. Compared **actual vs predicted temperatures** visually using scatter plots.

The model successfully captured complex patterns between weather features and temperature.

---

## 📊 Visualizations

The following visualizations were generated during the analysis:

- 🌡 **Temperature vs Time Plot** – Observed temperature trends over time  
- 🔥 **Correlation Heatmap** – Visualized relationships between numeric features  
- 📊 **Histograms** – Distribution of numeric features  
- ⚡ **Scatter Plots** – Examined temperature relationship with wind direction and other variables  
- 🎯 **Actual vs Predicted Plot** – Evaluated model performance visually  
- 🧩 **Pairplots** – Explored pairwise relationships between numeric features

---

## 🧮 Model Evaluation

The model’s performance was evaluated by comparing **actual vs predicted temperatures** using a scatter plot.  
A red diagonal line indicates perfect prediction — points close to the line indicate high accuracy.

### Quantitative Metrics
You can evaluate model performance with:

```python
from sklearn.metrics import r2_score, mean_absolute_error, mean_squared_error

print("R² Score:", r2_score(y_test, y_pred))
print("Mean Absolute Error (MAE):", mean_absolute_error(y_test, y_pred))
print("Mean Squared Error (MSE):", mean_squared_error(y_test, y_pred))
