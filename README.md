# Heart Disease Prediction Using Machine Learning

This repository presents a comprehensive machine learning study focused on predicting **heart disease** using clinical diagnostic data.  
The project includes **end‑to‑end preprocessing, EDA, outlier detection, six ML models, evaluation, and cross‑validation**.

A full technical report is available in:  
`reports/data-mining-project.pdf`

---

## 📌 Project Overview

Heart disease remains a leading global cause of mortality. Early identification significantly improves patient outcomes.  
This project uses machine learning techniques to classify patients based on demographic and clinical measurements.

The study covers:

- Rigorous **data preprocessing & cleaning**
- Extensive **EDA**
- Multiple **outlier‑detection frameworks**
- Training & evaluation of **six ML models**
- Visualizations, interpretability elements, and model comparison

---

## 👥 Team Members

- Seif Amjad Sobeih Heidar
- Abdelrahman Wael Maher  
- Ahmed Hossam Abdallah 
- Youssef Ahmed Farouk  
- Youssef Farid Haddad   
- Marwan Wagih Mohammed 

---

## 📁 Repository Structure

```
heart-disease-prediction-ml/
│
├── README.md
├── Project_2_Simple.ipynb
│
├── data/
│   └── heart.csv
│
├── reports/
    └── data-mining-project.pdf

```

---

## 📊 Dataset Summary

The dataset contains **303 samples** and **14 numeric features**, including patient demographics, clinical exam results, and stress-test outcomes.

### Target Variable
- `target`:  
  - `1` — heart disease present  
  - `0` — no heart disease  

### Categorical Features
`sex`, `cp`, `fbs`, `restecg`, `exang`, `slope`, `ca`, `thal`, `target`

### Numerical Features
`age`, `trestbps`, `chol`, `thalach`, `oldpeak`

---

## 🧹 Data Preprocessing

Key preprocessing steps include:

- Duplicate detection & removal  
- Type consistency checks  
- Categorical & numerical feature separation  
- Handling invalid values (simple/KNN imputation)  
- Outlier detection using:
  - IQR  
  - Isolation Forest  
  - Local Outlier Factor (LOF)  
  - Regression residual analysis  
  - Rare-category detection  

### Scaling & Encoding
Depending on the model:

- StandardScaler  
- RobustScaler  
- PowerTransformer  
- OneHotEncoder  
- ColumnTransformer pipelines  

---

## 📈 Exploratory Data Analysis (EDA)

The notebook provides extensive visual and statistical analysis:

- Histograms & distributions  
- Countplots for categorical variables  
- Boxplots with/without target hue  
- Pairplots (full & reduced)  
- Full and reduced correlation heatmaps  
- Top-correlation extraction for each feature  
- Relationship visualizations (scatter, categorical comparisons)

These analyses guide modeling choices and help identify influential predictors.

---

## 🤖 Machine Learning Models

Six supervised models were developed and evaluated:

### 1️⃣ Decision Tree Classifier
- Entropy criterion  
- Controlled depth to avoid overfitting  
- 10‑fold cross‑validation  

### 2️⃣ Gaussian Naive Bayes
- Winsorization of extreme values  
- PowerTransformer + StandardScaler pipeline  
- Stratified 5‑fold CV  

### 3️⃣ K‑Nearest Neighbors (KNN)
- StandardScaler  
- Search over k = 1–20  
- Stratified 5‑fold CV (Accuracy, F1, ROC‑AUC)

### 4️⃣ Logistic Regression
- Comparison of multiple outlier‑handling methods  
- ColumnTransformer pipeline  
- Metrics: Accuracy, F1, ROC‑AUC (via cross‑validation)

### 5️⃣ Support Vector Machine (SVM)
- RobustScaler  
- GridSearchCV for kernel, C, gamma  
- ROC‑based threshold optimization  
- Train/validation/test evaluation  

### 6️⃣ Random Forest
- Baseline + GridSearchCV tuning  
- Feature importance analysis  
- 5‑fold cross‑validation  

All models include confusion matrices, classification reports, and consistency checks.

---

## ▶️ Running the Project

### 1. Clone the Repository
```bash
git clone https://github.com/AnonyBOSS/heart-disease-prediction-ml.git
cd heart-disease-prediction-ml
```

### 2. Create the Environment
```bash
conda env create -f environment.yml
conda activate heart-disease
```

### 3. Launch the Notebook
```bash
jupyter notebook Project_2_Simple.ipynb
```

Ensure `data/heart.csv` is present in the correct folder.

---

## 📦 Dependencies

- Python 3.10+  
- numpy  
- pandas  
- scikit-learn  
- matplotlib  
- seaborn  
- scipy  
- jupyter  

---

## 📄 Full Report

For full methodology, results, and visualizations:

```
reports/data-mining-project.pdf
```


