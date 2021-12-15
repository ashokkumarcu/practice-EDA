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
sns.barplot(x = "Education" ,y ="Income", data = df, hue = "Kidhome")
sns.barplot(x = "Education" ,y ="Income", data = df, hue = "Teenhome")
df.drop("AcceptedCmp5", axis=1)
df.info()
df1 = df.drop(["AcceptedCmp1","AcceptedCmp2","AcceptedCmp3","AcceptedCmp4","AcceptedCmp5"], axis=1)
df1.info()
df1.describe()
cor_df = df1.corr()
sns.heatmap(cor_df)
