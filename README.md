# SalesAnalysis

Sales analysis using Python together with Pandas, Matplotlib, Seaborn and Numpy libraries.

• The dataset contains fictitious data of a supermarket sales. The columns were 7 in number.

• A dataframe was created using Pandas library.

• Matplot was using to plot graphs and Seaborn also.

## First I Imported Libraries
`import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
import numpy as np
import datetime`

These are some of the questions that would be answered.
1. What is the overall sales trend?
2. What are the top 10 product by sales?
3. Top 10 product by Quantity
4. Plot of Payment type
5. What are the most selling products?
6. What are the top selling categories and sub category?

## Importing the dataset
`sp = 'C:/Users/Denis/Documents/PORTFOLIO/SalesAnalysis/Supermarket.csv'`

`df = pd.read_csv(sp, header=0, encoding='unicode_escape')`

## Audit of Dataset

Print Column
`print(df.columns)`

![Columns](https://github.com/dennyny/SalesAnalysis/blob/main/Images/columns2.PNG)

`print(df.shape)`

**From Output below, Data contains 234,925 rows and 8 columns**

![shape](https://github.com/dennyny/SalesAnalysis/blob/main/Images/shape3.PNG)

`print(df.info())`

![Info](https://github.com/dennyny/SalesAnalysis/blob/main/Images/info4.PNG)

**Checking for Null Values**

`print(df.isnull().sum())`

![Null Values](https://github.com/dennyny/SalesAnalysis/blob/main/Images/InNull5.PNG)

**Getting descriptive information on Dataset**

`print(df.describe())`

![Describe](https://github.com/dennyny/SalesAnalysis/blob/main/Images/describe6.PNG)

## Exploratory Data Analysis

What is the overall sales trend?

**Minimum Order Date**

`df_min_order_date = df['Order_Date'].min()`

`print(df_min_order_date)`

![MinOrder](https://github.com/dennyny/SalesAnalysis/blob/main/Images/minorderdate7.PNG)

**Maximum Order Date**

`df_max_order_date = df['Order_Date'].max()`

`print(df_max_order_date)`

![MaxOrder](https://github.com/dennyny/SalesAnalysis/blob/main/Images/maxorderdate.PNG)

**Using datetime function to extract month from the year column**

`df['Sales Month'] = pd.DatetimeIndex(df['Order_Date']).month`

`print(df.head())`

![Month](https://github.com/dennyny/SalesAnalysis/blob/main/Images/extractsalesmonth8.PNG)

**Sales/Revenue by sales month. This was done using the groupby function.**

`df['Sales Month'] = pd.DatetimeIndex(df['Order_Date']).month`

`print(df.head())`

![Salesbymonth](https://github.com/dennyny/SalesAnalysis/blob/main/Images/Cost_PricevsPriceBar_Month.PNG)


**Monthly sales sort. July had the highest sale and February had the lowest.**

`df_month_Sort = df_month.sort_values('Price',ascending=False)`

`print(df_month_Sort)`

![Salessort](https://github.com/dennyny/SalesAnalysis/blob/main/Images/monthsort.PNG)



