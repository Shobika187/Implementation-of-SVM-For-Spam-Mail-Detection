# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. Import the required packages.
2.Import the dataset to operate on.
3.Split the dataset.
4.Predict the required output.
5.End the program.

```
## Program:
```

Program to implement the SVM For Spam Mail Detection..
Developed by: Shobika P
RegisterNumber:  212221230096
import chardet
file='/content/spam.csv'
with open(file,'rb') as rawdata:
  result=chardet.detect(rawdata.read(100000))
import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='Windows-1252')
data.isnull().sum()
data.info()
x=data['v1'].values
y=data['v2'].values
from sklearn.model_selection import train_test_split
x_tarin,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC svc=SVC() svc.fit(x_train,y_train)

y_pred=svc.predict(x_test) y_pred

from sklearn import metrics accuracy=metrics.accuracy_score(y_test,y_pred) accuracy
```

## Output:
![image](https://user-images.githubusercontent.com/94508142/204433597-16c87434-3e00-49ea-b3b3-a6aac54f7600.png)

![image](https://user-images.githubusercontent.com/94508142/204433628-5cdc6189-585e-463a-acec-7f63f6993d96.png)


![image](https://user-images.githubusercontent.com/94508142/204433661-bc4090db-fa45-422f-8cc1-a89c9bd3fc68.png)




![image](https://user-images.githubusercontent.com/94508142/204433694-93ef0145-f095-4730-9383-c707c956f238.png)


![image](https://user-images.githubusercontent.com/94508142/204434295-f00319c7-be3e-4c75-b75a-0d138c19aa75.png)



![image](https://user-images.githubusercontent.com/94508142/204433899-3299eb21-d400-4646-b5f5-b146bfe61348.png)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
