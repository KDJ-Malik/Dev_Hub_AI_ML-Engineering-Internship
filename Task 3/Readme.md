# Task 3: Heart Disease Prediction

## Objective
The objective of this task is to build an ML classification model that predicts whether a person is at risk of heart disease based on medical and health-related attributes.

The project focuses on:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Binary classification modeling
- Performance evaluation using classification metrics
- Identifying important health factors affecting prediction

---

## Dataset Used

**Dataset:** UCI Heart Disease Dataset  
**Source:** UCI Machine Learning Repository

The dataset contains medical information collected from patients and is commonly used for heart disease prediction research.

### Dataset Size
- **Total Samples:** 303
- **Training Samples:** 242
- **Testing Samples:** 61

### Features Included

Key medical attributes:

- **age** → Age of patient
- **sex** → Gender
- **cp** → Chest pain type
- **trestbps** → Resting blood pressure
- **chol** → Serum cholesterol
- **fbs** → Fasting blood sugar
- **restecg** → Resting ECG results
- **thalach** → Maximum heart rate achieved
- **exang** → Exercise-induced angina
- **oldpeak** → ST depression induced by exercise
- **slope** → Slope of peak exercise ST segment
- **ca** → Number of major vessels colored by fluoroscopy
- **thal** → Thalassemia blood disorder type

### Target Variable

Binary classification:

- **0** → No Heart Disease
- **1** → Heart Disease Present

---

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Data Cleaning and Preprocessing

### Missing Value Handling
Missing values that were represented by `?` were converted to NaN and replaced using the column median.

### Target Transformation
The target variable was converted into binary format:

- 0 → No Disease
- 1 → Disease

### Feature Scaling
StandardScaler was applied before model training.

### Train-Test Split
The dataset was split using stratified sampling:

- **80% Training**
- **20% Testing**

---

## Exploratory Data Analysis (EDA)

Several visualizations were made to understand patterns in the dataset.

### Class Distribution
This displayed the balance between healthy and diseased patients.

**Observation:**  
The classes are relatively balanced.

---

### Feature Distribution Histograms
We coompared distributions of important medical measurements based on the disease status.

Important patterns were observed for:

- Maximum heart rate (`thalach`)
- Chest pain type (`cp`)
- ST depression (`oldpeak`)

---

### Correlation Heatmap
A correlation heatmap visualized relationships between numerical variables.

**Observation:**  
Several clinical indicators showed meaningful relationships with disease presence.

---

## Models Applied

### 1. Logistic Regression

A linear classification model used as a strong baseline for binary prediction.

**Accuracy:**  
**86.89%**

---

### 2. Decision Tree Classifier

A non-linear model capable of capturing decision boundaries through hierarchical splits.

**Accuracy:**  
**77.05%**

---

## Model Evaluation Metrics

Models were evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve
- ROC-AUC Score

---

## Logistic Regression Results

### Classification Performance

| Metric | Value |
|--------|-------|
| Accuracy | 86.89% |
| Precision (Disease) | 0.81 |
| Recall (Disease) | 0.93 |
| F1-score | 0.87 |

### Key Strength
High recall for disease detection, making it effective for identifying at-risk patients.

---

## Decision Tree Results

### Classification Performance

| Metric | Value |
|--------|-------|
| Accuracy | 77.05% |
| Precision (Disease) | 0.71 |
| Recall (Disease) | 0.86 |
| F1-score | 0.77 |

### Key Strength
Interpretable decision rules for clinical understanding.

---

## Performance Comparison

| Model | Accuracy |
|-------|----------|
| Logistic Regression | **86.89%** |
| Decision Tree | **77.05%** |

**Best Performing Model:** Logistic Regression

---

## Feature Importance Analysis

### Top Features (Logistic Regression)

| Feature | Coefficient |
|---------|-------------|
| sex | 0.655563 |
| thal | 0.677821 |
| ca | 1.107898 |

---

### Top Features (Decision Tree)

| Feature | Importance |
|---------|------------|
| ca | 0.116874 |
| cp | 0.151595 |
| thal | 0.378859 |

---

## Most Predictive Clinical Indicators

| Feature | Meaning |
|---------|---------|
| **thalach** | Maximum heart rate achieved |
| **cp** | Chest pain type |
| **oldpeak** | ST depression induced by exercise |
| **ca** | Number of major vessels colored by fluoroscopy |
| **thal** | Thalassemia blood disorder type |

These features showed the strongest relationship with heart disease risk.

---

## Key Findings

### Logistic Regression Performed Best
It achieved the highest overall predictive performance.

### Chest Pain and Blood Vessel Count Mattered Most
Clinical indicators such as chest pain type and vessel blockage are highly predictive.

### Heart Rate and Exercise Response Are Strong Signals
Exercise-induced measurements significantly contribute to diagnosis.

### Medical Data Can Effectively Predict Risk
Machine learning can support early risk detection when trained on clinical measurements.

---

## Conclusion

This project successfully demonstrates binary classification for heart disease prediction using medical data.

Among the models tested, **Logistic Regression outperformed Decision Tree**, achieving **86.89% accuracy**, strong recall, and reliable classification performance.

The analysis shows that features such as **thal, chest pain type, major vessel count, and exercise-induced cardiac stress indicators** are the most important predictors of heart disease risk.

This highlights the potential of machine learning as a valuable tool for assisting medical diagnosis and early risk assessment.