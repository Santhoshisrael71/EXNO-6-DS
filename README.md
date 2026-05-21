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
 Include the necessary coding and corresponding screenshots
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np

x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]

sns.lineplot(x=x, y=y)
plt.title("Line Graph Using Seaborn")
plt.show()
```
<img width="534" height="433" alt="download" src="https://github.com/user-attachments/assets/e6e49032-f32d-4e97-9a2f-fde32061dae5" />

```
x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]

sns.lineplot(x=x, y=y1, label='Line 1')
sns.lineplot(x=x, y=y2, label='Line 2')
sns.lineplot(x=x, y=y3, label='Line 3')

plt.title("Multi-Line Plot")
plt.xlabel("X Label")
plt.ylabel("Y Label")
plt.show()

```
<img width="554" height="453" alt="download" src="https://github.com/user-attachments/assets/c3644077-420b-4966-91b8-3fd44d0e659c" />
```
tips = sns.load_dataset("tips")

sns.barplot(x='day', y='total_bill', hue='sex', data=tips)

plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
plt.show()
```
<img width="563" height="453" alt="download" src="https://github.com/user-attachments/assets/8585e571-29f5-4c8b-bc5f-00c6e38abc8a" />

```
sns.scatterplot(
    x='total_bill',
    y='tip',
    hue='sex',
    data=tips
)

plt.xlabel("Total Bill")
plt.ylabel("Tip Amount")
plt.title("Scatter Plot")
plt.show()
```
<img width="563" height="453" alt="download" src="https://github.com/user-attachments/assets/c36e14ce-b5dc-4132-9a9b-086f37e6b30a" />

```
np.random.seed(0)

num_var = np.random.randn(1000)

sns.histplot(num_var, kde=True)

plt.title("Histogram")
plt.show()

```
<img width="572" height="433" alt="download" src="https://github.com/user-attachments/assets/b80be070-f064-4662-95f2-36ec85a89fb0" />
```
np.random.seed(0)

marks = np.random.normal(
    loc=70,
    scale=10,
    size=100
)

sns.histplot(
    marks,
    bins=10,
    kde=True
)

plt.xlabel("Marks")
plt.ylabel("Density")
plt.title("Histogram of Student Marks")
plt.show()

```
<img width="576" height="453" alt="download" src="https://github.com/user-attachments/assets/ba8d9c77-f9f7-487e-8a18-8451d6027a0f" />

```
sns.boxplot(
    x='day',
    y='total_bill',
    hue='sex',
    data=tips
)

plt.title("Box Plot")
plt.show()

```
<img width="563" height="453" alt="download" src="https://github.com/user-attachments/assets/deec0c45-6c69-4e59-8b1f-e404c01a8c2b" />

```
sns.violinplot(
    x='day',
    y='total_bill',
    hue='smoker',
    data=tips
)

plt.xlabel("Day")
plt.ylabel("Total Bill")
plt.title("Violin Plot")
plt.show()

```
<img width="563" height="453" alt="download" src="https://github.com/user-attachments/assets/ec43f583-c5d8-467c-a21c-56898a34a0c0" />

```
sns.violinplot(
    x='day',
    y='tip',
    data=tips
)

plt.title("Violin Plot - Tips")
plt.show()
```
<img width="563" height="453" alt="download" src="https://github.com/user-attachments/assets/444174a5-4055-44c7-8799-c692bae20261" />

```
sns.kdeplot(
    data=tips,
    x='total_bill',
    hue='time',
    fill=True
)

plt.title("KDE Plot")
plt.show()

```
<img width="585" height="453" alt="download" src="https://github.com/user-attachments/assets/ff836416-b423-49c9-93c2-18fe444bbae1" />

```
sns.kdeplot(
    data=tips,
    x='total_bill',
    y='tip'
)

plt.title("Bivariate KDE Plot")
plt.show()
```
<img width="563" height="453" alt="download" src="https://github.com/user-attachments/assets/a16d2ed6-9f30-4f9e-af32-baee239ba100" />

```
data = np.random.randint(
    low=1,
    high=100,
    size=(10, 10)
)

sns.heatmap(data, annot=True)

plt.title("Heat Map")
plt.show()

```
<img width="511" height="433" alt="download" src="https://github.com/user-attachments/assets/144c870e-2bfa-4f48-9028-45d1d155f302" />

```
numeric_cols = tips.select_dtypes(
    include=np.number
).columns

corr = tips[numeric_cols].corr()

sns.heatmap(
    corr,
    annot=True,
    cmap='viridis'
)

plt.title("Heat Map for Tips Dataset")
plt.show()
```

<img width="515" height="433" alt="download" src="https://github.com/user-attachments/assets/5907fabb-2988-4d37-a8f4-9ce8560acf68" />

# Result:
 Include your result here
