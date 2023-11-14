# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries .
2. Read the data frame using pandas.
3. Get the information regarding the null values present in the dataframe.
4. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5.Determine training and test data set.
6.Apply decision tree regression on to the dataframe.
7.Get the values of Mean square error, r2 and data prediction.

## Program:
```python
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Vikash A R
RegisterNumber:  212222040179
*/
data=pd.read_csv("Salary Data.csv")
data.head()
data.tail()
data.info()
data["Gender"]=data["Gender"].astype('category')
data["Education Level"]=data["Education Level"].astype('category')
data["Job Title"]=data["Job Title"].astype('category')
data.info()
data["Gender"]=data["Gender"].cat.codes
data["Education Level"]=data["Education Level"].cat.codes
data["Job Title"]=data["Job Title"].cat.codes
data.info()
data.head()
x=data[['Age','Gender','Education Level','Job Title','Years of Experience']]
x
x.shape
y=data[['Salary']]
y.shape
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)
from sklearn.tree import DecisionTreeRegressor
dtr=DecisionTreeRegressor()
dtr.fit(x_train,y_train)
y_pred=dtr.predict(x_test)
print(y_pred)
x_train.shape
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dtr.predict([[44,0,2,130,20]])
```

## Output:

## READ CSV HEAD FILE:

![280455431-3ffb504d-a7a1-4b42-b749-0f3258bcf656](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/463e8712-c7e7-4066-a371-bdbefffb6a22)

## TAIL:

![280455469-79f6f7b2-e790-4c46-9b7b-f571c25ede2f](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/c86dc76b-1284-4c03-8a5f-ff38f3d44c62)


## DATASET INFO:

![280455480-271d7609-b28e-4831-8171-6c39b47a5d20](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/8f579edf-002f-482c-a6e6-de8f0ffc97b0)


![280455490-f73952ba-feef-4e59-b81b-641792c23306](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/94aa0f15-a1ad-4208-a673-7ae844a1d6cf)


![280455495-d3f6e59b-b67d-414c-a0cd-9ce4e5299dc4](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/256e0044-b16c-43d5-8d2e-4b5b3e3cbc76)


![280455503-fbab1c96-a847-49e5-9506-4f00c69fa18e](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/e0f03dfc-20b3-4a44-8a28-cabf439bbea7)

## X-DATA:

![280455514-87c15651-41cf-479b-ae52-02199bca48d2](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/5e91d2cb-3778-42db-9cc4-cf1464224ba1)

## DATA SHAPE:

![280455538-b13e6c8c-9715-4102-be85-56028ac0ad1b](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/278abd51-96f9-4f08-ade0-680707a2a732)

## Y_PRED:

![280455553-674e7856-c6c6-4897-8ad2-d4ac3827c18f](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/38e69801-efaf-465c-b899-4178a7731c87)

## MEAN SQUARED VALUE:

![280455571-ff568d12-9386-458b-8798-27dc71ba0ceb](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/2f177a23-a2b9-43d2-9e96-755c3347f5c3)

## R2 VALUE:

![280455583-f41bcce2-bce0-460f-970a-d4401fb4b4bf](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/a8f2bdf5-aacd-4586-985f-3d4d053f0fe5)

## DTR PREDICT:

![280455589-557c20fa-1ba0-43c1-a323-41cbed452f87](https://github.com/VIKASHAR/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405655/235cbc12-49c4-4e30-9091-fc9a5067ecbb)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
