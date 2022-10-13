# Ex-04-Multivariate-Analysis
## AIM
To perform Multivariate EDA on the given data set.

## Explanation
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM
## STEP 1
Import the built libraries required to perform EDA and outlier removal.

## STEP 2
Read the given csv file

## STEP 3
Convert the file into a dataframe and get information of the data.

## STEP 4
Return the objects containing counts of unique values using (value_counts()).

## STEP 5
Plot the counts in the form of Histogram or Bar Graph.

## STEP 6
Use seaborn the bar graph comparison of data can be viewed.

## STEP 7
Find the pairwise correlation of all columns in the dataframe.corr()

## STEP 8
Save the final data set into the file

## CODE
/*
~~~
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/SuperStore.csv")
df.head()
df.info()
df.isnull().sum()
df['Postal Code']=df['Postal Code'].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
sns.scatterplot(df['Postal Code'],df['Sales'])
state=df.loc[:,["State","Sales"]]
state=state.groupby(by=["State"]).sum().sort_values(by="Sales")
plt.figure(figsize=(17,7))
sns.barplot(x=state.index,y="Sales",data=state)
plt.xticks(rotation = 90)
plt.xlabel=("STATES")
plt.ylabel=("SALES")
plt.show()
state=df.loc[:,["State","Postal Code"]]
state=state.groupby(by=["State"]).sum().sort_values(by="Postal Code")
plt.figure(figsize=(17,7))
sns.barplot(x=state.index,y="Postal Code",data=state)
plt.xticks(rotation = 90)
plt.xlabel=("STATES")
plt.ylabel=("POSTAL CODE")
plt.show()
state=df.loc[:,["Segment","Sales"]]
state=state.groupby(by=["Segment"]).sum().sort_values(by="Sales")
plt.figure(figsize=(17,7))
sns.barplot(x=state.index,y="Sales",data=state)
plt.xticks(rotation = 90)
plt.xlabel=("SEGMENT")
plt.ylabel=("SALES")
plt.show()
sns.barplot(df['Postal Code'], df['Ship Mode'], hue=df['Region'])
df.corr()
sns.heatmap(df.corr(),annot=True)

~~~
*/

## OUTPUT
![image](https://user-images.githubusercontent.com/103166779/192589189-104c366a-886f-45b6-ba7e-ab98d341b273.png)

![image](https://user-images.githubusercontent.com/103166779/192589501-cbb5a502-0f37-4db4-a6db-5b756a5446bd.png)

![image](https://user-images.githubusercontent.com/103166779/192589773-887f8235-4083-48d5-8800-918289eec753.png)

![image](https://user-images.githubusercontent.com/103166779/192590058-d2cc22b9-9df9-4a88-a587-2dc699ddc54e.png)

![image](https://user-images.githubusercontent.com/103166779/192590343-963b2a43-0093-47e9-a7d7-1e8ce02ab2cb.png)

![image](https://user-images.githubusercontent.com/103166779/192590704-d78b58a5-dc1c-4cdb-8d3d-6b5d7d2a0a39.png)

![image](https://user-images.githubusercontent.com/103166779/192591201-72f05f1f-41e5-4cac-89d2-97bf14c573e9.png)

![image](https://user-images.githubusercontent.com/103166779/192591615-8d5c4bce-d151-4f79-a70d-49b2d226a4f7.png)

![image](https://user-images.githubusercontent.com/103166779/192591806-92293be2-6bda-4c46-a296-3a75fe1d10bd.png)

![image](https://user-images.githubusercontent.com/103166779/192591989-fbd72d9a-2620-4f5c-a1d6-7089944b3b6a.png)

## RESULT
Thus the program to perform EDA on the given data set is successfully executed.









