<H3> Sriram R </H3>
<H3>212223230215 </H3>
<H3>EX.NO.1</H3>
<H3>22-09-2025</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
### Import Libraries
```py

import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```

### Read the dataset 

```py
df=pd.read_csv("Churn_Modelling.csv")
df
```
### Checking Data
```py
df.head()
df.tail()
df.columns
```

### Check the missing data
```py
df.isnull().sum()
```

### Check for Duplicates
```py
df.duplicated()
```

### Assigning Y
```py
y = df.iloc[:, -1].values
print(y)
```

### Check for duplicates
```py
df.duplicated()
```

### Check for outliers
```py
df.describe()
```

### Dropping string values data from dataset
```py
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
```
### Checking datasets after dropping string values data from dataset
```py
data.head()
```

### Normalize the dataset
```py
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```

### Split the dataset
```py
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```

### Training and testing model
```py
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```
## OUTPUT:
### Data
<img width="1510" height="527" alt="image" src="https://github.com/user-attachments/assets/7877461d-8508-4e89-93ed-e119222e639c" />


### Data checking

<img width="264" height="364" alt="image" src="https://github.com/user-attachments/assets/7b9f9ec3-9a76-4138-8bdf-e54548be1452" />


### Missing Data 

<img width="334" height="302" alt="image" src="https://github.com/user-attachments/assets/23ba5264-d6dd-4a10-b507-907f0d2d74a3" />


### Duplicates identification

<img width="210" height="50" alt="image" src="https://github.com/user-attachments/assets/24186df7-a32d-41bf-abc7-d359edef2b2b" />

### Values of 'X'
<img width="233" height="49" alt="image" src="https://github.com/user-attachments/assets/29882523-7970-4665-85c5-7b9f7d027b81" />


### Values of 'Y'
<img width="307" height="301" alt="image" src="https://github.com/user-attachments/assets/44d51d03-f0eb-4724-88f6-37dc45d928cc" />

### Outliers
<img width="1539" height="387" alt="image" src="https://github.com/user-attachments/assets/afe8ddda-ff44-4851-a483-4b362dc052ae" />


### Checking datasets after dropping string values data from dataset
<img width="1244" height="261" alt="image" src="https://github.com/user-attachments/assets/5ecbc3a7-940c-44c6-b3a8-eceb1c6e5d33" />


### Normalize the dataset
<img width="819" height="628" alt="image" src="https://github.com/user-attachments/assets/aad78dd2-c54a-4c5d-9395-57b47d49a582" />

### Split the dataset
<img width="599" height="208" alt="image" src="https://github.com/user-attachments/assets/0fd5c899-7b67-4751-8f2b-10fe7ad712e4" />


### Training and testing model
<img width="601" height="565" alt="image" src="https://github.com/user-attachments/assets/eef0316c-8531-4048-b32f-528af4bd76f8" />


## RESULT:

### Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.
