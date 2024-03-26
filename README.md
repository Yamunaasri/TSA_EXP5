# Ex.No: 05  IMPLEMENTATION OF TIME SERIES ANALYSIS AND DECOMPOSITION
### Date: 23.03.2024
### AIM:
To Illustrates how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.

### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the decomposition process for the required data.
4. Plot the data according to need, either seasonal_decomposition or trend plot.
5. Display the overall results.

### PROGRAM:
```
NAME : YAMUNAASRI T S
REG NO : 212222240117
```
```
!pip install pandas

import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose

# Load dataset (replace with your data)
data = pd.read_csv('/content/AirPassengers.csv')

# Convert 'date' column to datetime format and set as index
data['Month'] = pd.to_datetime(data['Month'])
data.set_index('Month', inplace=True)

# Specify the period for decomposition
period = 12  # Change this to the appropriate period for your data

# Perform decomposition
result = seasonal_decompose(data, model='multiplicative', period=period)

# Plot the decomposition
result.plot()
plt.show()
```

### OUTPUT:
FIRST FIVE ROWS:
![image](https://github.com/Yamunaasri/TSA_EXP5/assets/115707860/9938f6d6-cdf7-4f66-a66e-77d8f5201da0)

PLOTTING THE DATA:
![image](https://github.com/Yamunaasri/TSA_EXP5/assets/115707860/ca47cafb-fdb4-4182-9cb2-8e5104eda1d5)

SEASONAL PLOT REPRESENTATION :

![image](https://github.com/Yamunaasri/TSA_EXP5/assets/115707860/503e0919-13b3-419f-925c-aea5d8b8d80d)

TREND PLOT REPRESENTATION :

![image](https://github.com/Yamunaasri/TSA_EXP5/assets/115707860/dca2b831-f79e-4568-b5ac-4f272f558d97)

OVERAL REPRESENTATION:



### RESULT:
Thus we have created the python code for the time series analysis and decomposition.
