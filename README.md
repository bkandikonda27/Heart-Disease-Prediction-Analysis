# Heart-Failure-Prediction-Analysis
Predicting Heart Failure based off Data received from Kaggle.


## Introduction
Heart Failure leads to over 600,000 deaths in America alone. The chart below from the World Health Organization (WHO) shows that heart failure was the most significant cause of death in 2000 and 2019, only growing its lead even further in 2019.

Being able to predict heart failure can save millions of lives around the world. I want to dig into this issue not only to uncover findings of what leads to heart failure but also to help medical professionals detect signs of heart failure before it becomes an even bigger problem.


## Data
Dataset: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

The raw dataset was combined from 5 different studies over 11 of the most common features that lead to heart failure. I downloaded this data from Kaggle; it had 918 rows and 12 columns, 1 of which is whether the individual had heart failure or not. The data set was mostly clean but I needed to modify some things to get it ready for further analysis. 
	
Features in the dataset:
1. Age: age of the patient [years]
2. Sex: sex of the patient [M: Male, F: Female]
3. ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
4. RestingBP: resting blood pressure [mm Hg]
5. Cholesterol: serum cholesterol [mm/dl]
6. FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
7. RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
8. MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
9. ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
10. Oldpeak: oldpeak = ST [Numeric value measured in depression]
11. ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
12. HeartDisease: output class [1: heart disease, 0: Normal]

## Exploratory Data Analysis

I found useful information here as the feature importance of each datapoint in the dataset. 
ST Slope, Chest Pain Type, Oldpeak, Max Heart Rate, and Age were the most important features for accurately predicting Heart Disease/Failure.

## Modeling

I used 3 different ML models for this dataset:
- Logistic Regression Classification
- Random Forest Classifier
- K-Nearest Neighbors

I then evaluated these models scores by using numerous criteria which include classification reports, ROC-AUC Curve, Precision-Recall Curve, and confusion matrices.

Logistic Regression Classficication model had the best scores among the 3 models at accurately predicting Heart Failure.

## Conclusion

The most important features for predicting Heart Failure are: ST Slope, Chest Pain Type, Oldpeak, Max Heart Rate, and Age.
I used RFECV to recursively track the most important features and the features mentioned above were always in the final dataset.

Doctor's should actively keep track of ST Slope, Chest Pain Type, Oldpeak, Max Heart Rate, and Age for their patients to check whether or not they are at-risk for Heart Failure.

