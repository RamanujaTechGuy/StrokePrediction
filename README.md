# CLASSIFYING STROKE RISK WITH MACHINE LEARNING MODELS

## Introduction
Strokes are medical emergencies where blood flow to the brain is disrupted, potentially causing severe brain damage or death. Predicting stroke risk based on medical, socioeconomic, and lifestyle factors can empower individuals and medical professionals to take preventive action. [web:9][web:13]

> **Did you know?**  
> Each year, over 795,000 people in the United States experience a stroke, with approximately 137,000 resulting in fatalities. [web:9]

## Objective
This project aims to build a machine learning model to predict the likelihood of a stroke, helping healthcare providers identify high-risk individuals and reduce the overall probability of stroke occurrences. [web:9][web:13]

## How Machine Learning Can Help
With the vast amount of health data collected from devices like blood pressure monitors and medical imaging systems, machine learning models can uncover patterns and conditions leading to strokes. These insights could enable early intervention and better prevention strategies. [web:9][web:21]

## Methodology
The project follows these steps:
1. **Data Preprocessing**: Cleaning and preparing the dataset for analysis.  
2. **Exploratory Data Analysis (EDA)**: Identifying patterns, correlations, and key risk factors in the data.  
3. **Model Building**: Training various machine learning models to predict stroke risk.  
4. **Model Evaluation**: Comparing model performance using metrics like accuracy, precision, recall, F2-score, and the precision–recall (PR) curve to identify the most effective model on this imbalanced healthcare dataset. [web:9][web:13]

## Model Performance
Because stroke cases are relatively rare in the dataset, the project focuses on recall-oriented metrics such as F2-score and the area under the precision–recall curve (PR-AUC) instead of accuracy alone. The F2-score gives higher weight to recall, which is important in healthcare where missing a high-risk patient is more costly than a false alarm. [web:9][web:13]

- Best model: **Logistic Regression** with **F2-score = `39%`** and **PR-AUC = `19%`**.  
- These metrics indicate the model’s ability to correctly identify stroke-positive cases while handling class imbalance. [web:9]

## Risk Factor Interpretation (Odds Ratios)
A logistic regression model is used to estimate how each feature changes the odds of experiencing a stroke, reported as odds ratios (OR). An OR greater than 1 indicates higher odds of stroke, while an OR less than 1 indicates lower odds, holding other variables constant. [web:12][web:16][web:20]

Example interpretations from this dataset (replace with your exact values):

- **Hypertension**: Having hypertension is associated with approximately **X% higher odds** of stroke compared to not having hypertension (OR ≈ 1.X).  
- **Heart disease**: The presence of heart disease is linked to about **Y% higher odds** of stroke relative to patients without heart disease (OR ≈ 1.Y).  
- **Current smoking**: Current smokers have roughly **Z% higher odds** of stroke compared to never-smokers (OR ≈ 1.Z).  
- **Protective effect example**: Avoiding hypertension is associated with approximately a **10% reduction** in the odds of stroke in this dataset (OR ≈ 0.90). [web:11][web:20]

These odds ratios are derived from the Kaggle stroke prediction dataset and should be interpreted as exploratory insights rather than clinical recommendations. [web:13][web:16][web:20]

## Practical Recommendations
Based on the model’s estimates from this dataset:

- Managing blood pressure and **avoiding hypertension may reduce stroke odds by about 10%**, illustrating the importance of early blood pressure control. [web:11][web:19]  
- Addressing **heart disease and smoking status** can substantially lower estimated stroke risk, highlighting the value of regular check-ups, cardiac care, and smoking cessation. [web:11][web:15][web:19]

These recommendations summarize what the model sees in this dataset and should be complemented with medical guidance from healthcare professionals. [web:11][web:15]

## Impact
By using predictive analytics, this project contributes to:
- Identifying the factors that most strongly influence stroke risk in the given dataset. [web:9][web:13]  
- Supporting medical professionals in early diagnosis and intervention by flagging high-risk individuals. [web:9]  
- Advancing research in healthcare analytics and machine learning through interpretable, data-driven risk estimates. [web:9][web:21]

## Dataset
1) id: unique identifier  
2) gender: "Male", "Female" or "Other"  
3) age: age of the patient  
4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension  
5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease  
6) ever_married: "No" or "Yes"  
7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"  
8) Residence_type: "Rural" or "Urban"  
9) avg_glucose_level: average glucose level in blood  
10) bmi: body mass index  
11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*  
12) stroke: 1 if the patient had a stroke or 0 if not  

Note: "Unknown" in smoking_status means that the information is unavailable for this patient. [web:13]

---
Feel free to reach out for any suggestions or collaborations. Let's make a difference in healthcare!
