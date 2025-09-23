# Linear Regression

This folder contains implementations and experiments using **Linear Regression** and its variants.

---

## What is Linear Regression?
Linear Regression is one of the most fundamental algorithms in **supervised learning**.  
It models the relationship between input features (**X**) and a continuous target variable (**y**) by fitting a linear function:

**y ≈ w₀ + w₁ x₁ + w₂ x₂ + ... + w_d x_d**

where `w₀` is the intercept and `w₁,...,w_d` are the coefficients.

---

## Types of Linear Regression
1. **Ordinary Least Squares (OLS)** → minimizes the sum of squared errors.  
2. **Ridge Regression (L2 Regularization)** → penalizes large coefficients to reduce overfitting.  
3. **Lasso Regression (L1 Regularization)** → encourages sparsity, some coefficients become 0.  
4. **Elastic Net** → combination of Ridge and Lasso.  

---

## scikit-learn Usage
- `LinearRegression()` → Ordinary Least Squares  
- `Ridge(alpha=1.0)` → Ridge Regression  
- `Lasso(alpha=1.0)` → Lasso Regression  
- `ElasticNet(alpha=1.0, l1_ratio=0.5)` → Elastic Net  

All models follow the same workflow:

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
```