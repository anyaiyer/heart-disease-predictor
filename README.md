# heart-disease-predictor
According to CDC, heart disease is the leading cause of death in the United States. Wouldn't it be great if we tried to diagnose heart disease before it becomes
severe? My model predicts whether a patient has heart disease or not based on the patient's medical reports.
## Download Dataset
This dataset is from UCI Machine Learning and can be downloaded here: https://www.kaggle.com/ronitf/heart-disease-uci 
## Dataset Specifics
In the data, you are given several attributes: 

 1. age
 
 2. sex
 
 3. chest pain type (4 values)
 
 4. resting blood pressure
 
 5. serum cholesterol in mg/dl
 
 6.  fasting blood sugar > 120 mg/dl
 
 7. resting electrocardiographic results (values 0, 1, 2)
 
 8. maximum heart rate achieved
 
 9. exercise induced angina
 
 10. oldpeak = ST depression induced by exercise relative to rest 
 
 11. the slope of the peak exercise ST segment
 
 12.  number of major vessels (0-3) colored by flourosopy
 
 13.   thal: 3 = normal; 6 = fixed defect; 7 = reversable defect

## Algorithm 
This is a classification problem (binary classification) and the results can be interpreted as 0 and 1 (0 = without heart disease, 1 = with heart disease). I used two methods: a [neural network]( https://en.wikipedia.org/wiki/Artificial_neural_network) using **Keras**, and [Logistic Regression](https://en.wikipedia.org/wiki/Logistic_regression#:~:text=Logistic%20regression%20is%20a%20statistical,a%20form%20of%20binary%20regression). My neural network involves the use of [Early Stopping](https://en.wikipedia.org/wiki/Early_stopping) and [Dropout Layers](https://keras.io/api/layers/regularization_layers/dropout/) to prevent overfitting of the data. Logistic Regression is used when dealing with categorical data (in this case, patients with and without heart disease).


| Type | Accuracy |  Precision| Recall|F1-Score|
|--|--|--|--|--|
| Logistic Regression | 85% | 0 = 88%, 1 = 82% | 0 = 80%, 1 = 89% |0 = 83%, 1 = 86%   |
| Neural Network|  87%| 0 = 88%, 1 = 86%| 0 = 84%, 1 = 89%| 0 = 86%, 1 = 88%
## Use
There is a csv file with the dataset: [**heart.csv**](https://github.com/anyaiyer/heart-disease-predictor/blob/main/heart.csv). 

[**Heart Disease Predictor.ipynb**](https://github.com/anyaiyer/heart-disease-predictor/blob/main/Heart%20Disease%20Predictor.ipynb) contains my code (EDA, train test split, and building the model). 

[**heart-disease-predictor.h5**](https://github.com/anyaiyer/heart-disease-predictor/blob/main/heart-disease-predictor.h5) is the Neural Network model with Keras.

[**heart-disease-LR.pkl**](https://github.com/anyaiyer/heart-disease-predictor/blob/main/heart-disease-LR.pkl) is the second model with Logistic Regression.

Use of matplotlib, pandas, numpy, seaborn, scikit learn, and tensorflow.keras is needed. Update to Python 3.5 is recommended.

