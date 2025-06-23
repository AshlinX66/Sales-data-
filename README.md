# Sales-data-
This project focuses on cleaning, standardizing, and analyzing sales data. Key tasks include converting datatypes, standardizing text values (like gender and country), removing duplicates, and dropping unnecessary columns. The goal is to prepare clean and structured data for accurate analysis and reporting.
# codes used
import numpy as np ,import pandas as pd 
data=pd.read_csv("train.csv")
data = data.drop(['Row ID', 'Ship Date', 'Ship Mode','Segment','Postal Code'], axis=1)
data.dropna(inplace=True)
data.isnull().sum()
data.info()
data=data.drop_duplicates().sum()
