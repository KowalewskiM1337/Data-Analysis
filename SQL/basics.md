SELECT DISTINCT _columnName_ --> selects item that distinct from others

SELECT * ... ORDER BY _columnName_ --> used to sort results in ascending or descending order

ROUND(_columnName_, x) --> rounds int value, where x is how many numbers after coma include

CEILING(_columnName_) --> rounds int value up

FLOOR(_columnName_) --> rounds int value down

ABS(_columnName_) --> takes the absolute of number (module)

LENGTH('text') / LEN('text') --> shows how many characters are in "text"

UPPER() --> changes all the letters to upper case letters

LOWERCASE --> changes all the letters to lower case letters

TRIM() --> removes all the whitespaces
    -- LTRIM() --> removes whitespace from the left
    -- RTRIM() --> removes whitespace from the right

LEFT('text', x) --> displays x amount of characters from the text in '' beginning from the left

RIGHT('text', x) --> displays x amount of characters from the text in '' beginning from the right

SUBSTRING('string', 2, x) --> display x amount of characters from the text in '' beginning from the 2nd position in text

REPLACE('string', 'a', 'z') --> replace 'a' in 'string' with 'z' [!!! CASE SENSITIVE !!!]

LOCATE('x', 'Alexander') --> locates character 'x' where it sits in 'Alexander' string

CONCAT() --> concatenate strings

// DATE

NOW() --> current date + date time

CURDATE() --> current date

CURTIME() --> current time

YEAR(NOW()) --> outputs only year from today's date

DAYNAME() --> outputs name of the day of the given date

// IF functions

Syntax: IF(condition, if true do this, if false do this)

Case statement: 

CASE
    WHEN ___ THEN ___
    WHEN ___ THEN ___ (an so on, it's similar to if else...)
    ELSE '...'
END AS '...'



CAST and CONVERT

Ex: SELECT CAST("2025-01-01" AS DATETIME); --> converts string to datetime

Ex: SELECT CAST(columnName, DATETIME); --> converts whole column to datetime

Ex: SELECT CONVERT(columnName, DATETIME); --> as mentioned above example



// GROUP BY

1. Summaries the rows
2. Often used with aggregate functions such as MAX, MIN, AVG etc.



// HAVING vs WHERE

HAVING --> filters based of aggregated columns
            comes after GROUP BY statement
            works with aggregate functions
WHERE --> filters based of regular columns
            comes before GROUP BY statement

!!! The main problem is execution order of those statements which can cause errors in query !!!


// Rollup 

syntax: GROUP BY _columnName_ WITH ROLLUP
--> rolls up and counts all the values in the rows in a column




// JOINS

- Are used to combine rows from two or more tables based on a related column
- There are several types of JOINs in SQL:
  - INNER JOIN
  - OUTER JOIN
  - CROSS JOIN
  - SELF JOIN
  - RIGHT JOIN
  - LEFT JOIN


1. INNER JOIN

- Returns records that have matching values in both tables

2. LEFT AND RIGHT JOIN

- RIGHT JOIN: Returns all records from the right table, and the matched records from the left table
- LEFT JOIN: Returns all records from the left table, and the matched records from the right table

3. FULL (OUTER) JOIN

- Returns all records from both tables
- It's essentially LEFT JOIN and RIGHT JOIN combined

4. SELF JOIN

- Joins the table to itself
- Has to have an alias to the table

5. CROSS JOIN

- Returns all possible combinations of all rows
- There's no need of "ON" clause


// JOIN vs UNION

UNION --> used to combine the results of two or more SELECT statements into a single result set
JOIN --> typically give a horizontal output, while UNIONs give a vertical output


























































