# Developed by:Subashini S
# Register No:212222240106
# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
---
1.Import Packages: Start by importing pandas and matplotlib.pyplot.
2.Load the Dataset: Use pandas to read the CSV file into a DataFrame.
3.Inspect Data: Optionally, print the first few rows of the DataFrame to understand its structure.
4.Plot the Data: Use matplotlib to plot the desired columns (e.g., Temperature over Time).
5.Display the Plot: Add labels, titles, and then display the graph using plt.show().
---
# PROGRAM:

---
import pandas as pd
import matplotlib.pyplot as plt

#Step 1: Load the data from the CSV file
file_path = '/content/weather_classification_data.csv'  # Ensure the file path is correct
df = pd.read_csv(file_path)

#Step 2: Inspect the first few rows of the dataframe to understand its structure
print(df.head())

#Step 3: Aggregate data by 'Season' and calculate the mean temperature
seasonal_data = df.groupby('Season')['Temperature'].mean().reset_index()

#Step 4: Aggregate data by 'Location' and calculate the mean temperature
location_data = df.groupby('Location')['Temperature'].mean().reset_index()

#Step 5: Plot the aggregated data by 'Season'
plt.figure(figsize=(12, 6))
plt.subplot(1, 2, 1)  # Create the first subplot
plt.plot(seasonal_data['Season'], seasonal_data['Temperature'], marker='o', linestyle='-', color='b')
plt.title('Average Temperature by Season')
plt.xlabel('Season')
plt.ylabel('Average Temperature (°C)')
plt.grid(True)
plt.xticks(rotation=45)

#Step 6: Plot the aggregated data by 'Location'
plt.subplot(1, 2, 2)  # Create the second subplot
plt.plot(location_data['Location'], location_data['Temperature'], marker='o', linestyle='-', color='g')
plt.title('Average Temperature by Location')
plt.xlabel('Location')
plt.ylabel('Average Temperature (°C)')
plt.grid(True)
plt.xticks(rotation=45)

#Step 7: Show the combined plot
plt.tight_layout()  # Adjust the layout to prevent overlap
plt.show()

---



# OUTPUT:


![Screenshot 2024-08-23 224525](https://github.com/user-attachments/assets/fb82045e-c915-497f-b594-126181a9a6e6)



![Screenshot 2024-08-23 224615](https://github.com/user-attachments/assets/57a4831b-6b1c-4055-a697-cf9121020693)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
