# Linear Algebra
---
### Why algebra used in ML
- It is a study of linear equation.
- Deals with vector spaces and a special Transformation with vector spaces called as Linear Transformation.
- To solve a ML Problem with n-Dimensions(n-Features) , with our basic visual skills we can see upto 3-Dimensions.
- we need a procedure to deal with greater than 3D ,that's where we use the concepts of linear algebra.

---

### Basic Terminology:
- **Scalar**: Any single value in an observation is a scalar.
- **Vector**:Every observation in the dataset is a vector.

---

# Linear Algebra Concepts: Linear Combination, Linear Dependence, Linear Independence, Dot Product

## 1. Linear Combination
A linear combination is formed by multiplying vectors with scalars and adding them together.

### **Definition**
Given vectors  
v₁, v₂, ..., vₙ  
and scalars  
a₁, a₂, ..., aₙ  

A linear combination is:
a₁v₁ + a₂v₂ + ... + aₙvₙ

### **Example**
Let  
v₁ = [1, 2]  
v₂ = [3, 1]

Then:
4v₁ − 2v₂ = 4[1,2] − 2[3,1] = [4,8] − [6,2] = [-2, 6]

### **In Machine Learning**
- Linear regression uses linear combinations of features.  
- Feature transformation operations are linear combinations.

---

## 2. Linear Dependence
A set of vectors is linearly dependent if at least one vector can be written as a linear combination of others.

### **Definition**
Vectors v₁, v₂, ..., vₙ are linearly dependent if:
a₁v₁ + a₂v₂ + ... + aₙvₙ = 0  
has a **non-zero** solution for the scalars.

### **Example**
v₁ = [1, 2]  
v₂ = [2, 4]

Here:
v₂ = 2v₁  
So the vectors are **linearly dependent**.

### **In Machine Learning**
- Occurs when features are strongly correlated.  
- Causes multicollinearity in linear regression.  
---

## 3. Linear Independence
Vectors are linearly independent if **no** vector can be written as a linear combination of the others.

### **Definition**
Vectors v₁, v₂, ..., vₙ are independent if:
a₁v₁ + a₂v₂ + ... + aₙvₙ = 0  
has **only the trivial solution**:  
a₁ = a₂ = ... = aₙ = 0

### **Example**
v₁ = [1, 0]  
v₂ = [0, 1]

These cannot be written in terms of each other → **independent**.

### **In Machine Learning**
- Independent features help in better learning.  
- Basis vectors in vector spaces are always independent.  
---

## 4. Dot Product
The dot product measures the similarity or alignment between two vectors.

### **Definition**
For vectors  
x = [x₁, x₂, ..., xₙ]  
y = [y₁, y₂, ..., yₙ]

Dot product:
x · y = x₁y₁ + x₂y₂ + ... + xₙyₙ

### **Geometric Interpretation**
x · y = ‖x‖ ‖y‖ cos(θ)

Where θ is the angle between the vectors.

- If dot product > 0 → angle < 90°, vectors point similarly  
- If dot product = 0 → vectors are orthogonal (independent direction)  
- If dot product < 0 → angle > 90°, vectors point opposite

### **Example**
[1, 2] · [3, 4]  
= 1×3 + 2×4  
= 11

### **In Machine Learning**
- Used in cosine similarity.  
- Neural network weights multiply inputs using dot product.  
- Word embeddings (Word2Vec, GloVe, BERT) rely on dot product to compute similarity.  
- SVM uses dot products in kernel functions.




