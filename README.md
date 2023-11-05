# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the libraries and read the data frame using pandas.
2.Calculate the null values present in the dataset and apply label encoder.
3.Determine test and training data set and apply decison tree regression in dataset.
4.calculate Mean square error,data prediction and r2. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Smriti .B
RegisterNumber:  212221040156
*/
```
```
import pandas as pd 
data=pd.read_csv("/content/Salary.csv")

data.head()
data.info()

data.isnull().sum()
from sklearn.preprocessing import LabelEncoder 
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"]) 
data.head()
x=data[["Position", "Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2, random_state=2)
from sklearn.tree import DecisionTreeRegressor 
dt=DecisionTreeRegressor() 
dt.fit(x_train,y_train) 
y_pred=dt.predict(x_test)
from sklearn import metrics 
mse=metrics.mean_squared_error(y_test, y_pred) 
mse
r2=metrics.r2_score (y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:
## data.head()
![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/5eb98d21-592d-4593-ac39-11f5767babac)
## data.info()
![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/1333d688-a67f-4e43-bbb3-1df9ac9c7346)
## isnull().sum()
![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/7b6da2e2-8abd-456e-a93c-2b5d62ea3556)
## data.head() for salary
![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/f8fab7f2-eb7a-4b2a-af60-2f4242a7e61d)

![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/05340ae8-cc09-4b47-8a50-482148f72edb)
## mse value
![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/09bf7655-aedc-499a-a89d-eda8eb0c4779)
## r2 value
![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/307b91e4-a87c-4061-92bd-6ef9ae3d1844)
## prediction
![image](https://github.com/smriti1910/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/133334803/61d99b77-a7bb-4252-9175-faf4efda00d5)





## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
