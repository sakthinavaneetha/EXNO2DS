# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
       
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df


![image](https://github.com/user-attachments/assets/1672caf0-6143-41ef-9735-f8d8f48c0355)

df.info()

![image](https://github.com/user-attachments/assets/299de69f-b58d-4c4d-a9e8-df32e534d790)

df.shape

![image](https://github.com/user-attachments/assets/65371432-9d75-4c87-a196-94065de00b34)

import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.set_index("PassengerId",inplace=True)
print(df.set_index)

![image](https://github.com/user-attachments/assets/7becd46c-15c4-4f9b-a75e-5e938f37ffd9)


df.describe()

![image](https://github.com/user-attachments/assets/3a65160e-6870-43d2-a669-829ec69aaa6e)

df.nunique()

![image](https://github.com/user-attachments/assets/69c95c5e-0ba9-46c1-9ec5-c16d1e83bfc6)

df["Survived"].value_counts()

![image](https://github.com/user-attachments/assets/3553d053-1a1b-4352-a949-2bd7cc80e15a)

per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per

![image](https://github.com/user-attachments/assets/d01cb488-c9c9-495f-8715-a6759120181f)

sns.countplot(data=df,x="Survived")

![image](https://github.com/user-attachments/assets/0b1f5070-e07a-4086-91bd-50610630480e)

df

![image](https://github.com/user-attachments/assets/2ff7937e-c207-4eac-aa01-cf694da8242d)

df.Pclass.unique()

![image](https://github.com/user-attachments/assets/f4b2e382-08bb-4af8-b024-11ff9fcf50cb)

import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
sns.catplot(x="Sex",col='Survived',kind="count",data=df,height=5, aspect=.7)

![image](https://github.com/user-attachments/assets/9ff2a3e5-8c14-4c2f-937a-43a67d845b9c)

sns.catplot(x='Survived',hue='Sex',data=df,kind='count')

![image](https://github.com/user-attachments/assets/8531623f-3c00-4e3b-a86d-fd776d806c62)

df.boxplot(column='Age',by="Survived")

![image](https://github.com/user-attachments/assets/876aa106-fd55-45bb-ac2d-cff2a6942144)

sns.scatterplot(x=df['Age'],y=df["Fare"])

import matplotlib.pyplot as plt
fig,ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=df)

![image](https://github.com/user-attachments/assets/19d1e1ac-ddca-437b-9d5e-6fbecaa429fe)

sns.catplot(data=df,col='Survived',x='Sex',hue='Pclass',kind='count')

![image](https://github.com/user-attachments/assets/681772a6-98c7-4f1a-8467-43b91b08eae6)

import seaborn as sns
corr=df.corr()
sns.heatmap(corr,annot=True)

![image](https://github.com/user-attachments/assets/8461faea-d6f0-4bdf-847a-12a4b0144485)

sns.pairplot(df)

![image](https://github.com/user-attachments/assets/a7f29db8-2184-4319-a568-84a9279b4506)


# RESULT
 Code are sucessfully executed.
