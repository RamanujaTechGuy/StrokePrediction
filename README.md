# CLASSIFYING STROKE RISK WITH MACHINE LEARNING MODELS

## Introduction
Strokes are medical emergencies where blood flow to the brain is disrupted, potentially causing severe brain damage or death. Predicting stroke risk based on medical, socioeconomic, and lifestyle factors can empower individuals and medical professionals to take preventive action.

> **Did you know?**  
> Each year, over 795,000 people in the United States experience a stroke, with approximately 137,000 resulting in fatalities.

## Objective
This project aims to build a machine learning model to predict the likelihood of a stroke, helping healthcare providers identify high-risk individuals and reduce the overall probability of stroke occurrences. 

## How Machine Learning Can Help
With the vast amount of health data collected from devices like blood pressure monitors and medical imaging systems, machine learning models can uncover patterns and conditions leading to strokes. These insights could enable early intervention and better prevention strategies.

## Methodology
The project follows these steps:
1. **Data Preprocessing**: Cleaning and preparing the dataset for analysis.  
2. **Exploratory Data Analysis (EDA)**: Identifying patterns, correlations, and key risk factors in the data.  
3. **Model Building**: Training various machine learning models to predict stroke risk.  
4. **Model Evaluation**: Comparing model performance using metrics like accuracy, precision, recall, F2-score, and the precision–recall (PR) curve to identify the most effective model on this imbalanced healthcare dataset.

## Model Performance
Because stroke cases are relatively rare in the dataset, the project focuses on recall-oriented metrics such as F2-score and the area under the precision–recall curve (PR-AUC) instead of accuracy alone. The F2-score gives higher weight to recall, which is important in healthcare where missing a high-risk patient is more costly than a false alarm.

- Best model: **Logistic Regression** with **F2-score = `39%`** and **PR-AUC = `19%`**.  
- These metrics indicate the model’s ability to correctly identify stroke-positive cases while handling class imbalance.

## Risk Factor Interpretation (Odds Ratios)
A logistic regression model is used to estimate how each feature changes the odds of experiencing a stroke, reported as odds ratios (OR). An OR greater than 1 indicates higher odds of stroke, while an OR less than 1 indicates lower odds, holding other variables constant.

Example interpretations from this dataset :
    - Glucose Levels: This is the most critical modifiable factor. Elevated average glucose levels are associated with a 33% increase in the odds of having a stroke.

    - Hypertension: A history of high blood pressure contributes to a 24.6% increase in stroke odds.

    - BMI: Higher Body Mass Index accounts for a 14.2% increase in risk.

These odds ratios are derived from the Kaggle stroke prediction dataset and should be interpreted as exploratory insights rather than clinical recommendations.

## Practical Recommendations
Based on the model’s estimates from this dataset:

- Managing blood pressure and **avoiding hypertension may reduce stroke odds by about 24%**, illustrating the importance of early blood pressure control.
- Addressing **heart disease and smoking status** can substantially lower estimated stroke risk, highlighting the value of regular check-ups, cardiac care, and smoking cessation.

These recommendations summarize what the model sees in this dataset and should be complemented with medical guidance from healthcare professionals.

## Impact
By using predictive analytics, this project contributes to:
- Identifying the factors that most strongly influence stroke risk in the given dataset. 
- Supporting medical professionals in early diagnosis and intervention by flagging high-risk individuals.  
- Advancing research in healthcare analytics and machine learning through interpretable, data-driven risk estimates.

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

Note: "Unknown" in smoking_status means that the information is unavailable for this patient.

---
Feel free to reach out for any suggestions or collaborations. Let's make a difference in healthcare!
