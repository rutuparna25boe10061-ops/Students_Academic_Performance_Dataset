# Students_Academic_Performance_Dataset
# 🎓 Student Performance Classification Model

## Project Title
**Predicting Student Academic Success: A Classification Approach**

## Overview of the Project
This project develops a **Machine Learning Classification Model** to predict a student's final academic performance level (categorized as **High Performer** or **Low Performer**) based on their demographic, socioeconomic, and preparatory attributes. The goal is to provide educational institutions with an early warning system to identify students at risk of failure, allowing for proactive intervention.

The model uses the **Random Forest Classifier** algorithm, chosen for its robustness and ability to provide useful feature importance insights.

## Features
1.  **Data Preprocessing:** Cleans and transforms raw categorical data (e.g., `gender`, `lunch` status) into a machine-readable numerical format using **One-Hot Encoding**.
2.  **Feature Engineering:** Creates a composite target variable, **`Performance_Level`**, by averaging the three subject scores and applying a predefined success threshold (average score $\ge 70$).
3.  **Model Training & Tuning:** Builds a full **Scikit-learn Pipeline** for automated feature transformation and model fitting. It uses **Grid Search** to optimize the model's hyperparameters for maximum predictive accuracy.
4.  **Prediction Interface:** Provides a function to take new student data and output a definitive prediction: **High Performer (Success)** or **Low Performer (Failure)**.
5.  **Reporting:** Generates key evaluation metrics (Accuracy, Precision, Recall) and visualizations (Confusion Matrix, Feature Importance) for comprehensive model assessment.

## Technologies/Tools Used
* **Language:** Python
* **Core Libraries:**
    * **Pandas:** Data manipulation and analysis.
    * **NumPy:** Numerical operations.
    * **Scikit-learn (sklearn):** Machine Learning modeling, preprocessing, and evaluation.
    * **Matplotlib/Seaborn:** Data visualization.
* **Model Persistence:** `pickle` (for saving and loading the trained model).

## Project Files
| File Name | Description |
| :--- | :--- |
| **`StudentsPerformance.csv`** | The raw dataset containing student attributes and scores. |
| **`student_performance_project.py`** | The main Python script implementing the end-to-end ML project workflow. |
| **`statement.md`** | **Problem Statement** and **Scope** document (required for submission). |
| **`student_performance_classifier.pkl`** | The serialized, trained **Random Forest Model** output (generated after running the script). |
| **`confusion_matrix.png`** | Visualization of the model's performance on the test set. |
| **`feature_importance.png`** | Chart showing the most influential features in the prediction model. |

## Steps to Install & Run the Project

### Prerequisites
You need a Python environment installed on your system.

### 1. Installation
Install the required Python libraries using pip:
```bash
pip install pandas scikit-learn numpy matplotlib seaborn
