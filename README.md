# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
# OUPUT
# DATA
![image](https://github.com/swethasurendar/Ex-01-Data-Cleaning/assets/133625914/85db3322-8cfc-4cab-89df-64806e87c3f6)
# NON NULL BEFORE
# df.info
![image](https://github.com/swethasurendar/Ex-01-Data-Cleaning/assets/133625914/32ac27a2-b2c6-4176-86c6-754f91c71422)
# Mode
![image](https://github.com/swethasurendar/Ex-01-Data-Cleaning/assets/133625914/1a82bd7a-f1a3-4246-ab04-8f11d155606b)
# Median
![image](https://github.com/swethasurendar/Ex-01-Data-Cleaning/assets/133625914/94d4d3d3-7e4c-433e-8564-e7a5d36229c0)
# NON NULL AFTER
# df.info()
![image](https://github.com/swethasurendar/Ex-01-Data-Cleaning/assets/133625914/4e092e0d-2f5b-401f-a011-954a8c086372)
# df.isnull().sum()
![image](https://github.com/swethasurendar/Ex-01-Data-Cleaning/assets/133625914/5b84f1ff-a260-4f16-bcad-0a8da0a0f82b)
# Result
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
