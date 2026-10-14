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
| **01** | **Introduction to Machine Learning** | [Homework 1 Notebook](notebooks/homeworks/Homework%201:%20Introduction%20to%20Machine%20Learning.ipynb) | ✅ Completed |
| **02** | **Machine Learning for Regression** | [Homework 2 Notebook](notebooks/homeworks/Homework%202:%20Machine%20Learning%20for%20Regression.ipynb) | ✅ Completed |
| **03** | **Machine Learning for Classification** | [Homework 3 Notebook](notebooks/homeworks/Homework%203:%20Machine%20Learning%20for%20Classification.ipynb) | ✅ Completed |
| **04** | Evaluation Metrics for Machine Learning | `notebooks/homeworks/` | 📅 Upcoming |
| **05** | Deploying Machine Learning Models | `deployment/` | 📅 Upcoming |
| **06** | Decision Trees and Ensemble Learning | `notebooks/homeworks/` | 📅 Upcoming |
| **Project 1** | **Midterm Project** | `projects/midterm/` | 📅 Upcoming |
| **08** | Deep Learning | `notebooks/homeworks/` | 📅 Upcoming |
| **09** | Serverless Deep Learning | `notebooks/homeworks/` | 📅 Upcoming |
| **10** | Kubernetes and TensorFlow Serving | `notebooks/homeworks/` | 📅 Upcoming |
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

Full interactive code and outputs can be viewed in [`notebooks/homeworks/Homework 1: Introduction to Machine Learning.ipynb`](notebooks/homeworks/Homework%201:%20Introduction%20to%20Machine%20Learning.ipynb).

---

## 📝 Homework 3: Machine Learning for Classification Summary

Dataset used: [2026 Lead Scoring Dataset](data/course_lead_scoring_2026.csv) (`course_lead_scoring_2026.csv`)  
Target: `converted` (binary classification)

### Key Results & Submission Answers

| # | Question | Answer | Method / Explanation |
|---|---|:---:|---|
| **1** | **Mode of `industry`** | `technology` | Most frequent category with 1,173 occurrences |
| **2** | **Features with biggest correlation** | `interaction_count` and `lead_score` | Pearson correlation coefficient $r = 0.9157$ |
| **3** | **Feature with highest mutual information** | `lead_source` | Mutual information score = 0.03 (vs employment_status: 0.02, industry: 0.00, location: 0.00) |
| **4** | **Logistic regression accuracy** | `0.65` | Model accuracy on validation set = 0.6450 (rounds to **0.65**) |
| **5** | **Feature with smallest accuracy difference** | `'number_of_courses_viewed'` | Accuracy drop when excluded: only **0.0020** (0.6450 → 0.6430) |
| **6** | **Best parameter `C`** | `0.001` | Evaluated across $[10^{-6}, 10^{-5}, 10^{-4}, 10^{-3}]$; $C = 0.001$ gives top validation accuracy (0.645) |

Full interactive code, correlation heatmap, and outputs can be viewed in [`notebooks/homeworks/Homework 3: Machine Learning for Classification.ipynb`](notebooks/homeworks/Homework%203:%20Machine%20Learning%20for%20Classification.ipynb).

---

## 📁 Repository Structure

```text
├── data/
│   ├── car_fuel_efficiency_2026.csv     # 2026 Car fuel efficiency dataset (10k records)
│   ├── course_lead_scoring_2026.csv     # 2026 Lead scoring dataset (5k records)
│   ├── homework_2026.md                  # Official assignment instructions for HW1
│   └── homework_03.md                    # Official assignment instructions for HW3
├── notebooks/
│   ├── homeworks/
│   │   ├── Homework 1: Introduction to Machine Learning.ipynb
│   │   ├── Homework 2: Machine Learning for Regression.ipynb
│   │   └── Homework 3: Machine Learning for Classification.ipynb
│   ├── 01_eda.ipynb
│   ├── 02_data_transformation.ipynb
│   └── 03_training_and_analysis.ipynb
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
