#  Data Scaling in Machine Learning

Data scaling is an essential preprocessing step used to **normalize and standardize numerical features** so that machine learning models can learn efficiently.  
Many ML algorithms — **KNN, SVM, Linear Regression, Gradient Descent–based models** — perform better when features are on a **similar scale**.

We will cover:

- **StandardScaler**
- **MinMaxScaler**
- **RobustScaler**

---

# 1. StandardScaler

##  What it does
StandardScaler transforms features such that:

- Mean becomes **0**
- Standard deviation becomes **1**

This is called **Z-score normalization**.

**Formula:**  
`X_scaled = (X - mean) / std`

---

##  When to use
- When data follows a **normal distribution**
- Works well for:
  - Logistic Regression
  - Linear Regression
  - SVM
  - KMeans

---

##  Pros
✔ Widely used  
✔ Works well with gradient-based algorithms  

## Cons
✖ Sensitive to outliers  

---

#  2. MinMaxScaler

##  What it does
Scales values to a fixed range, usually **0 to 1**.

**Formula:**  
`X_scaled = (X - Xmin) / (Xmax - Xmin)`

---

##  When to use
- When you need **bounded values (0–1)**
- Useful for:
  - Neural networks  
  - Distance-based models (KNN)

---

##  Pros
✔ Preserves original distribution shape  
✔ Maintains feature relationships  

##  Cons
✖ Very sensitive to outliers  

---

#  3. RobustScaler

##  What it does
Uses **median** and **IQR** (Interquartile Range) instead of mean and std.

**Formula:**  
`X_scaled = (X - Median) / IQR`

---

##  When to use
- When data contains **many outliers**
- Works well for skewed or real-world data

---

##  Pros
✔ Not affected by outliers  
✔ Good for skewed data  

##  Cons
✖ Does not scale data to a specific range  

---

#  Summary Table

| Scaler | What It Does | Best For | Outliers |
|--------|--------------|----------|-----------|
| **StandardScaler** | Normalize using mean & std | Normal distributions | ❌ Sensitive |
| **MinMaxScaler** | Scale to 0–1 | Neural nets, KNN | ❌ Very Sensitive |
| **RobustScaler** | Median & IQR | Outlier-heavy data | ✅ Resistant |

---
