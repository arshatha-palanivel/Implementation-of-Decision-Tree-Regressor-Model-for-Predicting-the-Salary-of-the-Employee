# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload the csv file and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree inport DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output.

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Arshatha P 
RegisterNumber: 212222230012
```
```
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
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:
Initial Dataset:

![001](https://github.com/arshatha-palanivel/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118682484/8223a3a9-9b4e-4d9a-a746-3ea2f4b266fd)


Data Info:

![002](https://github.com/arshatha-palanivel/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118682484/1b58353a-4dc8-401c-87b2-9d9be46e9de6)


Optimization of null values:

![003](https://github.com/arshatha-palanivel/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118682484/cc706ab0-efb8-49b7-b297-f1847faaf3cb)


Converting string literals to numerical values using label encoder:

![004](https://github.com/arshatha-palanivel/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118682484/1eb2aca3-221b-41bf-a186-7e1b0a08e38e)


Mean Squared Error:

![005](https://github.com/arshatha-palanivel/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118682484/0043e930-045b-4786-bd87-ccf92c1f8b2a)


R2 (Variance):

![006](https://github.com/arshatha-palanivel/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118682484/3613efcd-59a3-49b5-ac2f-9c8a5a43de39)


Perdicition:

![007](https://github.com/arshatha-palanivel/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118682484/0556f394-64c1-4fb3-8a76-e9f180144e28)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
