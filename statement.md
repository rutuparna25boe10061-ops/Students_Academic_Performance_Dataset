# Problem Statement & Scope

## Problem Statement
Educational institutions often struggle with reactively addressing student underperformance. This project addresses the need for a **proactive early warning system** by building a machine learning classification model to predict a student's final academic performance level based on their pre-existing attributes. The objective is to identify students who are at risk of achieving a **Low Performer** status, allowing educators to intervene with targeted support and resources before final examination results.

## Scope of the Project
The project is scoped as a **Supervised Classification Model** using the provided student dataset.

* **Input Data:** The model uses demographic (`gender`, `race/ethnicity`), socioeconomic (`lunch`), parental (`parental level of education`), and preparatory (`test preparation course`) features.
* **Prediction Task:** Binary classification.
* **Target Variable:** An engineered variable, **`Performance_Level`**, defined as **1 (High Performer)** for students with an average score $\ge 70$ and **0 (Low Performer)** for those below.
* **Modeling:** Implementation, training, and tuning of a **Random Forest Classifier** model via a Scikit-learn Pipeline.
* **Output:** The model outputs a definitive prediction of the student's performance category and provides clear performance metrics (Accuracy, Precision, Recall) and feature importance analysis.

## Target Users
The primary beneficiaries of this system are:

* **School Administrators:** To allocate resources (e.g., tutoring, counseling) efficiently.
* **Teachers/Educators:** To identify and monitor at-risk students for personalized teaching approaches.
* **Academic Counselors:** To use data-driven insights for student advisory services.

## High-Level Features (Functional Modules)

The system is built upon three major functional modules:

1.  **Data Preprocessing & Engineering:**
    * Loads and cleans the raw data.
    * Creates the binary **`Performance_Level`** target variable.
    * Transforms all categorical features into numerical format using One-Hot Encoding.
2.  **Model Training & Tuning:**
    * Splits the data into training and testing sets.
    * Trains a **Random Forest Classifier** within a robust Scikit-learn Pipeline.
    * Applies **Grid Search** for hyperparameter optimization to select the best-performing model.
    * Saves the final trained model (`.pkl` file).
3.  **Prediction & Reporting Interface:**
    * Generates comprehensive evaluation metrics (Classification Report, Confusion Matrix).
    * Produces visualizations for model interpretability (**Feature Importance**).
    * Accepts new student data and predicts their expected academic performance class.
