# EXN0-9 Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the packages.

2. Analyse the data. 

3. Use modelselection and Countvectorizer to preditct the values. 

4. Find the accuracy and display the result. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Ashwin Kumar S
RegisterNumber:  212222240013
*/
```
```
import pandas as pd
data=pd.read_csv("spam.csv", encoding='Windows-1252')
data

data.shape

x=data['v2'].values
y=data['v1'].values
x.shape

y.shape

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2, random_state=0)
x_train

x_train.shape
```
```
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc=accuracy_score(y_test,y_pred)
acc

con=confusion_matrix(y_test,y_pred)
print(con)

cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:
### data
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/4a522776-209c-4329-932c-be8f8102c5ba)

### data.shape()
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/f8f741f4-3206-4526-92fd-c890f6ecb1e5)

### x.shape()
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/2d7d8faa-ef77-405b-aedb-3009855bfeb9)

### y.shape()  
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/d3439f11-7e22-4ade-b5c6-917b3352cb8d)

### x_train
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/67edd510-0d60-49f7-bde7-cd13ba895357)

### x_train.shape()
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/e9f7eb9a-89b8-4d67-b58c-29e8bd8668e0)

### y_pred
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/d98bdfde-aa7b-46a0-814a-020100201f28)

### acc (accuracy)
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/da3dd64d-b341-4b5b-824e-dd621396b816)

### con (confusion matrix)
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/43ae6fb1-8477-4118-abea-e8b2891123aa)

### cl (classification report)
![image](https://github.com/amal-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/148410730/c1a9e002-dc90-4f21-bb0d-daf799640c92)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
