# Ex.No: 1B                     CONVERSION OF NON STATIONARY TO STATIONARY DATA
# Date: 11/03/2025

### AIM:
To perform regular differncing,seasonal adjustment and log transformatio on international airline passenger data
### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the data preprocessing if needed and apply regular differncing,seasonal adjustment,log transformation.
4. Plot the data according to need, before and after regular differncing,seasonal adjustment,log transformation.
5. Display the overall results.
### PROGRAM:

```
DEVELOPED  BY: KUKKADAPU CHARAN TEJ
REGISTER NUMBER:212224040167
```
```py
from matplotlib import pyplot as plt
import pandas as pd

df=pd.read_csv("/content/AirPassengers.csv")
# df=pd.read_csv("/content/test.csv",parse_dates=["date"],index_col="date"

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


### OUTPUT:
![image](https://github.com/user-attachments/assets/43793485-6758-47bf-bc53-32ca05007e78)





### RESULT:
Thus we have created the python code for the conversion of non stationary to stationary data on international airline passenger
data.
### Interpretation:
This is a Non stationary time series with Multiplicative Seasonality and Additive Trend
