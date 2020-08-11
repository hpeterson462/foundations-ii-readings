# Articles

## *SQLBolt*

* Structured Query Language
* Allows technical and non-technical users to query, manipulate, and transform data from a relational database
* Provide safe and scalable storage
* A relational database represents a collection of related (two-dimensional) tables
    * Similar to an Excel spreadsheet
* A query is a statement which declares what data we are looking for, where to find it, and (optionally) how to transform it before it is returned
    * Has a specific syntax
* `Select query for a specific columns
SELECT column, another_column, …
FROM mytable;`
    * Result of query will be a two-dimensional set of rows and columns
*  To filter certain results from being returned, we need to use a WHERE clause in the query
    * Applied to each row of data by checking specific column values to determine whether it should be included in the results or not
    * `Select query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;`
    * Complex clauses can be constructed by joining numerous AND or OR logical keywords
    * Allows the query to run faster due to the reduction in unnecessary data being returned
* Useful operators:
    * Case sensitive exact string comparison `=` 
    * Case sensitive exact string inequality comparison `!=` `<>`
    * Case insensitive exact string comparison `LIKE`
    * Case insensitive exact string inequality comparison `NOT LIKE`
    * sed anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE) `%`
    * Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) `-`
    * String exists in a list `IN (...)`
    * String does not exist in a list `NOT IN (...)`
* DISTINCT
    * To discard rows that have a duplicate column value
    * `Select query with unique results
SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);`
* ORDER BY
    * Sort your results by a given column in ascending or descending order
    * `Select query with ordered results
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC;`
*  Used with the ORDER BY clause are the LIMIT and OFFSET clauses
    * indicate to the database the subset of the results you care about
    * LIMIT will reduce the number of rows to return
    * OFFSET will specify where to begin counting the number rows from
    * `Select query with limited rows
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;`
* Database schema is what describes the structure of each table, and the datatypes that each column of the table can contain
* INSERT
    * Declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert
    * `Insert statement with values for all columns
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;`
* UPDATE
    * Specify exactly which table, columns, and rows to update
    * `Update statement with values
UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;`
* Always write the constraint first and test it in a SELECT query to make sure you are updating the right rows
    * Only then writing the column/value pairs to update
* DELETE
    * Delete data from a table in the database
    * Recommended that you run the constraint in a SELECT query first to ensure that you are removing the right rows
        * `Delete statement with condition
DELETE FROM mytable
WHERE condition;`
* CREATE TABLE
    * create a new database table
        * `Create table statement w/ optional table constraint and default value
CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);`
* ALTER TABLE 
    * update your corresponding tables and database schemas
    * Specify the data type of the column along with any potential table constraints and default values to be applied to both existing and new rows
    * `Altering table to add new column(s)
ALTER TABLE mytable
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;`
    * `Altering table to remove column(s)
ALTER TABLE mytable
DROP column_to_be_deleted;` 
* DROP TABLE
    * Differs from the DELETE statement in that it also removes the table schema from the database entirely
    * `Drop table statement
DROP TABLE IF EXISTS mytable;`
