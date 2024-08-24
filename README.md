### DEVELOPED BY: S JAIGANESH
### REGISTER NO: 212222240037
### DATE: 

# Ex.No: 01 PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import pandas for data manipulation and matplotlib.pyplot for plotting.
2. Read the CSV file using pandas.read_csv().
3. Convert the 'date' column to a datetime format using pd.to_datetime().
4. Group the data by 'date' and calculate the average 'money' spent per day using groupby() and mean().
5. Set up the plot using plt.figure() and specify the figure size.
6. Use plt.plot() to create a line plot with markers for the average money spent per day.
7. Use plt.tight_layout() to adjust the layout and plt.show() to display the plot.


# PROGRAM:

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the data
data = pd.read_csv('coffee_sales.csv')

# Convert 'date' to datetime format
data['date'] = pd.to_datetime(data['date'])

# Group by date and calculate the average money spent per day
daily_average = data.groupby('date')['money'].mean().reset_index()

# Plotting
plt.figure(figsize=(14, 7))
plt.plot(daily_average['date'], daily_average['money'], marker='o', linestyle='-', color='b')
plt.title('Average Money Spent per Day')
plt.xlabel('Date')
plt.ylabel('Average Money')
plt.xticks(rotation=45)
plt.grid()
plt.tight_layout()
plt.show()

```
<br>
<br>
<br>
<br>

# OUTPUT:
![image](https://github.com/user-attachments/assets/462ed2e9-af2e-4c25-ad04-f470fbe0dd8c)




# RESULT:
Thus we have created the Python code for plotting the time series of given data.
