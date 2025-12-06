# Data Scaling in Machine Learning

Data scaling is an essential preprocessing step used to **normalize and standardize numerical features** so that machine learning models can learn efficiently.  
Many ML algorithms — **KNN, SVM, Linear Regression, Gradient Descent–based models** — perform better when features are on a **similar scale**.

In this blog, we cover the three most commonly used scaling techniques:

- **StandardScaler**  
- **MinMaxScaler**  
- **RobustScaler**

---

# 🧮 1. StandardScaler

##  What it does
StandardScaler transforms features such that:

- Mean becomes **0**
- Standard deviation becomes **1**

This is called **Z-score normalization**.

\[
X_{\text{scaled}} = \frac{X - \mu}{\sigma}
\]

---

## 📌 When to use
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

##  Cons
✖ Sensitive to outliers (mean & std are affected)  

---

#  2. MinMaxScaler

##  What it does
Scales values into a fixed range, usually **0 to 1**.

\[
X_{\text{scaled}} = \frac{X - X_{\min}}{X_{\max} - X_{\min}}
\]

---

##  When to use
- When you need **bounded values (0–1)**
- Useful for:
  - Neural networks  
  - Distance-based models (KNN)  

---

##  Pros
✔ Preserves original distribution shape  
✔ Maintains all feature relationships  

##  Cons
✖ Very sensitive to outliers (depends on min & max)  

---

#  3. RobustScaler

##  What it does
Uses **median** and **IQR (Interquartile Range)** instead of mean and std.

\[
X_{\text{scaled}} = \frac{X - \text{Median}}{IQR}
\]

---

##  When to use
- When the dataset contains **many outliers**
- Works well for:
  - Finance data  
  - Retail/Sales datasets  
  - Sensor data  
  - Skewed distributions  

---

##  Pros
✔ Not affected by outliers  
✔ Better for skewed data  

##  Cons
✖ Does not scale values to a fixed range  
✖ May distort normally distributed data  

---

#  Summary Table

| Scaler | What It Does | Best For | Outliers |
|--------|--------------|----------|-----------|
| **StandardScaler** | Normalize using mean & std | Normal distributions | ❌ Sensitive |
| **MinMaxScaler** | Scale to 0–1 | Neural nets, KNN | ❌ Very Sensitive |
| **RobustScaler** | Median & IQR | Outlier-heavy data | ✅ Resistant |

---

