# Diabetes Classification Using Machine Learning Algorithms


## Introduction
The objective of our project is to diagnostically classify whether or not a patient has diabetes, based on certain diagnostic measurements included in the dataset. all patients here are females at least 21 years old of Pima Indian heritage.

**The Features:** Pregnancies, Glucose, blood pressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction & Age
## Methodology
The methodology consists of **4** methods and there are some limitations on the image that should be captured in **good light** with **high resolution** and **not tilted**.

### Method 1: Data Preprocessing

The following steps are followed in this method:
1. Removing NaNs 
2. Balancing the outcome class
3. Feature Importance & Outliers

#### 1. Removing NaNs:
We have found that the Dataset has zero NaN values. However, after some investigations, we have found that the NaNs values were replaced with 0.
so, we dropped all zero values from all the features.

### 2. Balancing the Outcome Class
We have found that the outcome class is not balanced. so, we decided to use oversampling using smote as our data is small to remove from it.
as shown below: 

<img src="https://github.com/a5medashraf/Diabetes-Classification-Using-Machine-Learning-Algorithms/assets/72763763/96083576-3296-4379-a843-a2c1af7f5991" width="250" height="250">

### 3. Feature Importance & Outliers
We have removed the extreme outliers from our dataset.
we have applied a Decision Tree Classifier to see the **feature's importance**. 
1. Since Insulin has 50% of data Nan values and has low Importance, we decided to remove it.
2. Since skin thickness correlates with BMI and has low Importance, we decided to remove it.

   
### Method 2: Scaling & Modelling
#### Scaling
We have **standardized** the features using **standard scaler**.
Also, we have transformed some features using **QuantileTransformer** as some models assume that the features are **Normally Distributed**.
we have applied a Decision Tree Classifier to see the **feature's importance**. 

#### Modelling

We have experimented with a lot of classifiers:
1. AdaBoost Model
2. RandomForest Model
3. KNN Model
4. Logistic Regression
5. Ensemble Classifier of all previous models (Hard Voting)

### Method 3: Results & Evaluation
We decided to focus on Recall & AUC (Area Under Curve)

| Model               | AUC      | Recall  |
|---------------------|----------|---------|
| AdaBoost            | 0.705015 | 0.666667|
| Random Forest       | 0.713864 | 0.666667|
| KNN                 | 0.717074 | 0.823529|
| Logistic Regression | 0.718289 | 0.666667|
| Ensemble            | 0.724623 | 0.705882|

