# Student Dropout Prediction

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Model](https://img.shields.io/badge/Model-LightGBM-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Overview
Not every dropout becomes the next Bill Gates. In reality, student dropout rates are a major challenge for universities.

This project analyzes demographic, socioeconomic, and academic data to identify key factors contributing to student dropout. I built and compared several Machine Learning models to predict whether a student will **Dropout**, **Graduate**, or remain **Enrolled**.

## The Data
The dataset is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success).
* **Target Variable:** `Dropout`, `Enrolled`, `Graduate`.
* **Features:** ~36 features including tuition fees, scholarship status, inflation rates, and grades from the 1st and 2nd semesters.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn.
* **Main Algorithm:** LightGBM (Gradient Boosting).

## Key Findings & Process

### 1. Data Cleaning & EDA
* Handled class imbalance using **SMOTE**.
* Analyzed correlations between financial pressure (debt/tuition) and academic performance.

### 2. What actually causes dropouts?
Based on the Feature Importance analysis, the strongest predictors were:
* **2nd Semester Grades:** If performance drops here, dropout risk spikes.
* **Tuition Fees:** Students with overdue payments are significantly more likely to leave.
* **1st Semester Grades:** Early academic struggles are a major red flag.

### 3. Modeling Results
I tested Logistic Regression, Decision Trees, and Random Forest, but **Ensemble Learning (LightGBM)** provided the best balance between precision and recall, especially for distinguishing between the 'Dropout' and 'Graduate' classes.

## How to Run

1.  **Clone the repo**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    ```

2.  **Install dependencies**
    ```bash
    pip install pandas numpy scikit-learn lightgbm matplotlib seaborn imbalanced-learn
    ```

3.  **Run the Notebook**
    Open `Project 2.ipynb` in Jupyter Notebook or Google Colab to see the full analysis and training process.

---
**Author:** Nguyen Hung Long
