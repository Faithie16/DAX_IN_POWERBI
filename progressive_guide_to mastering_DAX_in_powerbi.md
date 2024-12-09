# Step by Step Guide to Mastering DAX in Powerbi
## Calculated Columns

Before creating new columns, I noticed my data wasn't properly cleaned especially the date columns. The first step was to clean my data abit by highlighting the date columns one after another and changed the format to "Short Date.
![Cleaned Date Column](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/Line%20amount%20column%20created%20.jpg)

After cleaning the data, I used the YEAR(TODAY()) statement in power bi to derive the actual age of customers for better analysis.

I noticed some blank spaces in the birthdate column which returned "2024" as the customer's age, so I then included the IF statement in power bi to also return blank spaces in the age column using this function:
Age = IF(ISBLANK('Customer'[Birth Date]), BLANK(), YEAR(TODAY()) - YEAR('Customer'[Birth Date]))

![Age column](https://github.com/Faithie16/DAX_IN_POWERBI/blob/main/INtro%20to%20DAX%20imgs/Calculated%20age.jpg)

