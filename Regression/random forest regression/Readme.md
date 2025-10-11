# 🌾 Crop Yield Prediction using Random Forest Regression

## 📘 Project Overview
This project focuses on predicting **crop yield (tons per hectare)** based on various **agricultural, soil, irrigation, fertilizer, and weather features**.  
Using a **Random Forest Regressor**, we build a model to capture the relationships between these factors and crop productivity.

### 🔍 Key Highlights
- Data preprocessing and categorical encoding  
- Statistical and visual analysis of relationships  
- Feature correlation and outlier detection  
- Predictive modeling using **Random Forest Regression**

---

## 🧩 About the Dataset

### 📂 Dataset Name
**Crop Yield Dataset** — commonly used for agricultural data analysis and yield prediction.

### 🧠 Objective
To predict the **Yield (tons/ha)** using features like soil type, crop type, fertilizer, irrigation, rainfall, and temperature.

### 📊 Attribute Description

| Column Name | Description |
|-------------|-------------|
| **Region** | Geographical region of the farm |
| **Soil_Type** | Type of soil in the field |
| **Crop** | Type of crop planted |
| **Weather_Condition** | Weather conditions during crop growth |
| **Fertilizer_Used** | Type of fertilizer applied |
| **Irrigation_Used** | Type/amount of irrigation applied |
| **Rainfall_mm** | Rainfall received (mm) |
| **Temperature_Celsius** | Average temperature (°C) during growth |
| **Days_to_Harvest** | Number of days taken for crop to mature |
| **Yield_tons_per_hectare** | Crop yield (tons per hectare) — **target variable** |

---

## 🧹 Data Cleaning and Preparation

- **Missing Values:**  
  Checked for missing values and handled them accordingly.  

- **Encoding Categorical Data:**  
  Columns (`Region`, `Soil_Type`, `Crop`, `Weather_Condition`) were encoded using `LabelEncoder` to convert text labels into numeric form.  

- **Feature Selection:**  
  Excluded the target `Yield_tons_per_hectare` when training the model.  

- **Train-Test Split:**  
  Divided the dataset into **70% training** and **30% testing** sets for model evaluation.

---

## 📈 Data Analysis Summary

- **Target Distribution:** Examined the distribution of crop yield with histogram and KDE plot.  
- **Correlation Heatmap:** Analyzed relationships among numeric features (`Rainfall_mm`, `Temperature_Celsius`, `Days_to_Harvest`, `Yield_tons_per_hectare`).  
- **Categorical Feature Analysis:** Countplots and boxplots to explore the impact of categorical variables.  
- **Pairplots:** Visualized pairwise relationships between numeric features.  
- **Outlier Detection:** Boxplots to identify extreme values in numeric data.

---

## 🔬 Model Summary

A **Random Forest Regression** model was trained to predict **Yield (tons/ha)** based on farm, soil, weather, and crop features.

### ⚙️ Model Steps
1. Prepared the feature set (`X`) and target (`y`).  
2. Split the data into training and testing sets.  
3. Initialized a **Random Forest Regressor** with `n_estimators=10` and `random_state=42`.  
4. Trained the model on the training dataset.  
5. Predicted crop yields on the test set.  
6. Compared **actual vs predicted yields** visually and in a table.

The model successfully captured complex patterns between crop features and yield.

---

## 📊 Visualizations

The following visualizations were generated during the analysis:

- 🌾 **Yield Distribution Plot** – Observed distribution of crop yields  
- 🔥 **Correlation Heatmap** – Visualized relationships among numeric features  
- 📊 **Countplots for Categorical Features** – Distribution of categorical variables  
- ⚡ **Boxplots by Category** – Examined impact of categorical features on yield  
- 🎯 **Actual vs Predicted Plot** – Evaluated model performance visually  
- 🧩 **Pairplots** – Explored pairwise relationships between numeric features  
- 📦 **Outlier Boxplots** – Identified extreme values in numeric data

---

## 🧮 Model Evaluation

The model’s performance was evaluated by comparing **actual vs predicted crop yields** using a scatter plot.  
A red diagonal line indicates perfect prediction — points close to the line indicate high accuracy.

### Quantitative Metrics
You can evaluate model performance with:

```python
from sklearn.metrics import r2_score, mean_absolute_error, mean_squared_error

print("R² Score:", r2_score(y_test, y_pred))
print("Mean Absolute Error (MAE):", mean_absolute_error(y_test, y_pred))
print("Mean Squared Error (MSE):", mean_squared_error(y_test, y_pred))
