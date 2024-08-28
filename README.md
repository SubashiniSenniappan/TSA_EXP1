
# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 
## Developed by:Subashini S
## Register No:212222240106


# AIM:
To Develop a python program to Plot a time series data based on weather classification.
# ALGORITHM:
```
Import required libraries (pandas, matplotlib).
Load the dataset using pandas.read_csv().
Plot the time series using plt.plot() with the relevant columns.
Customize with labels and title.
Display the plot using plt.show().
```
# PROGRAM:

```
import pandas as pd
import matplotlib.pyplot as plt

# Load the data
df = pd.read_csv('/content/weather_classification_data.csv')

# Display the first few rows and columns to understand the structure
print(df.head())
print(df.columns)

# Adjust these column names based on the actual data
# If there's no 'Date' column, skip date parsing
# Example column names (replace with actual ones):
# temperature_column = 'Temperature'
# humidity_column = 'Humidity'

# Plot the time series data (replace with actual column names)
plt.figure(figsize=(10, 6))
plt.plot(df['Temperature'], label='Temperature')  # Replace 'Temperature' with actual column name
plt.title('Temperature Time Series')
plt.xlabel('Time')
plt.ylabel('Temperature')
plt.legend()
plt.grid(True)
plt.show()

```



# OUTPUT:

![Screenshot 2024-08-28 094118](https://github.com/user-attachments/assets/455dc1bd-b75e-4156-aa1f-805f77a57bae)

![Screenshot 2024-08-28 094130](https://github.com/user-attachments/assets/1aa73940-c59e-44de-863c-b459b9f9edbd)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
