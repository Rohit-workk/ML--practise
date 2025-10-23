# Fetal Health Classification - Machine Learning Pipeline

---

## 📂 Dataset
Dataset used: [Fetal Health Classification - Kaggle](https://www.kaggle.com/datasets/andrewmvd/fetal-health-classification)  
Number of samples: 2126  
Number of features: 22 (all numerical)  

---

## 🔍 Data Overview
- The dataset contains various features extracted from cardiotocogram (CTG) exams such as baseline value, accelerations, fetal movements, decelerations, variability measures, and histogram statistics.  
- Target variable (`fetal_health`) has 3 classes representing fetal health status.

---

## ⚙️ Preprocessing & Exploratory Data Analysis
- Loaded dataset and confirmed no missing values, ensuring clean data.  
- Detailed feature descriptions with statistical summaries (mean, std, min, max, quartiles).  
- Visualized feature distributions with histograms for all numerical columns.  
- Created a count plot to inspect class distribution of the target variable.  
- Plotted a correlation heatmap to understand inter-feature relationships and feature-target correlations.

---

## 🧩 Feature Importance & Modeling  
- Split dataset into training and testing sets using an 80-20 ratio.  
- Trained a Random Forest Classifier to predict fetal health status.  
- Calculated feature importance, revealing key predictors like:
  - `abnormal_short_term_variability`  
  - `mean_value_of_short_term_variability`  
  - `histogram_mean`  
  - `percentage_of_time_with_abnormal_long_term_variability`

### Performance without Hyperparameter Tuning
- Random Forest model attained ~92.96% accuracy on test data.  
- Confusion matrix showed strong class-wise performance indicating well-balanced predictions.  

---

## 🔧 Model Comparison & Hyperparameter Tuning
- Tested additional classifiers: AdaBoost, Bagging with Decision Trees, and standalone Decision Tree.  
- AdaBoost achieved ~88% accuracy, Bagging and Decision Trees slightly lower.  
- Applied GridSearchCV for AdaBoost and Random Forest for hyperparameter tuning:  
  - AdaBoost best params: `learning_rate=0.1`, `n_estimators=500`; accuracy ~90.11%  
  - Random Forest best params: `max_depth=20`, `min_samples_split=5`, `n_estimators=100`; accuracy ~94.88%  
- Retrained tuned models and compared performance to baseline.

---

## 📊 Summary
- The Random Forest classifier demonstrated high accuracy and identified important clinical features predictive of fetal health status.  
- Model tuning considerably improved AdaBoost and marginally impacted Random Forest performance.  
- Slight overfitting observed in cross-validation compared to test accuracy due to data distribution differences.

---

## 🔮 Future Work
- Experiment with other classifiers such as XGBoost, SVM, or neural networks to enhance performance.  
- Perform deeper feature engineering like interaction terms or dimensionality reduction.  
- Implement model explainability techniques for clinical interpretability.  
- Deploy best performing model to a real-time prediction system for fetal health monitoring.

---

## 📌 Usage
- This pipeline can be run in Python environments with scikit-learn, pandas, numpy, matplotlib, and seaborn.  
- Kaggle Notebooks provide an excellent platform for this analysis with seamless dataset integration.

---
