## Final Project

### 1. Load Data

1. Create a schema `pandemic` in the database using SQL commands.
2. Set it as the default schema using SQL commands.
3. Import data using Import wizard as you did in Topic 3:
    - `infectious_cases.csv`
4. Review the data to be in context.
    - ** As you can see, the Entity and Code attributes are constantly repeated. Get rid of this by normalizing the data.**

### 2. Normalize the `infectious_cases` table. Save two tables with normalized data in the same schema.

### 3. Analyze the data

1. For each unique combination of Entity and Code or their id, calculate the average, minimum, maximum and sum for the `Number_rabies` attribute.
    - ** Consider that the `Number_rabies` attribute may contain empty values ‘’ - you need to filter them out beforehand.**
2. Sort the result by the calculated average value in descending order.
3. Select only 10 rows for output.

### 4. Build a difference in years column

1. For the original or normalized table for the `Year` column, construct using built-in SQL functions:
    - An attribute that creates the date of the first of January of the corresponding year,
        - ** For example, if the attribute contains the value '1996', then the value of the new attribute should be '1996-01-01'.**
    - An attribute that is equal to the current date,
    - An attribute that is equal to the difference in years between the two aforementioned columns.
        - ** You do not need to list all other attributes, such as Number_malaria.**

 To find the necessary built-in functions, you may need the material from topic 7.

### 5. Build your own function

1. Create and use a function that builds the same attribute as in the previous task: the function should take a year value as input and return the difference in years between the current date and the date created from the year attribute (1996 → '1996-01-01').
    - ** If you did not complete the previous task, then you can build another function - a function that counts the number of cases over a certain period. To do this, you need to divide the number of cases per year by a certain number: 12 - to get the average number of cases per month, 4 - per quarter or 2 - per half year. Thus, the function will take two parameters: the number of cases per year and an arbitrary divisor. You also have to use it - run it on the data. Since not all rows contain the number of cases, you will need to filter out those that do not have a numeric value (≠ '').**