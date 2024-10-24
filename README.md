# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Start the program.

Step 2: Import the required packages.

Step 3: Import the dataset to operate on.

Step 4: Split the dataset.

Step 5: Predict the required output.

Step 6: End the program.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Hariharan A
RegisterNumber: 212223110013
*/

import pandas as pd
data=pd.read_csv("spam.csv",encoding = 'Windows-1252')
from sklearn.model_selection import train_test_split

data

data.shape

data.info()

x=data['v2'].values

y=data['v1'].values

x.shape

y.shape

x_train,x_test,y_train,y_test = train_test_split(x,y,test_size= 0.35,random_state=0)

x_train

x_train.shape

from sklearn.feature_extraction.text import CountVectorizer cv = CountVectorizer()

x_train= cv.fit_transform(x_train)
x_test= cv.transform(x_test)

from sklearn.svm import SVC

svc=SVC(0

svc.fit(x_train,y_train)

y_pred=svc.predict(x_test)

y_pred

from sklearn.metrics import accuracy_score,confusion_matrix, classification_report

acc=accuracy_score(y_test,y_pred)

acc

con=confusion_matrix(y_test,y_pred)

print(con)

cl=classification_report(y_test,y_pred)

print(cl)
```

## Output:

### data.head()
![image](https://github.com/user-attachments/assets/e592833a-8138-4501-ba30-917e6f13ef96)

### data.info()
![image](https://github.com/user-attachments/assets/e145e6f1-ffaa-4cd3-8856-6a3e68450a03)

### accuracy()

![image](https://github.com/user-attachments/assets/57977a63-e2c6-4d90-8559-796fd2024936)


### matrix

![image](https://github.com/user-attachments/assets/9941a424-0a05-4c49-979d-dea7284416eb)


### classification

![image](https://github.com/user-attachments/assets/dd007309-cc8a-474b-bdc8-10340e91134f)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
