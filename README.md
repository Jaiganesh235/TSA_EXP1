### DEVELOPED BY: S JAIGANESH
### REGISTER NO: 212222240037
### DATE: 

# Ex.No: 01 PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity/temperature).
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
data = pd.read_csv('/mnt/data/MLTempDataset.csv')

# Convert 'Datetime' to datetime format
data['Datetime'] = pd.to_datetime(data['Datetime'])

# Group by date and calculate the average 'DAYTON_MW' spent per day
daily_average = data.groupby(data['Datetime'].dt.date)['DAYTON_MW'].mean().reset_index()

# Plotting
plt.figure(figsize=(14, 7))
plt.plot(daily_average['Datetime'], daily_average['DAYTON_MW'], marker='o', linestyle='-', color='b')
plt.title('Average DAYTON_MW per Day')
plt.xlabel('Date')
plt.ylabel('Average DAYTON_MW')
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
![image](https://github.com/user-attachments/assets/fba2693e-1ee9-4f2b-bcd8-5754724ebed3)





# RESULT:
Thus, the Python code for plotting the time series of room temperature data had been executed successfully.
