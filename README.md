<H3>NAME : KANISHKAR M</H3>
<H3>REGISTER NO. 212222240044</H3>
<H3>EX. NO.1</H3>
<H3>DATE : 22/02/2024</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

### To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
### Hardware – PCs
### Anaconda – Python 3.7 Installation / Google Colab /Jupyter Notebook

## RELATED THEORETICAL CONCEPT:

### Kaggle:

Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

### Data preprocessing:


Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

### Need of Data Preprocessing :

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
### STEP 1:

#### Importing the libraries<BR>

### STEP 2:

#### Importing the dataset<BR>

### STEP 3:

#### Taking care of missing data<BR>

### STEP 4:

#### Encoding categorical data<BR>

### STEP 5:

#### Normalizing the data<BR>


### STEP 6:

Splitting the data into test and train<BR>

##  PROGRAM:

### Import Libraries
```py

from google.colab import files
import pandas as pd
import seaborn as sns
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
from scipy import stats
import numpy as np

```
### Read the dataset 

```py
df=pd.read_csv("Churn_Modelling.csv")

### Checking Data
py
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

### Data checking

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/76ab9146-5798-4317-93dd-9d830c73d6b2)


### Missing Data 

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/bb94ef90-f086-4ea4-816f-d21f00faab05)


### Duplicates identification

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/618361a3-778c-4214-bdc8-9fcffb27a729)


### Vakues of 'Y'

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/524182d8-7407-486b-85e0-df480c95db4a)


### Outliers

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/7f197886-1023-44e0-bbca-5d3e24a5c8b3)


### Checking datasets after dropping string values data from dataset

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/b02e4f08-d463-43f4-8d31-fdaa702c9759)


### Normalize the dataset

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/366dd7cd-310a-473f-a5dd-3e0876241bfe)


### Split the dataset

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/720a6939-69ae-47ba-9134-db483d9315f4)


### Training and testing model

![image](https://github.com/KANISHKAR2607/Ex-1-NN/assets/118886772/17964c03-0066-42ff-892a-4e0ead3ddcb9)




## RESULT:

### Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.
