# 🚗 Auto MPG Analysis and Polynomial Regression Project

## 📘 Project Overview
This project aims to analyze the **Auto MPG dataset** and develop a **Polynomial Regression model** to predict a car’s fuel efficiency, measured in **miles per gallon (MPG)**.  
Through data exploration and visualization, we study how different car characteristics — such as engine size, horsepower, and weight — affect fuel consumption.

The project highlights:
- Data cleaning and preprocessing
- Statistical analysis and visualization
- Relationship study among features
- Predictive modeling using Polynomial Regression

---

## 🧩 About the Dataset

### 📂 Dataset Name
**Auto MPG Dataset** — originally from the **U.S. Census Bureau and UC Irvine Machine Learning Repository (UCI)**.

### 🧠 Objective
To predict the **fuel efficiency (MPG)** of automobiles based on engine and design characteristics.

### 📊 Attributes Description

| Column Name | Description |
|--------------|-------------|
| **mpg** | Miles per gallon (target variable) – measures fuel efficiency. |
| **cylinders** | Number of cylinders in the engine. |
| **displacement** | Engine displacement in cubic inches. Represents engine size. |
| **horsepower** | Power output of the car’s engine. |
| **weight** | Vehicle weight in pounds. |
| **acceleration** | Time required to accelerate from 0 to 60 mph (in seconds). |
| **model year** | Year when the car model was manufactured. |
| **origin** | Country of origin (1 = USA, 2 = Europe, 3 = Asia). |
| **car name** | String with manufacturer and model name of the car. |

---

## 🧹 Data Cleaning and Preparation

- **Missing Values:**  
  Some entries in the `horsepower` column were missing or non-numeric. These were converted to numeric and filled with the mean value.
  
- **Irrelevant Features:**  
  The `car name` and `origin` columns were removed since they do not contribute to numerical prediction.

- **Feature Selection:**  
  Focused on numerical attributes directly affecting vehicle performance and fuel efficiency.

---

## 📈 Data Analysis Summary

- Cars with **fewer cylinders** generally show **higher MPG**.
- **Weight** and **horsepower** have a strong negative correlation with **MPG** — heavier and more powerful cars consume more fuel.
- Over the years, **average MPG increased**, showing improvement in car design and fuel economy.
- The **heatmap** and **pairplots** visualize strong interdependencies among `displacement`, `weight`, and `horsepower`.

---

## 🔬 Model Summary

A **Polynomial Regression model** (degree 4) was trained to capture non-linear relationships between car features and fuel efficiency.  
The model predicts MPG based on combinations of attributes such as horsepower, weight, and displacement.  

Results show a close match between actual and predicted MPG values, confirming that polynomial regression effectively models these complex relationships.

---

## 🏁 Insights & Conclusion

- Cars with smaller engines and lighter weight achieve better fuel efficiency.  
- Over time, manufacturers have improved engine efficiency, leading to higher MPG in later model years.  
- Polynomial regression provides a strong predictive performance for estimating MPG using numerical car features.  

This analysis demonstrates how **data-driven techniques** can uncover trends and insights in the automotive industry, helping design more efficient vehicles.

---

## 📚 References
- UCI Machine Learning Repository – [Auto MPG Dataset](https://archive.ics.uci.edu/ml/datasets/auto+mpg)
- U.S. Census Bureau – Car Performance and Efficiency Data

---
