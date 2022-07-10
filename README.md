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

[Output of Data Columns](https://github.com/dennyny/SalesAnalysis/blob/main/Images/columns2.PNG)




