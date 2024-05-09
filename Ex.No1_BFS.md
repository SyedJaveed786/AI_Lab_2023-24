### EX-No : 13 MINI PROJECT

#### DATA ANALYSIS USING MACHINE LEARNING TECHNIQUES.

### DATE: 22.04.2024
### REGISTER NUMBER: 212221220055

### AIM:

To Perform Data Analysis on the given dataset and save the data to a file.

### Equipments Required:
1.Jupyter notebook or Google colab

### ALGORITHM:

STEP 1 : Read the given Data

STEP 2 : Clean the Data Set using Data Cleaning Process

STEP 3 : Apply Feature generation and selection techniques to all the features of the data set

STEP 4 : Apply data visualization techniques to identify the patterns of the data.

### Program:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/ds_salaries.csv",encoding="ISO-8859-1")
dfdf.isnull()
df.info()
df.describe()
sns.lineplot(x="work_year",y="salary",data=df,marker='o')
plt.title("work_year vs salary")
plt.xticks(rotation = 90)
plt.show()

sns.barplot(x="work_year",y="salary",data=df)
plt.xticks(rotation = 90)
plt.show()
df.shape
df1 = df[(df.salary>= 60)]
df1.shape

plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
sns.lineplot(x="company_size",y="salary",data=df)
plt.show()
states=df.loc[:,["work_year","salary"]]
states=states.groupby(by=["work_year"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("work_year")
plt.ylabel=("salary")
plt.show()
df.groupby(['work_year']).sum().plot(kind='pie', y='salary',figsize=(6,9),pctdistance=1.7,labeldistance=1.2)
df["work_year"].corr(df["salary"])
df_corr = df.copy()
df_corr = df_corr[["work_year","salary"]]
df_corr.corr()
sns.pairplot(df_corr, kind="scatter")
plt.show()
grouped_data = df.groupby('employment_type')[['work_year', 'salary']].mean()
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
ax.bar(grouped_data.index, grouped_data['work_year'], label='work_year')
ax.bar(grouped_data.index, grouped_data['salary'], bottom=grouped_data['work_year'], label='salary')
ax.set_xlabel('employment_title')
ax.set_ylabel('Value')
ax.legend()
plt.show()
grouped_data = df.groupby(['job_title', 'company_size'])[['work_year', 'salary']].mean()
pivot_data = grouped_data.reset_index().pivot(index='job_title', columns='company_size', values=['work_year', 'salary'])
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
pivot_data.plot(kind='bar', ax=ax)
ax.set_xlabel('job_title')
ax.set_ylabel('Value')
plt.legend(title='company_size')
plt.show()
```
### Output:

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/310ac946-69d7-4806-a4b0-69a492cbc075)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/04c980a1-2698-43f0-9c92-a2f515b66c1e)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/668abbcc-b3dd-4371-88ff-f5e9b90785f2)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/73a1ec2b-7504-4f0c-a35d-56524ec212f6)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/afe48c1c-5258-457d-80ed-bee06f7c4559)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/2d9cf6a3-6812-4605-ab9e-7effb6d1888e)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/429a35ff-42af-4014-9267-0b1e79732035)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/5f3e3ebd-ffa8-456c-9215-c31018a682f4)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/2fe1f55d-3e5e-4e4b-a30e-c36427f68912)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/00564f75-bf9f-4f16-9393-8804a664c9f8)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/5753b053-7f4e-43cf-a9af-b9e071863a75)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/15949272-f516-4985-a0ce-ae0abd53bb6c)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/064f92a3-56fd-4fe3-a64b-6030d804f8b1)


![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/e1c18894-0ccf-4f2c-bd18-e92131d6e7c1)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/daf76c02-cd4c-4eaa-abec-d022decb16b9)

![image](https://github.com/Anandanaruvi/Mini-Project/assets/120443233/7000f55a-ec8d-4297-9c94-5eacfb42b795)

### Result:

Thus, Data analysis is performed on the given dataset and save the data to a file.
