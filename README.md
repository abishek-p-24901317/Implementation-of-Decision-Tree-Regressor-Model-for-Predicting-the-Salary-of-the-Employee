# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load and preprocess data:Read the CSV file and encode the "Position" column using LabelEncoder.
2. Prepare features and labels: Select "Position" and "Level" as input features (X), and "Salary" as the target variable (y).
3. Split the dataset:Divide the data into training and testing sets using an 80/20 split.
4. Train the model:Use DecisionTreeRegressor to fit the training data and make predictions.
5. Evaluate and predict:Calculate Mean Squared Error and R² score, and predict salary for input [5, 6].

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Abishek P
RegisterNumber:  212224240002

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
print("Mse: ")
mse

r2=metrics.r2_score(y_test,y_pred)
print('r2:')
r2

dt.predict([[5,6]])

*/
```

## Output:
## Head Values:
![image](https://github.com/user-attachments/assets/34093ba8-b028-459e-b6a3-20ed1d4bf6da)
## Data info:
![image](https://github.com/user-attachments/assets/8fb6920e-47a2-40e8-99da-74af1b33b9ac)
## Null values:
![image](https://github.com/user-attachments/assets/df9284da-c4cd-44cd-8b3c-12480f15522d)
## Transforming Position into int:
![image](https://github.com/user-attachments/assets/9f2dad63-bb30-4b0b-9b98-780cd6a84cc9)
## Position and level:
![image](https://github.com/user-attachments/assets/9ceb2196-3490-4611-a5fb-e8fdd99ad0b8)
## Mse Value:
![image](https://github.com/user-attachments/assets/880e2249-eb6e-4416-8e20-fcb6deb6ea0a)
## R2 Value:
![image](https://github.com/user-attachments/assets/895be29a-f20a-4cee-aba0-b198fb8a3873)
## Predicted Value:
![image](https://github.com/user-attachments/assets/fee6cb9d-fd2f-40ba-a9e1-a5cec5d94d68)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
