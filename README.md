<H3>NAME : Shalini V</H3>
<H3>REGISTER NO. 212222240096</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
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
#### importing libraries
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```

#### Reading the dataset
```
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df
```

#### Dropping the unwanted Columns
```
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df
```
#### Checking for null values
```
df.isnull().sum()
```
#### Checking for duplicate values
```
df.duplicated()
```
#### Describing the dataset
```
df.describe()
```
#### Scaling the dataset
```
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1
```
#### Allocating X and Y attributes
```
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y
```
#### Splitting the data into training and testing dataset
```
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```

## OUTPUT:
#### DATASET:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/518cc28a-6474-41b5-ba40-73d3aaef0ad3)


#### DROPPING THE UNWANTED DATASET:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/567df826-95f1-41b4-8173-4be4aa268b4d)


#### CHECKING NULL VALUES:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/eb2761c7-3fba-446f-988b-e6b59792ce36)


#### CHECKING FOR DUPLICATION:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/00f213b9-746e-4451-9aee-7558f65fb30e)


#### DESCRIBING THE DATASET:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/bc0faabb-0dd3-4ddd-ae82-9b2ba1e5c49b)

#### SCALING THE DATASET:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/f4c223ed-b49c-4991-b48f-4f6909f2eada)

#### X FEATURES:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/4b3e9f7d-55e4-44a5-8bb9-ed125d432489)



#### Y FEATURES:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/bc39d80f-f62a-40de-ba07-b62f072f214d)



#### SPLITTING THE TRAINING AND TESTING DATASET:

![image](https://github.com/shalini-venkatesan/Ex-1-NN/assets/118720291/e6b3d5fe-a448-476f-8fd8-d81b35188612)





## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


