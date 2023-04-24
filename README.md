# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file

# CODE
```
import pandas as pd
df=pd.read_csv('/content/Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
df1 = pd.read_csv("/content/data.csv")
df1.head()
df1['Ord_1'].unique()
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
df2 = pd.read_csv("/content/titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```

# OUPUT
![image](https://user-images.githubusercontent.com/121300272/233911084-7f3daf8e-6ec9-49f4-995b-68ea9ca9089f.png)

![image](https://user-images.githubusercontent.com/121300272/233911230-77ea18a0-9ee7-45de-917a-10141cbf86eb.png)
![image](https://user-images.githubusercontent.com/121300272/233911300-332dc3a2-549b-4691-b2a9-2befc30068fe.png)
![image](https://user-images.githubusercontent.com/121300272/233911371-84edec00-c8e5-4791-b490-05ae3f7e8960.png)
![image](https://user-images.githubusercontent.com/121300272/233911510-bd0b1258-e56b-4879-8573-c53d37b1de10.png)
![image](https://user-images.githubusercontent.com/121300272/233911573-3ea23b15-0041-4680-9a65-aacd03eecb39.png)
![image](https://user-images.githubusercontent.com/121300272/233911630-78a2208c-6117-46f5-8fa9-a1d0be11440a.png)
![image](https://user-images.githubusercontent.com/121300272/233911703-7d7508f1-0f33-4886-9542-24e87e41060c.png)
![image](https://user-images.githubusercontent.com/121300272/233911844-a4f212bd-5284-470f-b0f9-068c677120e4.png)
![image](https://user-images.githubusercontent.com/121300272/233911922-27bb7e1b-93c1-4eb8-95d7-e245d20efcb4.png)
![image](https://user-images.githubusercontent.com/121300272/233912006-6b884a70-d6d9-4fbf-bafc-38b92bcad3cb.png)

## RESULT
The Feature Generation process was performed and saved the data to a file. 
