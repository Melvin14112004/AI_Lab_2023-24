# Ex.No: 13 Wine Quality Prediction
### DATE: 24.10.24                                                                         
### REGISTER NUMBER : 212222040098
### AIM: 
To analyze and predict wine quality based on chemical properties using data preprocessing, exploratory data analysis (EDA), and machine learning techniques. 
### Algorithm:
1. Start the program
2. Load dataset, check for structure, and summarize key statistics.
3. Handle missing values by filling them with column means.
4. Visualize distributions of key features and wine quality.
5. Use a correlation heatmap to examine relationships between features.
6.  Prepare data by splitting into training and test sets.
7.   Train a classification model (e.g., Random Forest) to predict wine quality.
8.   Evaluate model accuracy and interpret the impact of chemical properties on quality.
### Program:
```py
import numpy as np
import pandas as pd 
import os
for dirname, _, filenames in os.walk('/kaggle/input'):
    for filename in filenames:
        print(os.path.join(dirname, filename)) 
df = pd.read_csv("/kaggle/input/wine-quality/winequalityN.csv")
df.head()
df.describe()
df.info()

# Import additional libraries for visualization
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline

# Check for missing values in each column
df.isnull().sum()

# View value counts for 'fixed acidity'
df["fixed acidity"].value_counts()

# Fill missing values in 'fixed acidity' column with its mean
mean = df["fixed acidity"].mean()
df["fixed acidity"].fillna(mean, inplace=True)
df["fixed acidity"].isnull().sum()

# Fill missing values in 'volatile acidity' column with its mean
mean2 = df["volatile acidity"].mean()
df["volatile acidity"].fillna(mean, inplace=True)
df["volatile acidity"].isnull().sum()

# View value counts for 'citric acid'
df["citric acid"].value_counts()

# Fill missing values in 'citric acid' column with its mean
mean3 = df["citric acid"].mean()
df["citric acid"].fillna(mean, inplace=True)
df["citric acid"].isnull().sum()

# View value counts for 'residual sugar'
df["residual sugar"].value_counts()

# Fill missing values in 'residual sugar' column with its mean
mean4 = df["residual sugar"].mean()
df["residual sugar"].fillna(mean, inplace=True)
df["residual sugar"].isnull().sum()

# Fill missing values in 'chlorides' column with its mean
mean5 = df["chlorides"].mean()
df["chlorides"].fillna(mean, inplace=True)
df["chlorides"].isnull().sum()

# Fill missing values in 'pH' column with its mean
mean6 = df["pH"].mean()
df["pH"].fillna(mean, inplace=True)
df["pH"].isnull().sum()

# Fill missing values in 'sulphates' column with its mean
mean7 = df["sulphates"].mean()
df["sulphates"].fillna(mean, inplace=True)
df["sulphates"].isnull().sum()

# Check if there are any remaining missing values
df.isnull().sum()

# View value counts for 'type' column
df["type"].value_counts()

# Plot distribution of wine types
sns.countplot(x="type", data=df)
plt.show()

# Plot histogram for the 'quality' column
sns.countplot(x="quality", data=df)
plt.show()

# Show correlation heatmap
plt.figure(figsize=(10, 8))
sns.heatmap(df.corr(), annot=True, cmap="coolwarm")
plt.show()

# Distribution plots for alcohol, chlorides, and density
sns.histplot(df["alcohol"], kde=True)
plt.show()

sns.histplot(df["chlorides"], kde=True)
plt.show()

sns.histplot(df["density"], kde=True)
plt.show()

# Scatter plot between alcohol and quality
sns.scatterplot(x="alcohol", y="quality", data=df)
plt.show()

# Scatter plot between volatile acidity and quality
sns.scatterplot(x="volatile acidity", y="quality", data=df)
plt.show()

```
### Output:
![alt text](<Screenshot 2024-08-12 224950.png>)
### Result:
The model successfully predicted wine quality with reasonable accuracy, identifying key features like alcohol content and acidity as influential factors.
