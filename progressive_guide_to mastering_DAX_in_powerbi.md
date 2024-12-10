# Step by Step Guide to Mastering DAX in Powerbi
## Calculated Columns

Before creating new columns, I noticed my data wasn't properly cleaned especially the date columns. The first step was to clean my data abit by highlighting the date columns one after another and changed the format to "Short Date.
![Cleaned Date Column](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/Line%20amount%20column%20created%20.jpg)

After cleaning the data, I used the YEAR(TODAY()) statement in power bi to derive the actual age of customers for better analysis.

I noticed some blank spaces in the birthdate column which returned "2024" as the customer's age, so I then included the IF statement in power bi to also return blank spaces in the age column using this function:
        Age = IF(ISBLANK('Customer'[Birth Date]), BLANK(), YEAR(TODAY()) - YEAR('Customer'[Birth Date]))

![Age column](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/Calculated%20age.jpg)

I went further to create a column on the sales table that will contain the Unit cost of each product which I called "Line Amount" in my project by multiplying the sales UNIT PRICE by QUANTITY, as seen in the Image below.

![Line Amount](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/Line%20amount%20column%20created%20.jpg)

Further more, The Line Margin column was created mainly to derive the profit margin for each product. This feat was accomplished, using the BODMAS idea, by minusing the sales UNIT COST from NET PRICE and multiply by QUANTITY.

![Line Margin](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/line%20margin%20created.jpg)

To get the Line Margin Percentage, the Line Margin was divided by the Line Amount using the SUM function.

![Line margin percentage](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/Line%20margin%20percent%20created.jpg)

## Calculated Measures

To get the columns I wanted to work on, I selected Age, Line Margin% and Margin%  and inserted them in the column table marked in the red circle in the image below.
![Column](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/sales%20-%20Copy.jpg)

All the columns selected appear on the white space.

Moving on, we need to calculate the sales amount using the SUM function by creating a measure on the sales data.
The function used to achieve this feat is as seen; 
        Sales Amount = SUM('Sales'[Line Amount])
![Sales amount using sum function](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/sales.jpg)

However, while perusing this data created, I realized the Margin% to be incorrect since the lowest percentage has to be 1% atleast.

![Sales amount using SUMX](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/sales%20amount%20using%20SUMX.jpg)

I went ahead to use SUMX function instead to get the correct and straightforward percentage value.

Furthermore, In Power Bi, variables are a powerful feature in DAX (Data Analysis Expressions) that allow you to store and reuse values or expressions within a single DAX formula. Variables make your calculations more readable, efficient, and reusable.

I used the variable (VAR) function to calculate the Margin% to ensure the calculations were correct from inception.

![Margin using Variable](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/margin%25%20using%20variable.jpg)

        VAR: Declares a variable and assigns it a value or expression.

        RETURN: Specifies the final calculation or result that uses the variable(s).
