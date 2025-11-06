# 🏥 Predicting Hospital Readmission Rates
*A machine learning–powered healthcare analytics project to identify patients at high risk of being readmitted after discharge.*

---
## 📘 Overview
Hospital readmissions are a critical healthcare metric that affects patient care quality and hospital performance. This project builds a **predictive analytics system** that uses **machine learning** to forecast which patients are most likely to be readmitted within 30 days of discharge.

By leveraging **electronic health record (EHR)** data and other patient-level attributes, this solution helps healthcare providers proactively design interventions, improve outcomes, and optimize hospital resources.

---
## 🎯 Objectives
- Identify factors contributing to frequent hospital readmissions.
- Develop a **predictive model** for readmission risk using historical EHR data.
- Create actionable insights for **care management teams** to reduce preventable readmissions.
- Build a **Power BI dashboard** for real-time visualization and operational monitoring.

---
## 🧩 Key Features
- **Data Cleaning & Preprocessing:** Handles missing data, outliers, and categorical encodings.
- **Feature Engineering:** Derives new variables such as *comorbidity index*, *length of stay*, and *follow-up compliance*.
- **Modeling:** Implements ML models such as Logistic Regression, Random Forest, and XGBoost.
- **Evaluation Metrics:** ROC-AUC, Precision-Recall, F1-score, and Confusion Matrix visualizations.
- **Deployment:** Interactive dashboard and model API integration for ongoing hospital use.

---

## 🧠 Tech Stack
| Category | Tools / Libraries |
|-----------|------------------|
| **Language** | Python 3.10+ |
| **Data Handling** | pandas, numpy, SQLAlchemy |
| **Machine Learning** | scikit-learn, xgboost, imbalanced-learn |
| **Visualization** | matplotlib, seaborn, Power BI |
| **Deployment** | Flask / FastAPI, Streamlit |
| **Version Control** | Git, GitHub |

---
## 📂 Folder Structure
```
Predicting-Hospital-Readmission-Rates/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── scripts/
│   ├── load_data.py
│   ├── clean_data.py
│   ├── feature_engineering.py
│   ├── train_model.py
│   └── app.py
│
├── dashboard/
│   └── PowerBI_Report_Spec.md
│
├── docs/
│   └── Workflow_Spec.md
│
├── requirements.txt
└── README.md
```


---

## ⚙️ Installation
```bash
git clone https://github.com/yourusername/Predicting-Hospital-Readmission-Rates.git
cd Predicting-Hospital-Readmission-Rates
pip install -r requirements.txt
```

---

## 🚀 Usage
```bash
python scripts/load_data.py
python scripts/clean_data.py
python scripts/feature_engineering.py
python scripts/train_model.py
streamlit run scripts/app.py
```

---

## 📊 Power BI Dashboard Preview
This Power BI dashboard transforms predictive analytics and EHR data into actionable insights for hospital management, clinicians, and quality teams. It integrates real-time updates from the model output and supports drill-through analysis for patient-level investigations.

---

## 🩺 1. Readmission Overview

**Objective:**  
Provide a high-level snapshot of hospital performance and patient readmission patterns.

**Visual Components:**
- KPI Cards: 30-Day Readmission Rate, Average Cost per Readmission, Average Length of Stay, Department-wise Readmission Rate
- Trend Line: Monthly readmission rate over time
- Stacked Bar Chart: Department-wise readmission distribution
- Heatmap: Readmission frequency by diagnosis category and age group
- Filters: Department, Diagnosis Group, Month, Insurance Type

**Example DAX Measures:**
```DAX
Readmission Rate (%) =
DIVIDE(
    COUNTROWS(FILTER('Patients', 'Patients'[Readmitted] = 1)),
    COUNTROWS('Patients')
) * 100

Avg Cost per Readmission =
AVERAGE('Patients'[ReadmissionCost])
```

**Business Questions Answered:**
- Which departments have the highest readmission rates?
- Are readmission costs increasing over time?
- What seasonal or temporal patterns exist?

---
## 🧠 2. Patient Risk Profiling

**Objective:**  
Segment and visualize patients by predicted readmission risk levels (Low, Medium, High).

**Visual Components:**
- Scatter Plot: Risk Score vs. Age, colored by risk group
- Table: Patient ID, Age, Diagnosis, Predicted Probability, Risk Category
- Donut Chart: Proportion of patients by risk group
- Histogram: Distribution of predicted probabilities
- KPI Card: Count of High-Risk Patients

**Example DAX Measures:**
```DAX
High Risk Patients =
COUNTROWS(FILTER('Predictions', 'Predictions'[RiskScore] > 0.7))

Avg Risk Score =
AVERAGE('Predictions'[RiskScore])
```

**Business Questions Answered:**
- Which patients are most likely to be readmitted?
- How can care teams prioritize interventions?
- How many high-risk patients were discharged recently?

---
