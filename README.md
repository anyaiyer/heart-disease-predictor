# heart-disease-predictor
According to CDC, heart disease is the leading cause of death in the United States. Wouldn't it be great if we tried to diagnose heart disease before it becomes
severe? My model predicts whether a patient has heart disease or not based on the patient's medical reports.

## Download Dataset
This dataset is from UCI Machine Learning and can be downloaded here: https://www.kaggle.com/ronitf/heart-disease-uci 

## Dataset Specifics
In the data, you are given several attributes: age, sex, chest pain type (4 values), resting blood pressure, serum cholestoral in mg/dl, 
fasting blood sugar > 120 mg/dl, resting electrocardiographic results (values 0,1,2), maximum heart rate achieved, exercise induced angina, 
oldpeak = ST depression induced by exercise relative to rest, the slope of the peak exercise ST segment, number of major vessels (0-3) colored by flourosopy,
thal: 3 = normal; 6 = fixed defect; 7 = reversable defect. 

## Algorthim 
This is a classification problem (binary classification) and the results can be intrepreted as 0 and 1 (0 = without heart disease, 1 = with heart disease).
I used two methods: a neural network using Keras, and Logistic Regression. My neural network involves the use of Early Stopping and Dropout
Layers to prevent overfitting of the data. Logistic Regression is used when dealing with categorical data (in this case, patients with and without heart disease).
My neural network had an overall accuracy of 87% while my model involving Logistic Regression had an accuracy of 85%. 

## Use
There is a csv file with the dataset. Heart Disease Predictor.ipynb contains my code (EDA, model, and save model). 


