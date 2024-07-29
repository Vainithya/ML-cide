import pandas as pd 
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
df = pd.read_csv('SaYoPillow.csv')
df.shape
df.head()
df.head()
df.describe().T
df.isnull().sum()

df["stress_level"].value_counts()
df["stress_level"].value_counts()
df.groupby('stress_level').mean()
corr = df.corr()
corr.style.background_gradient(cmap='coolwarm')
def comparisonplot(data, column1, column2, target):
    figure = px.scatter(data_frame = data, x=column1,
                    y=column2, color= target)
    # figure.show()

  cols = []
figure=[]
for col1 in df.columns:
    cols.append(col1)
    for col2 in df.columns:
        if col2 not in cols:
            fig =comparisonplot(df,col1, col2, 'stress_level')
            figure.append(fig)
            # Save the figures
            figure[0]
    
