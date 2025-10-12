# 🧪 Logistic Regression Training Project: Cancer Prediction

## 📌 Project Overview
This project demonstrates how to build a **Logistic Regression model** to predict whether a tumor is **benign** or **malignant** using the **Breast Cancer Wisconsin dataset**.  

The model uses various cell nucleus features to classify tumors and evaluate its performance through accuracy and other classification metrics.

---

## 🧰 Technologies & Libraries Used
- **Python 3.x**
- **Pandas** – Data manipulation and analysis  
- **Matplotlib & Seaborn** – Data visualization  
- **Scikit-learn (sklearn)** – Machine learning (Logistic Regression, preprocessing, evaluation)

---

## 📂 Dataset Information
- **Dataset:** `data.csv` (Breast Cancer Wisconsin Dataset)  
- **Key Feature:** `diagnosis` (target variable)  
  - `M` = Malignant  
  - `B` = Benign  
- **Unnecessary columns removed:** `id`, `Unnamed: 32`

### 📊 Features
The dataset includes multiple numerical features related to:
- Radius
- Texture
- Perimeter
- Area
- Smoothness
- Compactness
- Concavity
- Symmetry
- Fractal Dimension

---

## 🧼 Data Preprocessing
1. **Load the dataset** using Pandas.
2. **Explore data** using `.info()`, `.describe()`, and `head()`.
3. **Visualize missing values** using `sns.heatmap()`.
4. **Drop unnecessary columns** (`id` and `Unnamed: 32`).
5. **Encode labels**: Malignant → 1, Benign → 0.
6. **Convert labels** to categorical type.
7. **Normalize** the features using `StandardScaler` to standardize the data.

---

## 🧠 Model Building
1. **Split the dataset**: 70% training, 30% testing.
2. **Initialize** `LogisticRegression` model.
3. **Train** the model on training data.
4. **Predict** outcomes on the test set.

```python
from sklearn.linear_model import LogisticRegression
classification = LogisticRegression()
classification.fit(X_train, y_train)
y_pred = classification.predict(X_test)
