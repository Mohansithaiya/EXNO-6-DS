# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```python
NAME: MOHAN S
REG.NO: 212223240094
```
```PYTHON
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np

x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]

sns.lineplot(x=x,y=y)
```
![Screenshot 2025-05-06 112509](https://github.com/user-attachments/assets/be965a51-82f2-429e-be0d-be3eb09347a6)

```PYTHON
df = sns.load_dataset("tips")
df
```
![Screenshot 2025-05-06 112600](https://github.com/user-attachments/assets/a0b5fe75-04ef-4f00-a536-812c76f0694e)

```PYTHON
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![Screenshot 2025-05-06 112637](https://github.com/user-attachments/assets/a495a007-a72d-4d5d-9ae0-7561c4df4286)

```PYTHON
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]

sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![Screenshot 2025-05-06 112716](https://github.com/user-attachments/assets/4fb82870-93b0-406e-abec-ba155a83897f)

```PYTHON
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![Screenshot 2025-05-06 112754](https://github.com/user-attachments/assets/8e24485e-4d6b-4604-b686-7761d18a27fe)

```PYTHON
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![Screenshot 2025-05-06 112829](https://github.com/user-attachments/assets/ff7050ab-e039-4f6c-be4c-209d78b98732)

```PYTHON
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![Screenshot 2025-05-06 112908](https://github.com/user-attachments/assets/d7eb5ed5-5893-4ed2-bb0c-ad9fe3f2787b)

```PYTHON
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![Screenshot 2025-05-06 112944](https://github.com/user-attachments/assets/d6b3339b-e2c5-4eba-a507-022e96d2c071)

```PYTHON
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![Screenshot 2025-05-06 113020](https://github.com/user-attachments/assets/57691081-5dc9-48a4-a250-0067b3f14e80)

```PYTHON
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![Screenshot 2025-05-06 113057](https://github.com/user-attachments/assets/c60728c0-6920-4806-ae74-8f71869aeabd)

```PYTHON
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![Screenshot 2025-05-06 113146](https://github.com/user-attachments/assets/09360e8f-7b2f-40e3-a765-ed0ad66c2aff)

```PYTHON
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![Screenshot 2025-05-06 113230](https://github.com/user-attachments/assets/bcc2d0ab-4cf4-4da7-b507-abd5452a8ef2)

```PYTHON
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![Screenshot 2025-05-06 113304](https://github.com/user-attachments/assets/c5646888-785c-405b-86c6-f2d70981b649)

```PYTHON
sns.histplot(data = num_var, kde = True)
```
![Screenshot 2025-05-06 113336](https://github.com/user-attachments/assets/bef827d1-f4f7-4921-abb7-95a884d21425)

```PYTHON
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![Screenshot 2025-05-06 113412](https://github.com/user-attachments/assets/0cf08f8d-caaa-4e13-b07b-c9d159232e03)

```PYTHON
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![Screenshot 2025-05-06 113444](https://github.com/user-attachments/assets/bb2c6622-0082-4642-9718-183ad543a672)

```PYTHON
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![Screenshot 2025-05-06 113520](https://github.com/user-attachments/assets/52718fa4-5b04-41d0-a008-9413df87cade)

```PYTHON
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![Screenshot 2025-05-06 113554](https://github.com/user-attachments/assets/7e8ccec9-3799-4d68-9741-71c274fed2b3)

```PYTHON
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![Screenshot 2025-05-06 113627](https://github.com/user-attachments/assets/e2b15394-f7ea-49d1-8bee-f1695afd1585)

```PYTHON
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![Screenshot 2025-05-06 113658](https://github.com/user-attachments/assets/867330e3-c628-428a-87af-0a25c13996ed)

```PYTHON
sns.kdeplot(data=mart,x='PassengerId')
```
![Screenshot 2025-05-06 113735](https://github.com/user-attachments/assets/1c80a117-ba61-4abb-a1dd-ec64c0fb08d0)

```PYTHON
sns.kdeplot(data=mart,x='Age')
```
![Screenshot 2025-05-06 113822](https://github.com/user-attachments/assets/7387c0e8-a140-47eb-a2ef-982bcf803e57)

```PYTHON
sns.kdeplot(data=mart)
```
![Screenshot 2025-05-06 113917](https://github.com/user-attachments/assets/7c6de7e1-fd9d-4246-8892-30023c0faac2)

```PYTHON
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![Screenshot 2025-05-06 113948](https://github.com/user-attachments/assets/612c0fbe-4677-49e1-9558-aa03891fe303)

```PYTHON
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![Screenshot 2025-05-06 114129](https://github.com/user-attachments/assets/3ed284f1-ba95-49b3-bde7-5e9f51b3d5d5)

```PYTHON
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![Screenshot 2025-05-06 114214](https://github.com/user-attachments/assets/38493db8-65eb-4a80-8524-15741ed460e3)

```PYTHON
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/4ee4baba-745a-48cc-ae46-08827e7b0ba3)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
