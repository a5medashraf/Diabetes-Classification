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
3. Feature Importance

#### 1. Removing NaNs:
We have found that the Dataset has zero NaN values. However, after some investigations, we have found that the NaNs values were replaced with 0.
so, we dropped all zero values from all the features.

### 2. Balancing the Outcome Class
We have found that the outcome class is not balanced. so, we decided to use oversampling using smote as our data is small to remove from it.
as shown below: 
<img src="<img src="URL_OF_THE_IMAGE" width="150" height="150">

### Method 2: Modelling
