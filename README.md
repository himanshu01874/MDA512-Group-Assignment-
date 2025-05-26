# MDA512-Group-Assignment-
This analysis inspired from the Unit data science as a part of the group to do analysis which will be important real time problem.
# Task 1: Summarize Employee Data
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv("C:\\Users\\shelly\\Downloads\\archive\\watson_healthcare_modified.csv")
df.info()
df.describe(include='all')
df.groupby(['Department', 'Gender', 'JobRole'])['Attrition'].value_counts().unstack().fillna(0)
