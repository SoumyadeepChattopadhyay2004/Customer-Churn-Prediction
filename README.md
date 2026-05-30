# 📉 Customer Churn Prediction

> A machine learning project to predict customer churn for a telecommunications company using the IBM Watson Telco dataset.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Methodology](#methodology)
- [Model Comparison](#model-comparison)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Author](#author)

---

## 🔍 Overview

Customer churn — when a customer stops doing business with a company — is one of the most important business metrics for subscription-based industries like telecom. This project builds and compares multiple machine learning models to **predict whether a customer is likely to churn**, enabling proactive retention strategies.

Key goals:
- Explore patterns and trends in customer behavior that correlate with churn
- Build and evaluate multiple classification models
- Identify the most important features driving churn
- Provide actionable business insights

---

## 📂 Dataset

**Source:** [IBM Watson Analytics Sample Data – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
**File:** `WA_Fn-UseC_-Telco-Customer-Churn.csv`

The dataset contains information on **7,043 customers** across **21 features**, including:

| Feature | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `gender` | Customer gender (Male/Female) |
| `SeniorCitizen` | Whether the customer is a senior citizen (1/0) |
| `tenure` | Number of months the customer has stayed |
| `PhoneService` | Whether the customer has phone service |
| `InternetService` | Internet service provider (DSL, Fiber optic, No) |
| `Contract` | Contract type (Month-to-month, One year, Two year) |
| `MonthlyCharges` | Amount charged to the customer monthly |
| `TotalCharges` | Total amount charged |
| `Churn` | **Target variable** — whether the customer churned (Yes/No) |

---

## 🗂️ Project Structure

```
Customer-Churn-Prediction/
│
├── analysis.ipynb                          # Main Jupyter notebook
├── WA_Fn-UseC_-Telco-Customer-Churn.csv   # Dataset
├── requirements.txt                        # Python dependencies
├── Summary.pdf                             # Project summary report
│
├── Chart 1.png                             # EDA visualization 1
├── Chart 2.png                             # EDA visualization 2
├── Chart 3.png                             # EDA visualization 3
├── Chart 4.png                             # EDA visualization 4
├── Chart 5 (Bonus).png                     # Bonus visualization
├── Chart 6 (Additional).png               # Additional visualization
└── model_comparison.png                    # Model performance comparison
```

---

## 📊 Exploratory Data Analysis

The EDA covers:

- **Churn distribution** — understanding the class imbalance
- **Demographic analysis** — churn rates by gender, age group, and dependents
- **Service usage patterns** — how phone, internet, and streaming services relate to churn
- **Contract & billing behavior** — impact of contract type, payment method, and charges
- **Tenure analysis** — how long customers stay before churning
- **Correlation heatmaps** — feature relationships with the churn label

Key findings:
- Customers on **month-to-month contracts** churn significantly more than those on annual contracts
- **Fiber optic internet** users have higher churn rates compared to DSL users
- Customers with **shorter tenure** and **higher monthly charges** are at greater churn risk
- **Electronic check** payment users churn more than those using automatic payment methods

---

## 🧪 Methodology

```
Raw Data
    ↓
Data Cleaning & Preprocessing
    ↓
Exploratory Data Analysis
    ↓
Feature Engineering & Encoding
    ↓
Train / Test Split
    ↓
Model Training & Hyperparameter Tuning
    ↓
Model Evaluation & Comparison
    ↓
Feature Importance Analysis
    ↓
Conclusions & Insights
```

**Preprocessing steps:**
- Handled missing/incorrect values in `TotalCharges`
- Encoded categorical variables using Label Encoding / One-Hot Encoding
- Scaled numerical features where necessary
- Addressed class imbalance

---

## 🤖 Model Comparison

Multiple classification algorithms were trained and evaluated:

| Model | Description |
|---|---|
| Logistic Regression | Baseline linear classifier |
| Decision Tree | Tree-based interpretable model |
| Random Forest | Ensemble of decision trees |
| Gradient Boosting | Sequential boosting ensemble |
| XGBoost | Optimized gradient boosting |
| Support Vector Machine | Margin-based classifier |
| K-Nearest Neighbors | Distance-based classifier |

Models were compared on **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **ROC-AUC**.

See `model_comparison.png` for a visual breakdown.

---

## 📈 Results

The best-performing model achieved strong results on the test set. Key evaluation metrics included ROC-AUC to handle the class imbalance inherent in churn datasets.

> For full metrics and analysis, refer to [`analysis.ipynb`](./analysis.ipynb) or [`Summary.pdf`](./Summary.pdf).

---

## ⚙️ Installation

1. **Clone the repository**

```bash
git clone https://github.com/SoumyadeepChattopadhyay2004/Customer-Churn-Prediction.git
cd Customer-Churn-Prediction
```

2. **Create a virtual environment (recommended)**

```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

Launch Jupyter Notebook and open the main analysis file:

```bash
jupyter notebook analysis.ipynb
```

Run all cells sequentially to reproduce the full analysis — from data loading through EDA, model training, and evaluation.

---

## 🛠️ Technologies Used

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical-013243?logo=numpy)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?logo=scikit-learn)
![XGBoost](https://img.shields.io/badge/XGBoost-Boosting-blue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0)

| Library | Purpose |
|---|---|
| `pandas` | Data manipulation and analysis |
| `numpy` | Numerical computing |
| `matplotlib` & `seaborn` | Data visualization |
| `scikit-learn` | Machine learning models and utilities |
| `xgboost` | Gradient boosting classifier |
| `plotly` | Interactive visualizations |
| `imbalanced-learn` | Handling class imbalance |

---

## 👤 Author

**Soumyadeep Chattopadhyay**

[![GitHub](https://img.shields.io/badge/GitHub-SoumyadeepChattopadhyay2004-181717?logo=github)](https://github.com/SoumyadeepChattopadhyay2004)

---

## 📄 License

This project is open-source and available for educational and research purposes.

---

> ⭐ If you found this project helpful, please consider giving it a star!
