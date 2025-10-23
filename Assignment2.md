# Assignment 2: E-commerce Inventory Analyst

## Objective
To simulate a small inventory analysis task using NumPy for data manipulation and calculations, and Pandas for structured data viewing. The goal is to identify underperforming products and calculate new stocking levels.

## Part 1: NumPy Array Manipulation (The Core Data)
Assume you are working with an inventory dataset. Create the following data using NumPy arrays:

    1. Product Data:
        - Create a 1-dimensional NumPy array named product_ids containing 10 unique integer IDs (e.g., 1001, 1002, ...).
        - Create a 2-dimensional NumPy array named inventory_data with a shape of (10, 3). This array will represent 10 products and their details:
            - Column 0: Current Stock Level (Integers, e.g., 50, 120, 30)
            - Column 1: Average Weekly Sales (Floats, e.g., 15.5, 3.2, 25.0)
            - Column 2: Unit Cost (Floats, e.g., 10.99, 50.50, 5.00)
    2. Basic Calculations and Attributes:
        - Print the shape and data type (dtype) of the inventory_data array.
        - Use arithmetic operations on arrays to calculate the Total Value of the current stock for all products. **Formula: Total Value = Current Stock Level * Unit Cost**. Print the resulting array.
    3. Slicing, Indexing, and Statistics:
        - Use NumPy slicing to extract and print the data for products 3 through 7 (inclusive) from inventory_data.
        - Use a NumPy aggregation function (e.g., mean, sum, max) to find the average Average Weekly Sales across all 10 products. Print this result.
        - Access and print the Unit Cost of the product at index 0 (the first product).

## Part 2: Advanced NumPy Analysis (Re-stocking Logic)
The core task involves identifying products that need immediate attention:

    1. Boolean Masking (The "Low-Stock" Check):
        - Calculate the number of weeks the current stock will last based on average sales. Formula: Weeks of Stock = Current Stock Level / Average Weekly Sales.
        - Create a boolean mask that is True for any product where the Weeks of Stock is less than 4 (i.e., less than a month's supply).
        - Use this boolean mask to extract and print the entire rows from inventory_data for the products that are low in stock.
    2. Reshaping and Concatenation (Updating Data):
        - Create a new 1-dimensional NumPy array named reorder_quantity where each value is calculated as: (4 * Average Weekly Sales) - Current Stock Level (i.e., enough to bring stock up to a 4-week supply).
        - Use a conditional statement or NumPy function to ensure that all values in reorder_quantity are non-negative (you can't reorder a negative amount).
        - Reshape the reorder_quantity array to a (10, 1) 2D array.
        - Use NumPy concatenation to combine the original inventory_data array with the new reorder_quantity array along the appropriate axis (resulting in a (10, 4) array). Print the new, concatenated array.

## Part 3: Introduction to Pandas (Viewing the Results)
To make the data readable, use the basics of the Pandas library:

    1. Create a DataFrame:
        - Create a Pandas DataFrame using the final, concatenated NumPy array from Part 2.
        - Assign appropriate column names (e.g., 'Stock', 'Sales', 'Cost', 'Reorder Qty').
    2. Basic Selection:
        - Select and print only the 'Stock' and 'Reorder Qty' columns from the DataFrame.
        - Select and print the first 5 rows of the DataFrame.