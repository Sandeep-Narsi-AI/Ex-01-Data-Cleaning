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

# CODE :
~~~
import pandas as pd
df = pd.read_csv('Data_set.csv')
df.head()
df.tail()
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['show_name'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()

~~~
# OUTPUT :
## HEAD
![GitHubLogo](ex1head.png)
## TAIL
![GitHubLogo](ex1tail.png)
## INFO
![GitHubLogo](ex1info.png)
## ISNULL
![GitHubLogo](ex1isnull.png)
## MODE
![GitHubLogo](ex1mode.png)
## MEAN
![GitHubLogo](ex1mean.png)
## MEDIAN
![GitHubLogo](ex1median.png)
## FINAL
![GitHubLogo](ex1final1.png)
![GitHubLogo](ex1final2.png)

# RESULT :
 The data is cleaned and it is filled with MEAN, MODE and MEDIAN and in the final output we can see that it has 0 null values.