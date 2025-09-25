# Mobile Price Prediction Project

This project analyzes a dataset of mobile phone specifications and predicts the price range category of the devices. The project includes data exploration, preprocessing, visualization, and multiple machine learning models for classification.

---

## 📁 Dataset Overview

- **Shape:** 2000 rows × 21 columns
- **Columns:** ['battery_power', 'blue', 'clock_speed', 'dual_sim', 'fc', 'four_g',
'int_memory', 'm_dep', 'mobile_wt', 'n_cores', 'pc', 'px_height',
'px_width', 'ram', 'sc_h', 'sc_w', 'talk_time', 'three_g',
'touch_screen', 'wifi', 'price_range']


- **Data Types:**  
  - Numeric: 21 (int64 and float64)  
  - Non-numeric: None

- **Target Variable:** `price_range` (0, 1, 2, 3), each with 500 instances.

---

## 🔍 Data Analysis & Visualization

- Checked for missing values → **No null values found**.  
- Explored feature distributions, unique values, and statistical summaries.  
- Correlation with target (`price_range`):  
  - Strongest correlation: `ram` (~0.917)  
  - Moderate: `battery_power`, `px_width`, `px_height`  
  - Weak/low: `touch_screen`, `mobile_wt`, `clock_speed`  

- Visualizations included:
  - Distribution plots of features
  - Correlation heatmaps
  - Barplots of top correlated features

---

## 🤖 Machine Learning Models

Several classification models were trained and evaluated:

| Model                     | Accuracy |
|----------------------------|---------|
| Logistic Regression        | 0.700   |
| Decision Tree              | 0.855   |
| Random Forest              | 0.8525  |
| AdaBoost                   | 0.4975  |
| Bagging                    | 0.8675  |
| K-Nearest Neighbors (KNN)  | 0.9125  |
| Support Vector Classifier (SVC) | 0.9425 |

**Insights:**  
- SVC achieved the highest accuracy (~94.25%).  
- KNN and Bagging also performed well (>86%).  
- AdaBoost underperformed, possibly due to dataset characteristics.

---

## 🛠 Tech Stack

- **Programming Language:** Python 3  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn  

---

## ⚡ Key Highlights

- End-to-end data preprocessing and cleaning
- Feature exploration and visualization
- Training multiple machine learning classifiers
- Identifying top features influencing mobile price prediction

---

## 🚀 Future Improvements

- Hyperparameter tuning for better accuracy
- Cross-validation for robust evaluation
- Model deployment using Flask or Streamlit
