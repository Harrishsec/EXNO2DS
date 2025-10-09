# EXNO2DS
# NAME: Harrish P
# Register No: 212224230088
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
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df
```
OUTPUT:

<img width="1385" height="661" alt="image" src="https://github.com/user-attachments/assets/9074e6bd-7430-48c3-9672-ef38b044559c" />

```
df.info()
```
OUTPUT:

<img width="461" height="429" alt="image" src="https://github.com/user-attachments/assets/ba6a7800-3704-4856-8cb9-eb867976416d" />

```
df.describe()
```
OUTPUT:

<img width="937" height="377" alt="image" src="https://github.com/user-attachments/assets/4f87f304-e6a0-4306-814a-0ad8097a9cbb" />

```
df.dtypes
```
OUTPUT:

<img width="313" height="583" alt="image" src="https://github.com/user-attachments/assets/6e8a9c4c-b5a5-4006-b555-33f6181729e4" />

```
df.shape
```
OUTPUT:

<img width="161" height="98" alt="image" src="https://github.com/user-attachments/assets/37dc5d3a-9f47-4838-96d0-6a025ecbd65e" />

```
df.value_counts()
```

OUTPUT:

<img width="1411" height="588" alt="image" src="https://github.com/user-attachments/assets/63b2379a-0f6e-4a0e-a673-06ba7f9f352d" />

```
df['Age'].value_counts()
```

OUTPUT:

<img width="263" height="591" alt="image" src="https://github.com/user-attachments/assets/d8a68e17-36e5-4b11-9155-71f670bde705" />

```
df.set_index("PassengerId", inplace=True)
df
```

OUTPUT:

<img width="1385" height="587" alt="image" src="https://github.com/user-attachments/assets/ee4b155f-2796-4452-8534-dc7747c09b20" />

```
df.nunique()
```

OUTPUT:

<img width="243" height="543" alt="image" src="https://github.com/user-attachments/assets/a8031061-24bd-4619-8940-96a11c224a19" />

```
sns.countplot(data=df,x='Survived')
```
OUTPUT:

<img width="730" height="570" alt="image" src="https://github.com/user-attachments/assets/65157c4a-f123-4ea3-ab7f-35526505e284" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```

OUTPUT:

<img width="1376" height="603" alt="image" src="https://github.com/user-attachments/assets/5989a7cc-9462-4811-a780-244ebc46fce8" />

```
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=0.7)
```
OUTPUT:

<img width="858" height="623" alt="image" src="https://github.com/user-attachments/assets/415637cd-b11a-4874-bf7d-0a42702f0ab8" />

```
df.boxplot(column="Age",by="Survived")
```
OUTPUT:

<img width="713" height="604" alt="image" src="https://github.com/user-attachments/assets/a6584ec4-66a9-4572-a905-083758668778" />

```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```
OUTPUT:

<img width="709" height="570" alt="image" src="https://github.com/user-attachments/assets/36dcfa75-8c2d-4f25-a4f0-4450c7cd95a8" />

```
fig, axl=plt.subplots(figsize=(8,5))
plt=sns.boxplot(ax=axl,x='Pclass',y='Age',hue='Gender',data=df)
```

OUTPUT:

<img width="844" height="585" alt="image" src="https://github.com/user-attachments/assets/7788bec5-7b64-4ded-83c7-37a75544fc02" />

```
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
```

OUTPUT:

<img width="740" height="532" alt="image" src="https://github.com/user-attachments/assets/a2557896-81d7-400a-9688-32666476fae1" />

```
import seaborn as sns
sns.catplot(x='Pclass',y="Age",hue="Gender",col="Survived",kind="box",data=df)
```

OUTPUT:

<img width="1297" height="653" alt="image" src="https://github.com/user-attachments/assets/3eaac700-4fa3-4cb2-9a3f-890a3946cc74" />

```
sns.catplot(data=df,col="Survived",x="Gender",hue='Pclass',kind="count")
```

OUTPUT:

<img width="1263" height="631" alt="image" src="https://github.com/user-attachments/assets/18fe827b-8497-40fe-ab86-52bb2e2b5550" />

```
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)

```

OUTPUT:

<img width="1356" height="640" alt="image" src="https://github.com/user-attachments/assets/52661cd8-64b0-4e0c-b814-ae568e8e16e2" />

```
corr=df.select_dtypes(include=np.number).corr()
sns.heatmap(corr,annot=True)
```

OUTPUT:

<img width="852" height="671" alt="image" src="https://github.com/user-attachments/assets/378a3b1d-fba5-4057-b233-82a1dff47ce0" />




# RESULT
       Thus performed Exploratory Data Analysis on the given data set.

