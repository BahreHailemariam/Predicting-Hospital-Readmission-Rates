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
