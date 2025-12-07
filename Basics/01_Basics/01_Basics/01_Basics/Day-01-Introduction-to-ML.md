# 📘 Day 01 – Introduction to Machine Learning.

## Date  
3/12/2025

---

## What I Learned Today  
I wanted to document the basics of Machine Learning as part of my ML Learning Blog. Today I revised the core ideas that form the foundation of all ML models.

---

##  What is Machine Learning?
Machine Learning (ML) is a field of computer science that enables systems to learn from data and improve automatically, without being explicitly programmed for every scenario.

Instead of giving rules to the computer, we give **data**, and the model learns **patterns**, **relationships**, and **representations** from that data.

---

## 🌍 Why ML is Useful
Machine Learning powers many real-world applications:
- Product recommendations (Amazon, Netflix)
- Spam detection in email
- Credit card fraud detection
- Image classification & object detection
- Speech recognition & chatbots
- Predictive analytics in business

---

## Types of Machine Learning (High-level)
Even though I’ll cover this in detail later, here is a quick overview:

### **1. Supervised Learning**
- Data has labels
- Model learns to predict outcomes  
Examples: Regression, Classification  

### **2. Unsupervised Learning**
- Data has no labels  
- Model finds hidden patterns  
Examples: Clustering, Dimensionality Reduction  

### **3. Reinforcement Learning**
- Model learns through rewards & punishments  
- Used in robotics, gaming, autonomous systems

---

## Simple Example (Python Code)
Here’s a minimal ML workflow using Scikit-Learn:

```python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# Load data
data = load_iris()
X = data.data
y = data.target

# Split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Model
model = LogisticRegression()
model.fit(X_train, y_train)

# Accuracy
print("Accuracy:", model.score(X_test, y_test))
