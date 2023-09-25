# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.
2. Upload the dataset and check for any null or duplicated values using .isnull() and .duplicated() function respectively.
3. Import LabelEncoder and encode the dataset.
4. Import LogisticRegression from sklearn and apply the model on the dataset.
5. Predict the values of array.
6. Calculate the accuracy, confusion and classification report by importing the required modules from sklearn.
7. Apply new unknown values.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: s.monicka
RegisterNumber: 212221220033 

#import modules
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

#reading the file
dataset=pd.read_csv('Placement_Data_Full_Class.csv')
dataset
dataset.head(20)
dataset.tail(20)

#droping tha serial no salary col
dataset = dataset.drop('sl_no',axis=1)
#dataset = dataset.drop('salary',axis=1)
dataset

dataset = dataset.drop('gender',axis=1)
dataset = dataset.drop('ssc_b',axis=1)
dataset = dataset.drop('hsc_b',axis=1)
dataset

dataset.shape
(215, 10)

dataset.info()

#catgorising for further labeling
dataset["degree_t"]=dataset["degree_t"].astype('category')
dataset["specialisation"]=dataset["specialisation"].astype('category')
dataset["status"]=dataset["status"].astype('category')
dataset["hsc_s"]=dataset["hsc_s"].astype('category')
dataset["workex"]=dataset["workex"].astype('category')
dataset.dtypes

dataset.info()

dataset["degree_t"]=dataset["degree_t"].cat.codes
dataset["specialisation"]=dataset["specialisation"].cat.codes
dataset["status"]=dataset["status"].cat.codes
dataset["hsc_s"]=dataset["hsc_s"].cat.codes
dataset["workex"]=dataset["workex"].cat.codes
dataset
dataset.info()
dataset

x = dataset.iloc[:,:-1].values
y = dataset.iloc[:,-1].values
y

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x, y,test_size=0.2)
dataset.head()
x_train.shape
x_test.shape
y_train.shape
y_test.shape

from sklearn.linear_model import LogisticRegression
clf= LogisticRegression()
clf.fit(x_train,y_train)
clf.score(x_test,y_test)

clf.predict([[0, 87, 0, 95, 0, 2, 78, 2, 0]])

*/
```

## Output:
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/3209cd1e-c24c-4b2e-bc3c-c9181e094fbb)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/19696eb8-77a0-4151-b608-55a8717fb971)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/568b991b-dba3-4ac2-80ea-c091a37833b9)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/9fb132d4-758f-4976-a1f8-afa3a22dc2d8)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/fe3933ad-6d9c-4e6b-a77f-9d7a50045315)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/26af2dff-a721-4762-af24-5447dcaae858)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/a20f6228-a829-4274-809e-9b87d7abc7f2)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/96930417-cea1-456d-b761-436a3545a73b)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/f7072544-173b-498f-a714-fba354b4bd81)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/dd0d361a-bf9a-4481-b479-397f49cc0756)
![image](https://github.com/Monicka19/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/143497806/1f643853-9216-4b1a-823f-7108ee85725a)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
