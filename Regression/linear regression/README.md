# 🛒 Ecommerce Customer Spending Prediction using Linear Regression

## 📘 Project Overview
This project aims to predict the **Yearly Amount Spent by customers** on an ecommerce platform using features like **session length**, **time spent on the app**, **time on the website**, and **length of membership**.  
A **Multiple Linear Regression model** is used to analyze how these factors influence customer spending behavior.

### 🔍 Key Highlights
- Data exploration and visualization  
- Relationship analysis between key customer metrics  
- Model training and evaluation using **Linear Regression**  
- Performance metrics and residual analysis  

---

## 🧩 About the Dataset

### 📂 Dataset Name
**Ecommerce Customers Dataset** — a dataset containing ecommerce customer behavior and spending data.

### 🧠 Objective
To predict how much a customer will spend annually based on their website and app activity and membership length.

### 📊 Attribute Description

| Column Name | Description |
|--------------|-------------|
| **Email** | Customer’s email address |
| **Address** | Customer’s address |
| **Avatar** | Customer’s profile image |
| **Avg. Session Length** | Average length of user sessions on the site (in minutes) |
| **Time on App** | Average time spent on the mobile app (minutes) |
| **Time on Website** | Average time spent on the website (minutes) |
| **Length of Membership** | Years since the customer became a member |
| **Yearly Amount Spent** | Total annual spending by the customer (**target variable**) |

---

## 🧹 Data Cleaning and Preparation

- Verified dataset information and summary statistics (`dataset.info()`, `dataset.describe()`).  
- No missing values were detected.  
- Selected relevant numerical columns for modeling:
- Split dataset into **70% training** and **30% testing** using `train_test_split`.

---

## 📈 Exploratory Data Analysis (EDA)

### Key Visualizations
- **Joint Plots:**  
- `Time on Website` vs. `Yearly Amount Spent`  
- `Time on App` vs. `Yearly Amount Spent`
- **Pair Plot:**  
Explored pairwise relationships between all numeric features.
- **Regression Plot (lmplot):**  
Showed the strong linear relationship between `Length of Membership` and `Yearly Amount Spent`.

---

## 🔬 Model Summary

A **Multiple Linear Regression** model was trained using **Scikit-learn**.

### ⚙️ Model Steps
1. Split dataset into training and testing sets.  
2. Initialized and trained a `LinearRegression()` model.  
3. Extracted model coefficients and interpreted feature importance.  
4. Evaluated the model using R², MAE, MSE, and RMSE.  
5. Visualized predicted vs. actual values.

### 📉 Model Coefficients
The learned coefficients help explain how much each feature contributes to yearly spending:
