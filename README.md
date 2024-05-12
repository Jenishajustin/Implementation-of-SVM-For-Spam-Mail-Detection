# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: 
RegisterNumber:  
*/
```
```python
import chardet
file='spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
resultimport pandas as pd
data=pd.read_csv("spam.csv",encoding="'Windows-1252")
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
#Countvectorizer is a method to convert text to numerical data. The text is transformed to a sparse matrix
cv = CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("Accuracy=",accuracy)

```

## Output:
### result
![Screenshot 2024-05-12 084520](https://github.com/Jenishajustin/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119405070/a6a9d3ff-92a3-4924-9628-28fc03cb0e92)

### dataset
![Screenshot 2024-05-12 084604](https://github.com/Jenishajustin/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119405070/7a4d3478-20f9-4703-b4c4-a9822e58cc72)

### data.info()
![Screenshot 2024-05-12 084628](https://github.com/Jenishajustin/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119405070/20a11c45-17e2-4ea0-839f-25876ed1f5a3)

### NULL values
![Screenshot 2024-05-12 084706](https://github.com/Jenishajustin/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119405070/e9fd0ffe-4102-4bfb-b871-1bb66e1ecd26)

### y_pred
![Screenshot 2024-05-12 084751](https://github.com/Jenishajustin/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119405070/5a4f1c02-d8bc-455f-858c-6800dab8ee3f)

### Accuracy
![Screenshot 2024-05-12 084840](https://github.com/Jenishajustin/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119405070/ccdb9148-89e7-4d7f-b0d8-1c45beb0d64a)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
