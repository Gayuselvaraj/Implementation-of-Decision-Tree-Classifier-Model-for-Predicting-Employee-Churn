# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.import pandas module and import the required data set.

2.Find the null values and count them.

3.Count number of left values.

4.From sklearn import LabelEncoder to convert string values to numerical values.

5.From sklearn.model_selection import train_test_split.

6.Assign the train dataset and test dataset.

7.From sklearn.tree import DecisionTreeClassifier.

8.Use criteria as entropy.

9.From sklearn import metrics.

10.Find the accuracy of our model and predict the require values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: GAYATHRI S
RegisterNumber:  212224230073
import pandas as pd

data = pd.read_csv("Employee.csv")

data.head()

data.info()

data.isnull().sum()

data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()

data["salary"] = le.fit_transform(data["salary"])
data.head()

x=data[["satisfaction_level","last_evaluation","number_project", "average_montly_hours",
"time_spend_company", "Work_accident","promotion_last_5years","salary"]]
x.head()

y = data["left"]

from sklearn.model_selection import train_test_split
x_train, x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn. tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt. predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)

accuracy
dt.predict([[0.5,0.8,9,260, 6,0,1,2]])
*/
```

## Output:
data.head:

<img width="1363" height="227" alt="318775359-d5cb75c8-1a61-40b1-9f55-9dd6e2f28fe9" src="https://github.com/user-attachments/assets/e920366a-d3ba-48e4-9296-eae273bb9c19" />

dataset info:

<img width="480" height="367" alt="318775482-909d5c90-e8fc-4e80-a696-180be9736872" src="https://github.com/user-attachments/assets/5dcf67c7-36bc-4e5b-b3eb-9e479631f7e7" />

null dataset:

<img width="268" height="246" alt="318775624-955a342a-5f5c-4b9e-b092-08c418ca2f04" src="https://github.com/user-attachments/assets/3dcc3590-2db7-493f-82a1-6990a3958208" />

x.head:

<img width="1197" height="222" alt="318776032-f10c925a-3ac2-44ef-a6ec-1e15da68f1d8" src="https://github.com/user-attachments/assets/16f93f17-1363-4ebf-ac0a-c4b2212a6ff9" />

accuracy:

<img width="1140" height="27" alt="318776125-723a87ad-58a9-4512-90d1-31cddd146a48" src="https://github.com/user-attachments/assets/a9954381-1157-433d-8f11-f0719ea3a0b4" />

data prediction:

<img width="1367" height="101" alt="318776215-c51ce862-b453-4847-abcc-cfb56674ed3d" src="https://github.com/user-attachments/assets/1d96fc39-4c24-40e6-afb9-d095cec9c833" />

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
