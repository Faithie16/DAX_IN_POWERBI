# DAX_IN_POWERBI

Project Case: Mastering DAX in Power Bi.

I have completed an interesting project which explains how to use Power Bi, a data visualization and leading business intelligence tool, and Data Analysis Expression (DAX) to build hands-on expertise in creating interactive reports, dashboards and advanced analytics solutions.
Here is a breakdown of the steps and techniques implemented in this project:

###### Calculated Columns

Data Cleaning:
Highlighted the date columns and changed the format to "Short date"

Actual Age:
Used the IF statement to determine the actual age of the customers for better analysis.
There was some blank spaces in the birthdate column which returned "2024" as the customer's age, I included the "IF (ISBLANK,CUSTOMER BIRTHDATE), RETURN BLANK() to also return blank spaces in the age column.

Line Amount:
Created a new column and multiplied the Sales Unit Price by the Sales Quantity to get the Unit Cost.

Line Margin:
a new column was created for the profit on each product by using the BODMAS mathematical guide to calculate the profit.

Line Margin%:
Divided the Line Margin by the Line Amount to derive the percentage profit on each product.

Time Intelligence:
Year(Today) was implemented in the IF statement to derive the actual age of the customers from their birth date.

###### Calculated Measures
