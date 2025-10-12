# 🌸 Iris Species Classification using K-Nearest Neighbors (KNN)

## 📘 Project Overview
This project focuses on **classifying the Iris species** based on **physical measurements** such as Sepal Length, Sepal Width, Petal Length, and Petal Width.  
Using the **K-Nearest Neighbors (KNN)** algorithm, we build a predictive model to accurately classify each sample into one of the three Iris species: **Setosa, Versicolor, or Virginica**.

### 🔍 Key Highlights
- Data preprocessing and encoding  
- Statistical and visual analysis of features  
- Outlier detection and correlation studies  
- Predictive modeling using **KNN**  
- Decision boundary visualization for 2D feature spaces  
- Comparison of actual vs predicted species

---

## 🧩 About the Dataset

### 📂 Dataset Name
**Iris Dataset** — a classic dataset widely used for classification problems, available in **UCI Machine Learning Repository**.

### 🧠 Objective
To predict the **species of an Iris flower** using its physical measurements.

### 📊 Attribute Description

| Column Name       | Description |
|------------------|-------------|
| **SepalLengthCm** | Sepal length in cm |
| **SepalWidthCm**  | Sepal width in cm |
| **PetalLengthCm** | Petal length in cm |
| **PetalWidthCm**  | Petal width in cm |
| **Species**       | Target variable (Setosa, Versicolor, Virginica) |

---

## 🧹 Data Cleaning and Preparation

- **Missing Values:**  
  Checked for missing values — none were found in the dataset.

- **Encoding Categorical Data:**  
  The `Species` column was encoded using `LabelEncoder` from `sklearn.preprocessing` to convert species names into numeric labels:  
  `Setosa = 0, Versicolor = 1, Virginica = 2`.

- **Feature Scaling:**  
  All features were standardized using `StandardScaler` to ensure equal importance during KNN training.

- **Train-Test Split:**  
  Data was divided into **70% training** and **30% testing** sets to evaluate model performance.

---

## 📈 Data Analysis Summary

- **Feature Distributions:** Histograms show the spread of sepal and petal dimensions.  
- **Boxplots:** Used to detect potential outliers in measurements.  
- **Pairplots:** Show relationships between features and help identify separability among species.  
- **Correlation Heatmap:** Sepal and petal features show strong positive correlation with petal length and width.  
- **Species Count Plot:** Shows the dataset is **balanced** across all three species.

---

## 🔬 Model Summary

A **K-Nearest Neighbors (KNN)** classifier was trained to predict Iris species.

### ⚙️ Model Steps
1. Standardized feature data using `StandardScaler`.  
2. Trained a **KNN classifier** (`n_neighbors=3`) on the training set.  
3. Predicted species on the test set.  
4. Compared **actual vs predicted** results using tables and plots.  
5. Visualized **decision boundaries** for two key features: Sepal Length vs Petal Length.

The model performed **very well**, achieving high accuracy in predicting the correct species.

---

## 📊 Visualizations

The following visualizations were created during analysis:

- 🌟 **Feature Distribution Histograms** – Understanding spread of sepal and petal dimensions  
- 📦 **Boxplots** – Detect outliers  
- 🔄 **Pairplots** – Feature relationships and species separability  
- 🔥 **Correlation Heatmap** – Feature correlation insights  
- 🌺 **Species Count Plot** – Distribution of classes  
- 🎯 **Decision Boundary Plots** – Visual representation of KNN predictions (2D features)  
- 📊 **Actual vs Predicted Count Plot** – Comparing model predictions with true labels

---

## 🧮 Model Evaluation

The model’s performance was evaluated using:

- **Confusion Matrix**
- **Accuracy Score**
- **Classification Report** (Precision, Recall, F1-score for each class)

Example Metrics:

```python
from sklearn.metrics import confusion_matrix, accuracy_score, classification_report

cm = confusion_matrix(y_test, y_pred)
print(cm)

accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)

print(classification_report(y_test, y_pred))
