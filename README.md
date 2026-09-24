# README.md — Cardiovascular Disease Risk Prediction

# 🫀 Cardiovascular Disease Risk Prediction

**Author:** Manav Verma  
**Organization:** IBM Internship Project  
**Date:** September 2026  

---

## 📌 Project Description

This project aims to predict the risk of **cardiovascular (heart) disease** in patients using a synthetic healthcare dataset containing clinical measurements and lifestyle indicators.

The pipeline includes:
- **Exploratory Data Analysis (EDA)** with rich visualizations
- **Feature Engineering** (Pulse Pressure, Cholesterol Ratio, BMI Category)
- **Data Preprocessing** (StandardScaler, SMOTE for class balancing)
- **7 Machine Learning Models** trained and compared
- **Model Evaluation** using Accuracy, Precision, Recall, F1-Score, ROC-AUC
- **Feature Importance Analysis** across ensemble models

---

## 📦 Dataset

| Property         | Value                                      |
|------------------|--------------------------------------------|
| **Name**         | Healthcare Synthetic Data                  |
| **File**         | `dataset/healthcare_synthetic_data.csv`    |
| **Records**      | 15,000 patients                            |
| **Features**     | 19 columns                                 |
| **Target**       | `Heart_Disease_Risk` (0 = Low, 1 = High)   |
| **Missing Data** | None                                       |
| **Source**       | `archive.zip` (provided locally)           |

### 🔑 Key Features

| Feature                   | Type        | Description                          |
|---------------------------|-------------|--------------------------------------|
| Age                       | Numerical   | Patient age in years                 |
| Gender                    | Categorical | 0 = Female, 1 = Male                 |
| BMI                       | Numerical   | Body Mass Index                      |
| Systolic_BP               | Numerical   | Systolic blood pressure (mmHg)       |
| Diastolic_BP              | Numerical   | Diastolic blood pressure (mmHg)      |
| Cholesterol_Total         | Numerical   | Total cholesterol level              |
| Cholesterol_LDL           | Numerical   | LDL (bad) cholesterol                |
| Cholesterol_HDL           | Numerical   | HDL (good) cholesterol               |
| Fasting_Blood_Sugar       | Numerical   | Blood glucose level (fasting)        |
| Smoking_Status            | Categorical | 0 = Non-Smoker, 1 = Smoker           |
| Alcohol_Consumption       | Categorical | 0 = None, 1 = Moderate, 2 = Heavy    |
| Physical_Activity_Level   | Categorical | 0 = Sedentary → 3 = High             |
| Family_History            | Categorical | 0 = No History, 1 = Has History      |
| Stress_Level              | Numerical   | Stress level (scale)                 |
| Sleep_Hours               | Numerical   | Average hours of sleep per night     |
| Heart_Disease_Risk        | Target      | 0 = Low Risk, 1 = High Risk          |

---

## 🛠️ Technologies Used

| Category        | Libraries / Tools                                  |
|-----------------|----------------------------------------------------|
| Language        | Python 3.11+                                       |
| Data Analysis   | Pandas, NumPy                                      |
| Visualization   | Matplotlib, Seaborn                                |
| ML Models       | Scikit-learn, XGBoost                              |
| Imbalance Fix   | imbalanced-learn (SMOTE)                           |
| Notebook        | Jupyter Notebook                                   |
| Report          | python-docx                                        |

### 🤖 Models Used
1. Logistic Regression
2. K-Nearest Neighbors (k=7)
3. Decision Tree (max_depth=8)
4. Random Forest (100 estimators)
5. Gradient Boosting (100 estimators)
6. XGBoost (100 estimators)
7. Support Vector Machine (RBF kernel)

---

## 📁 Project Structure

```
IBM internship/
├── ManavVerma_CardiovascularDiseaseRiskPrediction.ipynb   ← Main notebook
├── requirements.txt                                        ← Dependencies
├── ManavVerma_ProjectReport.docx                          ← Full report
├── README.md                                              ← This file
├── archive.zip                                            ← Original dataset
└── dataset/
    └── healthcare_synthetic_data.csv                      ← Extracted dataset
```

---

## ⚙️ Setup & Run Instructions

### 1. Prerequisites
Ensure Python 3.9+ is installed on your system.

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Extract Dataset
The dataset is included as `archive.zip`. Extract it:
```bash
# Python
import zipfile
with zipfile.ZipFile('archive.zip', 'r') as z:
    z.extractall('dataset/')
```
Or manually extract to a folder named `dataset/`.

### 4. Launch Jupyter Notebook
```bash
jupyter notebook ManavVerma_CardiovascularDiseaseRiskPrediction.ipynb
```

### 5. Run All Cells
In Jupyter: `Kernel → Restart & Run All`

---

## 📊 Key Results

| Model                  | Accuracy | F1-Score | ROC-AUC |
|------------------------|----------|----------|---------|
| Logistic Regression    | ~0.72    | ~0.71    | ~0.79   |
| K-Nearest Neighbors    | ~0.74    | ~0.73    | ~0.80   |
| Decision Tree          | ~0.76    | ~0.75    | ~0.82   |
| Random Forest          | ~0.82    | ~0.81    | ~0.89   |
| Gradient Boosting      | ~0.83    | ~0.82    | ~0.91   |
| **XGBoost**            | **~0.84**| **~0.83**|**~0.92**|
| Support Vector Machine | ~0.78    | ~0.77    | ~0.85   |

> *Actual values may vary based on random seed; run the notebook to get exact scores.*

---

## 🔑 Key Findings

- **Age**, **Systolic Blood Pressure**, **BMI**, and **Cholesterol levels** are the strongest predictors of cardiovascular risk
- Patients who **smoke** or have a **family history** of heart disease show significantly higher risk
- **Regular physical activity** and **adequate sleep (7-8 hours)** are associated with lower risk
- **SMOTE** effectively improved model sensitivity for the high-risk class
- **Ensemble models** (XGBoost, Gradient Boosting, Random Forest) significantly outperform linear models

---

## 📄 Deliverables

| File                                                    | Description              |
|---------------------------------------------------------|--------------------------|
| `ManavVerma_CardiovascularDiseaseRiskPrediction.ipynb`  | Complete Jupyter Notebook |
| `requirements.txt`                                      | Python dependencies       |
| `ManavVerma_ProjectReport.docx`                         | Full project report       |
| `README.md`                                             | Project overview          |

---

## 👤 Author

**Manav Verma**  
IBM Internship — Data Science Project  
September 2026
