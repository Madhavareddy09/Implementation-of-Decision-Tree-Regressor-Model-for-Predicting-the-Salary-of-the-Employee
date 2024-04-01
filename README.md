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
```python
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by : K MADHAVA REDDY
RegisterNumber : 212223240064 

import pandas as pd
data = pd.read_csv(r'Salary.csv')
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```

## Output:

### data.head()
![image](https://github.com/Madhavareddy09/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145742470/0e73ac61-d819-4042-acd6-09c85e78f031)

### data.info()
![image](https://github.com/Madhavareddy09/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145742470/4de6264e-adf2-4be7-88a1-3275cdcf2a62)

### isnull and sum()
![image](https://github.com/Madhavareddy09/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145742470/05f3f92d-3325-4cbe-9bbd-3f6cbd88b33c)

### position head()
![image](https://github.com/Madhavareddy09/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145742470/cb7ae265-a9cd-4c36-9210-c688a89b6834)

### Value of MSE
![image](https://github.com/Madhavareddy09/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145742470/233c7e6f-6bc2-4c97-bab1-0ed1bd29c270)
### value of r2
![image](https://github.com/Madhavareddy09/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145742470/ebb5da48-d4ce-4713-b15b-a063afb22405)

### data.prediction()
![image](https://github.com/Madhavareddy09/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145742470/683e3616-444d-4146-b118-9983fe1bc805)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
