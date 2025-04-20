# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
M.Suryakumar
 <pre>
import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("tips")
print(df.head())
sns.lineplot(x="total_bill", y="tip", data=df, hue="sex", linestyle="solid", legend="auto", palette="Set1")
import seaborn as sns
import matplotlib.pyplot as plt
tips = sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")["total_bill"].mean()
avg_tip = tips.groupby("day")["tip"].mean()
plt.figure(figsize=(8,6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill")
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
avg_total_bill_time = tips.groupby('time', observed=False)['total_bill'].mean()
avg_tip_time = tips.groupby('time', observed=False)['tip'].mean()
plt.figure(figsize=(6, 5))
p1 = plt.bar(avg_total_bill_time.index, avg_total_bill_time, label="Total Bill", width=0.4)
p2 = plt.bar(avg_tip_time.index, avg_tip_time, bottom=avg_total_bill_time, label="Tip", width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
plt.show()
import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("tips")
sns.barplot(x="day", y="total_bill", hue="sex", data=df, palette="Set3")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
plt.show()
import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("tips")
sns.scatterplot(x="total_bill", y="tip", hue="sex", data=df, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
plt.show()
sns.histplot(data=df, x="total_bill", hue="smoker", kde=True, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Smoker Status")
plt.show()
import seaborn as sns
import pandas as pd
df = sns.load_dataset('tips')
sns.boxplot(x='day', y='total_bill', hue='sex', data=df, palette='Set2')
plt.xlabel('Day')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Sex')
plt.show()
sns.boxplot(x="day", y="total_bill", hue="smoker",
data=df, linewidth=2, width=0.6,
fliersize=7, flierprops={"marker": "o", "markerfacecolor": "grey"},
boxprops={"facecolor": "red", "edgecolor": "black"},
whiskerprops={"color": "darkblue", "linestyle": "--", "linewidth": 2},
capprops={"color": "darkblue", "linestyle": "-", "linewidth": 2},
palette='Set1')
plt.xlabel('Day')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Smoker Status')
plt.show()
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette='Set1', inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
plt.show()
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset('tips')
sns.violinplot(x='day', y='tip', data=tip, palette="Set2")
plt.xlabel('Day')
plt.ylabel('Tip Amount')
plt.title('Tip Amount Distribution by Day')
plt.show()
import seaborn as sns
sns.set(style='whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"], palette="Set1")
plt.xlabel('Total Bill')
plt.title('Distribution of Total Bill')
plt.show()

import seaborn as sns
sns.set(style="whitegrid")
tips = sns.load_dataset("tips")
sns.violinplot(x="tip", y="day", data=tips, palette="rainbow")
plt.xlabel("Tip Amount")
plt.ylabel("Day of the Week")
plt.title("Tip Amount Distribution by Day")
plt.show()
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='layer', linewidth=3, palette='Set2', alpha=0.6)
plt.xlabel('Total Bill')
plt.ylabel('Density')
plt.title('Distribution of Total Bill by Time of Day')
plt.show()
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set3', alpha=0.8)
plt.xlabel('Total Bill')
plt.ylabel('Density')
plt.title('Stacked Distribution of Total Bill by Time of Day')
plt.show()
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='fill', linewidth=3, palette='Set1', alpha=0.8)
plt.xlabel('Total Bill')
plt.ylabel('Density')
plt.title('Filled Distribution of Total Bill by Time of Day')
plt.show()
import seaborn as sns
tip = sns.load_dataset('tips')
num = tip.select_dtypes(include=['float64', 'int64']).columns
corr = tip[num].corr()
sns.heatmap(corr, annot=True, cmap="YlGnBu")
plt.title('Correlation Heatmap of Numerical Features')
plt.show()
sns.heatmap(corr, cmap="YlGnBu")
plt.title('Correlation Heatmap of Numerical Features')
plt.show()

 </pre>
# Result:
 Thus the data visualization techniques of seaborn has been implemented.
