# Airline_Passenger_Satisfaction
### Introduction
This analysis was done for an airline that is interested in knowing how its customers rated their services. The airline did a survey on its service. As a data Analyst, I am tasked with cleaning,analyzing, visualizing and sharing of the survey result in order to help improve their services.
#### Business Task
How did the customers rate our services? How can we improve? Use the survey result to analyze and present findings.
#### Data Background
It is a public data gotten from kaggle https://www.kaggle.com/datasets/mysarahmadbhat/airline-passenger-satisfaction
I chose Python for cleaning and exploratory analysis then visualized with python. To import,clean,analyze and visualize the dataset, I installed and imported pandas,numpy,matplotlib.pyplot and seaborn.
`# import libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
print('imported')`
`# import the file
df = pd.read_csv("C:/Users/user/Desktop/airline_passenger_satisfaction.csv")
print('done')`
We familiarize with the dataset
`# See first 5 rows of the dataset 
df.head()`
`# See last 5 rows of dataset
df.tail()`
`# See the columns
df.columns`
`# Check for duplicates
duplicate = df.duplicated()
duplicate.value_counts()`
`# Look at the structure of the dataset
df.info()`
`# check for null values
df.isnull().sum()`
`# Remove null values
df = df.dropna()
print(df.isnull().sum())`
`# Get summary statistics of the dataset
df.describe()`
`# plot to show age distribution of customers
fig= plt.figure(figsize = (30,18))
sns.countplot(x=df['Age'])
plt.title('Age Distribution',fontsize=20,weight='bold')
plt.xlabel('Age',fontsize = 16,weight='bold')
plt.ylabel('Count',fontsize = 18,weight='bold')`
`# plot to show gender distribution
sns.countplot(df['Gender'])
plt.title('Gender Distribution',weight='bold')`
`# plot showing customer satisfaction
sns.countplot(df['Satisfaction'])
plt.title('Customer Satisfaction',weight='bold')`
`# plot showing customer type
sns.countplot(df['Customer Type'])
plt.title('Customer Type',weight='bold')`
`# plot showing type of travel
sns.countplot(df['Type of Travel'])
plt.title('Type of Travel',weight='bold')`
`# plot showing class of customers
sns.countplot(df['Class'])
plt.title('Class of Customers',weight='bold')`
`# Save as csv
df.to_csv('air_passenger_satisfaction.csv')`
I saved as a csv and imported into Microsoft PowerBi for visualization.
