# Arthritis Prediction

## Overview    

The goal of this project was to select an optimal classification machine learning model to predict whether or not a participant in the survey has arthritis based on the answers. 
The data ultilized by the project was a part of the 2018 Behavioral Risk Factor Surveillance System (BRFSS) Survey Data prepared by CDC. The final XGBoost model performed with 73% accuracy and 0.78 ROC_AUC socre determing what features are most important in seperating participants who have arthritis from who do not have arthritis. Based on the model, age, physical health, health status, health access, and BMI category were the most predictive variables in classifying arthritis.  

## Business Understanding    

Arthritis, a chronic condition affecting millions worldwide, significantly impacts quality of life, productivity, and healthcare costs. Whereas, early detection and timely intervention can slow disease progression, reduce pain, and maintain joint function. Early intervention and treatment can not only help patients maintain independence, productivity, and overall well-being, but also prevent costly surgeries, hospitalizations, and long-term care.
By developing a predictive model using survey data to identify individuals at high risk of developing arthritis, healthcare providers can implement targeted screening and early intervention programs, optimize resource allocation for prevention and treatment, and reduce the overall burden of arthritis on individuals and society.

## Data Understanding    

BRFSS’s objective is to collect uniform state-specific data on health risk behaviors, chronic diseases and conditions, access to health care, and use of preventive health services related to the leading causes of death and disability in the United States. Factors assessed by the BRFSS in 2018 included health status, healthy days/health-related quality of life, health care access, exercise, inadequate sleep, chronic health conditions, oral health, tobacco use, e-cigarettes, alcohol consumption, immunization, falls, seat belt use, drinking and driving, breast- and cervical cancer screening, prostate cancer screening, colorectal cancer screening, and HIV/AIDS knowledge. (link to the data information and documentation: https://www.cdc.gov/brfss/annual_data/annual_2018.html). In this project, 17 caculated variables were selected for analysis. The common focus of these variables is on health behaviors that are associated with a risk of illness or injury. 

![image](https://github.com/user-attachments/assets/fc652e8a-d771-4fe2-ad7b-68c9eb1b62d2)    

Arthritis column with labels 0 and 1 and sex column with labels 1 and 2 were seleted. All the duplicated values and missing values were removed. 

## Modeling and Evaluation
Naïve Bayes, Logistic regression, Neural, KNN, SVC, and three tree-based models (Decision tree, Random forest, XGBoost) were built. Their performances on the test data were compared. Finally, The Naïve Bayes model has the best recall on the test data and the XGBoost model had the best overall performance across all the metrics. The below plots show the confusion matrix for Naïve Bayes classification and feature importance in the XGBoost model.    

![image](https://github.com/user-attachments/assets/b909c33c-f3ac-4047-9e17-d87ea53cebf3)    
confusion matrix for Naïve Bayes classification


![image](https://github.com/user-attachments/assets/1907b353-4060-4de9-a424-9d15d5707151)    
The top five predictive features in the XGBoost model for arthritis are age, physical health, health status, health access, and BMI category if we exclude sex. 

## Conclusion    
The developed model offers potential benefits to healthcare providers by predicting the likelihood of arthritis based on patient responses to specific questions. However, the model's moderate recall rate presents a significant limitation. This means that a proportion of patients with arthritis might be incorrectly classified as arthritis-free, potentially leading to adverse consequences, including legal liabilities for healthcare organizations.

This project serves as a foundational exploration of the dataset's potential for arthritis prediction. To enhance model performance, future research should focus on refining data quality by addressing missing, inconsistant or irrelevant values, incorporating additional relevant features, and expanding the dataset for training.



