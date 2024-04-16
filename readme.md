## Final Project Description

**1. Load the data:**

* Create a `pandemic` schema in the database using an SQL command.
* Set it as the default schema using an SQL command.
* Import data using the Import wizard as you did in Topic 3:
    * `infectious_cases.csv`
* Review the data to get context.
    * ** As you can see, the Entity and Code attributes are constantly repeated. Get rid of this by normalizing the data.**

**2. Normalize the `infectious_cases` table. Save two normalized data tables to the same schema.**

**3. Analyze the data:**

* For each unique combination of Entity and Code or their id, calculate the average, minimum, maximum value and sum for the `Number_rabies` attribute.
    * ** Consider that the `Number_rabies` attribute may contain empty values ‘’ - you must first filter them out.**
* Sort the result by the calculated average value in descending order.
* Select only 10 rows for output.

**4. Build a difference in years column.**

* For the original or normalized table for the `Year` column, construct using built-in SQL functions:
    * An attribute that creates the date of the first of January of the corresponding year,
        * ** For example, if the attribute contains the value ’1996’, the value of the new attribute should be ‘1996-01-01’.**
    * An attribute that is equal to the current date,
    * An attribute that is equal to the difference in years between the two aforementioned columns.
        * ** It is not necessary to list all other attributes, such as `Number_malaria`.**

** You may need the material from Topic 7 to find the necessary built-in functions.**

**5. Build your own function.**

* Create and use a function that builds the same attribute as in the previous task: the function should take a year value as input and return the difference in years between the current date and the date created from the year attribute (1996 → ‘1996-01-01’).
    * ** If you did not complete the previous task, you can build another function - a function that calculates the number of diseases over a certain period. To do this, you need to divide the number of diseases per year by a certain number: 12 - to get the average number of diseases per month, 4 - per quarter or 2 - per half year. Thus, the function will take two parameters: the number of diseases per year and an arbitrary divisor. You should also use it - run it on the data. Since not all rows contain the number of diseases, you will need to filter out those that do not have a numeric value (≠ ‘’).**
