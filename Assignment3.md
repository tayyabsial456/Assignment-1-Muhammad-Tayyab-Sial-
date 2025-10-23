# Assignment 3: Global Sales Data Analyst

## Objective
To act as a Data Analyst, cleaning, transforming, and analyzing a simulated sales dataset to answer key business questions. This assignment integrates Pandas techniques for indexing, filtering, grouping, data cleaning, and date/time operations.

## Part 1: Reading and inspecting data
    - Read the data from the provided .csv file into a pandas DataFrame
    - Print the first 5 rows and the data types of all columns using appropiate DataFrame methods

## Part 2: Data Cleaning and Indexing

    1. Handling Missing Values and Casting:
        - Fill Missing Values: Replace the missing values (NaN) in the Units_Sold column with the mean value of the entire column.
        - Data Type Casting: Convert the Sales column to a numeric data type (float). Handle any remaining non-numeric values during conversion (e.g., by coercing them to NaN and then filling them with 0).
        - Casting Dates: Convert the Date column to a proper datetime object.
    2. Indexing and Setting:
        - Use the OrderID column to set a new index for the DataFrame.
        - Reset the index, and then set the Date column as the index. This makes the DataFrame suitable for time series analysis.

## Part 3: Filtering, Modifying, and Sorting

    1. Filtering Data:
        - Create a new DataFrame named high_value_sales that contains only the sales records where the Sales amount is greater than $500 AND the Region is 'Europe'. Print the head of this new DataFrame.
    2. Updating and Adding Columns:
        - Update a Row: Select a specific row (e.g., the 5th row of the original DataFrame) and modify its Units_Sold value to 99.
        - Add a Column: Add a new column named Profit calculated as: Profit = Sales * 0.20.
    3. Sorting Data:
        - Sort the DataFrame first by Region (ascending) and then by Sales (descending). Print the first few rows of the sorted DataFrame.

## Part 4: Grouping and Aggregation (Analysis)
Answer the following business questions using the groupby() method and appropriate aggregation functions:

    1. Regional Performance:
        - Group the data by Region and calculate the total sum of Sales and the average Units_Sold for each region. Print the result.
    2. Product Deep Dive:
        - Group the data by Product and find the maximum Profit achieved for each product type. Print the result.
    3. Time Series Analysis (Bonus/Challenge):
        - Since the Date column is the index, use a time-based resampling method (e.g., .resample('M')) to calculate the monthly total sales. Print the result.
