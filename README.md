# DAX_IN_POWERBI

Project Case: Mastering DAX in Power Bi.

I have completed an interesting project which explains how to use Power Bi, a data visualization and leading business intelligence tool, and Data Analysis Expression (DAX) to build hands-on expertise in creating interactive reports, dashboards and advanced analytics solutions.
Here is a breakdown of the steps and techniques implemented in this project:

#### Calculated Columns

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

#### Calculated Measures

        Ratios and Percentages:
        Created a column for sales margin % using the SUMX function.

        Aggregations:
        The total sales amount was calculated also using the SUMX function to get the Total Sales of all products.

#### Calculated Tables

        New tables are created by clicking on the modeling tab in the Powerbi ribbon then enter the formula to define the table. In this case, I copied the content of another data into the new table I created.

        Filter function was used to filter a particular set of data I needed for my calculations.

        SUMX function is used to sum an expression for each row, it iterates row by row and then sum up the results unlike the basic SUM function which adds up the values in a single columns. I used this function to derive the total sum of sales.

        The ALL function was used to get sales for all data, ignoring all the filters originally applied in the data.