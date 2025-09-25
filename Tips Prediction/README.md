# Tip Prediction Dataset Analysis

This repository contains a detailed analysis of a dataset containing restaurant tips, along with training and evaluation of multiple regression models.

---

## 📊 Dataset Overview

- **Shape of dataset:** `(244, 7)`  
- **Columns:** `['total_bill', 'tip', 'sex', 'smoker', 'day', 'time', 'size']`  

### Data Types
| Column       | Data Type |
|-------------|-----------|
| total_bill  | float64   |
| tip         | float64   |
| sex         | object    |
| smoker      | object    |
| day         | object    |
| time        | object    |
| size        | int64     |

- **Number of entries:** 244  
- **Memory usage:** ~13.5 KB  

---

## 🔹 Numerical Columns
`['total_bill', 'tip', 'size']`  

### Descriptive Statistics
| Column      | Count | Mean    | Std      | Min   | 25%    | 50%    | 75%    | Max   |
|------------|-------|---------|---------|-------|--------|--------|--------|-------|
| total_bill | 244   | 19.786  | 8.902   | 3.07  | 13.348 | 17.795 | 24.128 | 50.81 |
| tip        | 244   | 2.998   | 1.384   | 1.0   | 2.0    | 2.9    | 3.563  | 10.0  |
| size       | 244   | 2.570   | 0.951   | 1.0   | 2.0    | 2.0    | 3.0    | 6.0   |

---

## 🔹 Categorical Columns
`['sex', 'smoker', 'day', 'time']`  

---

## 🛠️ Models Trained

Multiple regression models were trained to predict `tip` based on the other features.

| Model                     | R² Score | RMSE  | Notes |
|----------------------------|----------|-------|-------|
| Linear Regression (LR)     | 0.488    | 1.161 | Baseline linear model |
| Decision Tree Regressor    | 0.027    | 1.600 | Poor performance, may overfit/underfit |
| Ridge Regression           | 0.493    | 1.155 | Regularized linear regression, slight improvement |
| Lasso Regression           | 0.488    | 1.161 | L1 regularization, similar to baseline |

---

## 🔹 Insights
- Linear and Ridge regression models perform best for this dataset.  
- Decision Tree regression struggles, possibly due to small dataset size and lack of strong non-linear patterns.  
- Feature scaling or feature engineering may further improve model performance.  

---

## 🔹 Purpose
- To demonstrate exploratory data analysis (EDA) for a small dataset.  
- To train multiple regression models and compare their performance.  
- To provide a clear workflow for dataset analysis and predictive modeling.  

---

## ⚡ Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  

---

## 🔹 Project Structure
