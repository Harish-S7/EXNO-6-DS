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
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
# OUTPUT:
<img width="1216" height="202" alt="Screenshot 2025-11-05 155904" src="https://github.com/user-attachments/assets/d4f7d769-59e2-4c04-b1d7-c2c5841b669d" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
# OUTPUT:
<img width="1190" height="498" alt="Screenshot 2025-11-05 155920" src="https://github.com/user-attachments/assets/b786541b-5f44-4916-97ec-2483460c1ec2" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
# OUTPUT:
<img width="719" height="505" alt="Screenshot 2025-11-05 160952" src="https://github.com/user-attachments/assets/a405cad6-c999-41e8-b7ef-4689eaf33a3d" />


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
# OUTPUT:
<img width="1019" height="509" alt="Screenshot 2025-11-05 155938" src="https://github.com/user-attachments/assets/cdd7746a-1335-4147-be30-17a16792cec2" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
# OUTPUT:
<img width="1077" height="509" alt="Screenshot 2025-11-05 155944" src="https://github.com/user-attachments/assets/d228d9b9-71e7-4b6f-a40f-44d7ba7b71ce" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
# OUTPUT:
<img width="1017" height="500" alt="Screenshot 2025-11-05 155949" src="https://github.com/user-attachments/assets/7b2e8b1a-14a2-49de-9a1a-84f1bfb732c7" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
# OUTPUT:
<img width="1117" height="502" alt="Screenshot 2025-11-05 155956" src="https://github.com/user-attachments/assets/814962e5-c1fa-4907-9ab7-42883d4f60cd" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

# OUTPUT:
<img width="1041" height="521" alt="Screenshot 2025-11-05 160000" src="https://github.com/user-attachments/assets/5b2d120a-3992-4973-81bb-816110242955" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

# OUTPUT:
<img width="1009" height="511" alt="Screenshot 2025-11-05 160006" src="https://github.com/user-attachments/assets/9c7a5ee9-4d88-4223-93c8-a3e7e3556c43" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

# OUTPUT:
<img width="1098" height="510" alt="Screenshot 2025-11-05 160011" src="https://github.com/user-attachments/assets/5ac6e673-3d5f-442f-9804-a1e854b27c24" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

# OUTPUT:
<img width="1089" height="573" alt="Screenshot 2025-11-05 160019" src="https://github.com/user-attachments/assets/3a3a5fbd-ca1f-4b8a-9df9-d626132c9f2e" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
