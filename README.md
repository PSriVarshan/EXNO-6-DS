# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
### Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:

STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Developed By : Sri Varshan P 
Reg.no: 212222240104
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/d4963da4-a2cb-4651-9063-b0f7b48a28b9)


### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/e9df55e0-9994-48e5-8417-c05196762725)

### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/5f29e38a-fb70-4250-8871-78e72ec01d6f)


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/c31da087-66a2-4737-b761-ce7b61769f37)

### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/efcb6677-f8d2-410d-9aca-45f7f74b2e28)

### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/cff4b062-0418-4e21-a6e2-35ea77aaa40a)

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/2f332a56-13b1-4483-be35-4f3716af95fc)

### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/e7389943-e8a0-46aa-8287-febcf205f782)

### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/17cc7c89-dbba-472d-a322-99d1a3dac949)

### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/daa436f7-e2e8-4d2b-92ba-968408c176ab)

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/PSriVarshan/EXNO-6-DS/assets/114944059/51a516d5-9d5f-4a20-859d-41aa8fe75d1b)


## Result:
  
  ### Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

