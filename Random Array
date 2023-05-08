import random
import csv

# Define the dimensions of the array
rows = 35
cols = 10

# Define the number of ones in each row and column
num_ones_row = 3
num_ones_left_col = 10
num_ones_right_col = 11

# Initialize the array with zeros
arr = [[0 for j in range(cols)] for i in range(rows)]

# Fill the first 5 columns with ones
for i in range(rows):
    for j in range(num_ones_left_col):
        arr[i][j] = 1

# Fill the last 5 columns with ones
for i in range(rows):
    for j in range(cols - num_ones_right_col, cols):
        arr[i][j] = 1

# Fill each row with num_ones_row ones in random positions
for i in range(rows):
    ones_left = num_ones_row
    while ones_left > 0:
        j = random.randint(0, cols - 1)
        if arr[i][j] == 0:
            arr[i][j] = 1
            ones_left -= 1

# Write the array to a CSV file
with open('array.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile)
    for row in arr:
        writer.writerow(row)
