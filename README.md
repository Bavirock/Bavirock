import pandas as pd
import matplotlib.pyplot as plt

# Load your dfset
data = pd.read_csv('cleaned_dataset.csv')

# Specify the column for which you want to create a histogram
column_name = 'Global_average'

# Convert the 'value' column to a numeric df type (int or float) if needed
data[column_name] = pd.to_numeric(data[column_name], errors='coerce')

# Create a histogram
plt.hist(df[column_name].dropna(), bins=200, edgecolor='k')  # Adjust the number of bins as needed
plt.xlabel(column_name)
plt.ylabel('Frequency')
plt.title(f'Histogram of {column_name}')

# Set a custom x-axis range
plt.xlim(0, 3000)  # Adjust the range as needed

plt.show()
