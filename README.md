# 🚗 Car Rental & Price Prediction System

[![Python](https://img.shields.io/badge/Python-3.11%20%7C%203.14-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.24%2B-013243?logo=numpy&logoColor=white)](https://numpy.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3%2B-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![ML Zoomcamp](https://img.shields.io/badge/DataTalks.Club-ML%20Zoomcamp%202026-orange)](https://datatalks.club/courses/machine-learning-zoomcamp.html)

> End-to-end machine learning system for predicting vehicle prices, rental valuations, and fuel efficiency metrics. Developed as part of the **[DataTalks.Club Machine Learning Zoomcamp](https://github.com/DataTalksClub/machine-learning-zoomcamp) (2026 Cohort)**.

---

## 📌 Project Overview

This repository hosts the practical coursework, exploratory data analysis, and predictive modeling pipelines for vehicle data analytics. The core goal is to build robust, reproducible machine learning models that estimate vehicle market valuation and efficiency from underlying technical specifications (engine displacement, horsepower, weight, cylinders, drivetrain, etc.).

All code and assignments adhere to the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** methodology covered in the course.

---

## 📚 Machine Learning Zoomcamp Progress

| Module | Topic | Notebook / Code | Status |
|---|---|---|:---:|
| **01** | **Introduction to Machine Learning** | [Homework 1 Notebook](homework_notebooks/Homework%201:%20Introduction%20to%20Machine%20Learning.ipynb) | ✅ Completed |
| **02** | Machine Learning for Regression | `homework_notebooks/02-regression/` | ⏳ In Progress |
| **03** | Machine Learning for Classification | `homework_notebooks/03-classification/` | 📅 Upcoming |
| **04** | Evaluation Metrics for Machine Learning | `homework_notebooks/04-evaluation/` | 📅 Upcoming |
| **05** | Deploying Machine Learning Models | `deployment/` | 📅 Upcoming |
| **06** | Decision Trees and Ensemble Learning | `homework_notebooks/06-trees/` | 📅 Upcoming |
| **Project 1** | **Midterm Project** | `projects/midterm/` | 📅 Upcoming |
| **08** | Deep Learning | `homework_notebooks/08-deep-learning/` | 📅 Upcoming |
| **09** | Serverless Deep Learning | `homework_notebooks/09-serverless/` | 📅 Upcoming |
| **10** | Kubernetes and TensorFlow Serving | `homework_notebooks/10-kubernetes/` | 📅 Upcoming |
| **Project 2** | **Capstone Project** | `projects/capstone/` | 📅 Upcoming |

---

## 📝 Homework 1: Introduction to Machine Learning Summary

Dataset used: [2026 Car Fuel Efficiency Dataset](data/car_fuel_efficiency_2026.csv) (`car_fuel_efficiency_2026.csv`)

### Key Results & Submission Answers

| # | Question | Answer | Formula / Method |
|---|---|:---:|---|
| **1** | **Pandas version** | `3.0.6` | `pd.__version__` |
| **2** | **Records count** | `10000` | `len(df)` |
| **3** | **Fuel types count** | `3` | `df['fuel_type'].nunique()` (`Gasoline`, `Diesel`, `Hybrid`) |
| **4** | **Columns with missing values** | `2` | `(df.isna().sum() > 0).sum()` (`horsepower`: 877, `acceleration`: 264) |
| **5** | **Max fuel efficiency** | `41.2` | `df[df['origin'] == 'Asia']['fuel_efficiency_mpg'].max()` |
| **6** | **Median value of horsepower** | `Yes, it decreased` | Median before: `254.0` → mode: `252.0` → Median after imputation: `252.0` |
| **7** | **Sum of weights** | `0.369` | Normal Equation: $w = (X^T X)^{-1} X^T y$, $\sum w \approx 0.3692$ |

Full interactive code and outputs can be viewed in [`homework_notebooks/Homework 1: Introduction to Machine Learning.ipynb`](homework_notebooks/Homework%201:%20Introduction%20to%20Machine%20Learning.ipynb).

---

## 📁 Repository Structure

```text
├── data/
│   ├── car_fuel_efficiency_2026.csv     # 2026 Car fuel efficiency dataset (10k records)
│   ├── data.csv                          # Car features and MSRP dataset (11.9k records)
│   └── homework_2026.md                  # Official assignment instructions (Cohort 2026)
├── homework_notebooks/
│   └── Homework 1: Introduction to Machine Learning.ipynb   # Completed HW1 notebook
├── requirements.txt                      # Project dependencies
├── .gitignore                            # Clean git exclusion rules
└── README.md                             # Project documentation & progress
```

---

## 🚀 Setup & Reproducibility

### 1. Clone the repository
```bash
git clone git@github.com:bkget/car-rental-prediction-system.git
cd car-rental-prediction-system
```

### 2. Create and activate a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```
Navigate to `homework_notebooks/` and open `Homework 1: Introduction to Machine Learning.ipynb`.

---

## 👤 Author

**Biruk Getaneh**
- GitHub: [@bkget](https://github.com/bkget)
- Course: [DataTalks.Club Machine Learning Zoomcamp (2026)](https://datatalks.club/courses/machine-learning-zoomcamp.html)
