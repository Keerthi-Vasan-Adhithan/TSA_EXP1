# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a Python program to Plot time series data (population/ market price of a commodity
/temperature.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.

# PROGRAM:
```py
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("/content/apple_stock.csv")
df.head()

df['Date'] = pd.to_datetime(df['Date'])
df.set_index('Date', inplace=True)

plt.figure(figsize=(14, 7))
plt.plot(df['Adj Close'], label='Adjusted Close Price')
plt.title('Apple Stock Adjusted Close Price Over Time')
plt.xlabel('Date')
plt.ylabel('Adjusted Close Price (USD)')
plt.legend()
plt.grid(True)
plt.show()

```

# DATASET:
![Screenshot 2024-08-24 092428](https://github.com/user-attachments/assets/9ff42729-fce6-4ede-a5d6-179df9ba8f14)

# OUTPUT:
![Screenshot 2024-08-24 092455](https://github.com/user-attachments/assets/cb568f40-b444-4871-98c2-c85935511bff)


# RESULT:
Thus we have created the Python code for plotting the time series of given data.
