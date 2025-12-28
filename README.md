# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given data.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

# Step 1: Include the necessary libraries 
    import pandas as pd 
    import numpy as np 
    import matplotlib.pyplot as plt 
    import seaborn as sns 
    data=pd.read_csv("titanic_dataset.csv")
    df=pd.DataFrame(data)
    df.head(

<img width="1354" height="225" alt="image" src="https://github.com/user-attachments/assets/51ea7bc0-9af6-467d-928c-c83b0288c973" />

    # Visualize missing data 
    plt.figure(figsize=(10,6)) 
    sns.heatmap(df.isnull(), cbar=False, cmap='viridis', yticklabels=False) 
    plt.title("Missing Values Heatmap") 
    plt.show()

<img width="1368" height="735" alt="image" src="https://github.com/user-attachments/assets/b1a3ab4d-8350-49c8-85fd-6c9f87d1523b" />

    plt.figure(figsize=(8,5)) 
    sns.countplot(x='Sex', data=df, palette='pastel') 
    plt.title("Passenger Count by Gender") 
    plt.show()

<img width="1191" height="603" alt="image" src="https://github.com/user-attachments/assets/490460a2-2ece-4b8a-a4cf-bea3521c6cf4" />

    #  Countplot - Survival vs Class 
    plt.figure(figsize=(8,5))  
    sns.countplot(x='Survived', hue='Pclass', data=df, palette='Set2') 
    plt.title("Survival Count by Passenger Class") 
    plt.xlabel("Survived (0 = No, 1 = Yes)") 
    plt.ylabel("Count") 
    plt.legend(title="Class") 
    plt.show()

<img width="1195" height="604" alt="image" src="https://github.com/user-attachments/assets/790c0728-6c82-4457-bcb5-1635001f63b6" />

    #  Step 5: Histogram - Continuous Data Distribution 
    plt.figure(figsize=(8,5)) 
      sns.histplot(data=df, x='Age', kde=True, bins=30, color='skyblue') 
    plt.title("Age Distribution of Passengers") 
    plt.xlabel("Age") 
    plt.ylabel("Frequency") 
    plt.show()

<img width="1040" height="599" alt="image" src="https://github.com/user-attachments/assets/fbab9b02-8eb0-4d53-afc6-8af12d4963e1" />

    #  Step 6: Boxplot - Outlier Detection and Comparison 
    plt.figure(figsize=(8,5)) 
    sns.boxplot(x='Pclass', y='Age', data=df, palette='muted') 
    plt.title("Age Distribution across Passenger Classes") 
    plt.xlabel("Passenger Class") 
    plt.ylabel("Age") 
    plt.show() 

<img width="1270" height="607" alt="image" src="https://github.com/user-attachments/assets/d25ce992-63e2-47d8-8668-ff905e43f0d4" />

    #  Step 7: Pairplot - Multiple Feature Interactions 
    sns.pairplot(df[['Age', 'Fare', 'Pclass', 'Survived']], hue='Survived', palette='coolwarm') 
    plt.suptitle("Pairwise Relationships", y=1.02) 
    plt.show() 

<img width="987" height="916" alt="image" src="https://github.com/user-attachments/assets/9f289a10-d351-4794-8cfe-7ab3f0302d50" />

    # Step 8: Correlation Heatmap - Numeric Feature Correlation 
    plt.figure(figsize=(10,7)) 
    corr_matrix = df.corr() 
    sns.heatmap(corr_matrix, annot=True, cmap='Blues', linewidths=0.5) 
    plt.title("Correlation Matrix Heatmap") 
    plt.show()

<img width="1247" height="753" alt="image" src="https://github.com/user-attachments/assets/c1b32dea-29ac-4de4-a781-137400aa9c7e" />

# Result:

Thus the python program to Perform Data Visualization using matplot python library for the given data is written executed successfully.
