# practice-EDA
import pandas as pd
import numpy as np
import os
import seaborn as sns
os.chdir("Documents")
df = pd.read_csv("marketing_campaign.csv")
df.head()
df.drop("AcceptedCmp3", axis=1)
df.isnull()
df.isull().count()
sns.heatmap(df.isnull())
sns.lineplot(x = "Education" ,y ="Income", data = df)
sns.violinplot(x = "Education" ,y ="Income", data = df)
sns.scatterplot(x = "Education" ,y ="Income", data = df)
sns.barplot(x = "Education" ,y ="Income", data = df, hue = "Complain")
