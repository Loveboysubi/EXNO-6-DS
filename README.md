# EX.NO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[2,3,7,1,5]
sns.lineplot(x=x,y=y)
```
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/ae872d38-6071-4bd2-b557-1e665575218c)
```
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by day')
plt.legend()
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/0ccbaa1e-a50e-4148-bc64-ed4e410b2f97)
```
sns.barplot(x='day',y='total_bill',hue='sex',data=df,palette='Set2')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by day and gender')
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/80c36388-8357-4a58-babc-47b2bddb0867)
```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter plot of total bill vd Tip amount')
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/a1964412-6062-43d1-9c26-6ffc6e97988e)
```
import seaborn as sns
import numpy as np
import pandas as pd
num_var=pd.read_csv("/content/titanic_dataset.csv")
num_var
sns.histplot(data=num_var,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/e665a3f7-e169-4e80-bfcc-f8fc1f8719d3)
```
np.random.seed(1)
num=np.random.randn(100)
num=pd.Series(num,name="Numerical Variable")
num
sns.histplot(data=num,kde=True)
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/6acf5030-bf4e-4a27-99df-e8bc051cb055)
```
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
sns.histplot(data=marks,bins=10,kde=True,stat="count",cumulative=False,multiple="stack",element="bars",palette="Set1",color="black",shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students marks')
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/7083bfd5-90d0-4781-bdf3-99f5e173d2e8)
```
import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/25682f13-a20a-4f4c-8dcb-0a7042c0b970)
```
sns.boxplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, boxprops={'facecolor':'lightblue','edgecolor':'black'},whiskerprops={'color':'blue','linestyle':'--','linewidth':1.5},capprops={'color':'red','linestyle':'--','linewidth':1.5})
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/c2217c5a-5f0a-467e-8221-2677731346ff)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
sns.violinplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, palette='Set1',color='blue',inner="quartile")
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Violin plot of Total bill by day and smoker status')
```
![image](https://github.com/22008837/EXNO-6-DS/assets/120194155/292d2569-76f9-49b6-99e4-61b9c41bf68f)


## Result:
Thus, all the data visualization techniques of seaborn has been implemented.
