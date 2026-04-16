# Heart Disease Prediction Project

### 🌟 What this project does
This is a **Machine Learning project** that predicts heart disease. Instead of using just one file, I used **three different datasets** to make the results more reliable:
1.  **Lifestyle Data:** Exercise, smoking, and sleep habits.
2.  **Vitals Data:** Blood pressure and cholesterol levels.
3.  **Hospital Data:** Specific medical tests from doctors.

### 🧠 Smart Features (The "Paradox" Logic)
I created new columns (features) to help the ML model understand a person's health better:
* **Resilience:** Finds people who have a high BMI but are healthy because they exercise and sleep well.
* **Hidden Risk:** Flags young people (under 30) who already show signs of heart problems.
* **Strain:** Measures how "unhealthy" a person feels compared to how much they exercise.

### 🛠️ ML Algorithms Used
* **XGBoost & LightGBM:** Fast and strong models for finding patterns in data.
* **CatBoost:** Great for handling "Yes/No" answers from the survey data.
* **SMOTE-ENN:** A technique to fix "imbalanced data." It helps the model learn about "sick" people since most people in the data were "healthy."
* **Stacking:** Combining multiple models together to get the best final answer.

### 📊 The Triple-Vote System
I built a **Consensus Engine**. It works like a team of three experts. Each expert is an ML model trained on a different dataset. They all vote on a patient’s risk to give a final score.

* **Heart_2020:** 86% Accuracy (Optimized to catch more sick people).
* **Cardio Data:** 72% Accuracy.
* **Hospital Data:** 91% Accuracy.

### 🚀 How to Run
1.  Download `code1.ipynb` and the three CSV data files.
2.  Install the tools: `pip install xgboost lightgbm catboost optuna imblearn`.
3.  Open the notebook and run all cells.

**Note:** For the survey data, I used a **0.18 threshold**. This makes the ML model "extra careful" so it doesn't miss anyone who might actually be sick.
