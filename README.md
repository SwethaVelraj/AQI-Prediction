#install necessary libraries
pip install jupyter
pip install notebook
pip install seaborn
pip install --upgrade pip
import seaborn as sns
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from warnings import filterwarnings
filterwarnings('ignore')
df= pd.read_csv('air quality data.csv')
df.head() #top 5 rows
df.shape
df.info #information
df.duplicated().sum() #to know the duplicate values
df.isnull().sum()
df.dropna(subset=['AQI'],inplace= True) #dropping the rows where aqi has missing values
df.isnull().sum().sort_values(ascending=False) #checking missing values
df.shape #changed
print(df.dtypes)
df.describe().T #T--> transpose
null_values_percentage=(df.isnull().sum()/df.isnull().count()*100).sort_values(ascending=False)
null_values_percentage #checking percentage of null values

finding correlations between pollutants This identifies which pollutants impact AQI the most
checking aqi distribution by plotting histogram

plt.figure(figsize=(10,5))  # Creates a figure with a width of 10 and height of 5.  
sns.histplot(df["AQI"], bins=30, kde=True, color='blue')  # Plots a histogram of AQI with 30 bins, adds a KDE curve, and sets color to blue.  
plt.title("Air Quality Index (AQI) Distribution")  # Adds a title to the plot.  
plt.xlabel("AQI")  # Labels the X-axis as "AQI".  
plt.ylabel("Frequency")  # Labels the Y-axis as "Frequency".  
plt.show()  # Displays the plot. 
