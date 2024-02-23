# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output:
```
import pandas as pd 
df=pd.read_csv("/content/Data_set.csv") 
print(df)
df.head(5)
df.info()
df.isnull().sum() 
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0]) 
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0]) 
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0]) 
df.head() 
df['rating']=df['rating'].fillna(df['rating'].mean()) 
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean()) 
df.head() 
df['watchers']=df['watchers'].fillna(df['watchers'].median()) 
df.head() 
df.info() 
df.isnull().sum()
```
![image](https://github.com/Reebak04/exno1/assets/118364993/d5e58e4f-80a4-4122-aba9-4f0a5cecfff3)
![image](https://github.com/Reebak04/exno1/assets/118364993/6c03e6c8-0b61-40c3-9a2c-c9aa32bf8757)

# Result

