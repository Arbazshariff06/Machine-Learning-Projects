# 🐟 Fish Weight Prediction using Support Vector Regression (SVR)

## 📘 Project Overview
This project focuses on predicting the **weight of a fish** based on its **physical characteristics** such as length, height, and width.  
Using **Support Vector Regression (SVR)** with the **RBF kernel**, we build a robust predictive model that captures non-linear relationships between body measurements and fish weight.

### 🔍 Key Highlights
- Data preprocessing and encoding  
- Statistical and visual analysis of relationships  
- Outlier detection and correlation studies  
- Predictive modeling using **SVR**

---

## 🧩 About the Dataset

### 📂 Dataset Name
**Fish Market Dataset** — available on **Kaggle** and widely used for regression analysis.

### 🧠 Objective
To predict the **Weight** (in grams) of a fish using its **species** and **body dimensions**.

### 📊 Attribute Description

| Column Name | Description |
|--------------|-------------|
| **Species** | Type of fish (e.g., Bream, Roach, Pike, etc.) |
| **Weight** | Weight of the fish in grams (**target variable**) |
| **Length1** | Vertical length of the fish (in cm) |
| **Length2** | Diagonal length of the fish (in cm) |
| **Length3** | Cross length of the fish (in cm) |
| **Height** | Height of the fish (in cm) |
| **Width** | Diagonal width of the fish (in cm) |

---

## 🧹 Data Cleaning and Preparation

- **Missing Values:**  
  Checked for missing values — none were found in the dataset.  

- **Encoding Categorical Data:**  
  The `Species` column was encoded using `LabelEncoder` from `sklearn.preprocessing` to convert text labels into numerical form.  

- **Feature Scaling:**  
  All numerical features and the target variable were standardized using `StandardScaler` to ensure equal importance during model training.  

- **Train-Test Split:**  
  Data was divided into **70% training** and **30% testing** sets to evaluate model generalization.

---

## 📈 Data Analysis Summary

- **Length1**, **Length2**, and **Length3** show a **strong positive correlation** with **Weight**.  
- **Distribution plots** reveal that most fish weights lie in the lower range.  
- **Count plots** show uneven species distribution (some species appear more frequently).  
- **Scatter plots and pairplots** confirm that as fish length and width increase, so does the weight.  
- **Boxplots** help identify potential outliers that may influence regression results.

---

## 🔬 Model Summary

A **Support Vector Regression (SVR)** model was trained using the **RBF (Radial Basis Function)** kernel.

### ⚙️ Model Steps
1. Applied `StandardScaler` to normalize features and target values.  
2. Trained the **SVR** model using the training dataset.  
3. Predicted fish weights on the test set.  
4. Inverse-transformed predictions back to original scale.  
5. Compared **actual vs predicted** results visually and numerically.

The SVR model successfully captured **non-linear relationships** between the features and fish weight.

---

## 📊 Visualizations

The following visualizations were created during analysis:

- 🔥 **Correlation Heatmap** – Feature relationships visualization  
- 📈 **Weight Distribution Plot** – Understanding data spread and skewness  
- 🐠 **Species Count Plot** – Frequency of each fish species  
- ⚖️ **Scatter Plots** – Relationship between Weight and Lengths/Width/Height  
- 🎯 **Actual vs Predicted Plot** – Visualizing model accuracy  
- 📦 **Boxplots** – Outlier detection  

---

## 🧮 Model Evaluation

The model’s performance was evaluated by comparing **actual vs predicted weights** using a scatter plot.  
A red diagonal line indicates perfect prediction — the closer the blue points are to this line, the better the model.

### Optional: Add Quantitative Metrics
You can compute regression performance metrics using:

```python
from sklearn.metrics import r2_score, mean_absolute_error, mean_squared_error

print("R² Score:", r2_score(y_test, y_pred))
print("MAE:", mean_absolute_error(y_test, y_pred))
print("MSE:", mean_squared_error(y_test, y_pred))
