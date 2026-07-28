 Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 28/7/2026
### GOWTHAM C
### 21224240046


# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```
from matplotlib import pyplot as plt
import pandas as pd

df=pd.read_csv("/content/test.csv")

df.head()

df['Month']=pd.to_datetime(df['Month'])

df.dtypes

df.set_index('Month',inplace=True)

df_resampled = df['#Passengers'].resample('D').interpolate()
df_resampled.plot(kind='line',label='Total Sales', color='black')
plt.title('Time Series Plot of Number of passengers ecah day')
plt.xlabel('Day')
plt.ylabel('Number of passengers')
plt.legend()
plt.grid(True)
plt.show()


```






# OUTPUT:

![image](https://github.com/user-attachments/assets/6f4bdc9d-ad16-45a7-a5c1-d333a2dcc25e)





# RESULT:
Thus we have created the python code for plotting the time series of given data.
# Interpretation:
This is a Non stationary time series with Multiplicative Seasonality and Additive Trend
