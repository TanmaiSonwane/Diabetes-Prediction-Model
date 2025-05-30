# Diabetes-Prediction-Model
Project Overview:
This project aims to predict whether an individual is diabetic based on various health-related features using machine learning. The focus is on robust data preprocessing, effective outlier handling, addressing class imbalance, and optimizing the model for high recall, which is critical in healthcare to minimize missed diabetic cases.

Dataset:
Source: diabetes.csv
Contains health metrics like Glucose, Blood Pressure, Skin Thickness, Insulin, BMI, etc.
No missing values, but contains unrealistic zero values in key columns which require cleaning.

Key Steps & Methodology:
1. Data Cleaning & Imputation:
Invalid zero values replaced using median (for skewed features) or mean (for symmetric distributions) to maintain medical realism.

2. Outlier Detection & Removal:
Used IQR filtering to remove extreme outliers.
Applied additional quantile filtering (99th percentile cutoff) to balance data retention and cleanliness.

3. Standardization:
Features normalized using StandardScaler to ensure equal weighting during model training.

4. Train-Test Split & Imbalance Handling:
Data split with 33% test size.
Addressed class imbalance (more non-diabetic than diabetic cases) using SMOTE (Synthetic Minority Oversampling Technique) to generate synthetic minority class examples and avoid overfitting.

5. Model Training & Evaluation:
Logistic Regression trained on resampled data.
Evaluation focused on recall to prioritize identifying diabetic cases correctly.
Achieved strong recall and accuracy metrics.

6. Model Saving:
Final model saved using pickle for deployment and reuse.

