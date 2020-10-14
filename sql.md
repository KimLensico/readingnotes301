# SQL

## What is SQL?
> SQL, or **Structured Query Language** - a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database 
- due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications

## Relational Databases
> represents a collection of related (two-dimensional) tables 
 - Each of the tables are similar to an Excel spreadsheet, with:
   - a fixed number of named columns (the attributes or properties of the table) 
   - any number of rows of data

## SELECT queries 101
To retrieve data from a SQL database, we need to write SELECT statements
  - are often colloquially referred to as queries
    - a query is just a statement which declares:
      1. what data we are looking for 
      2. where to find it in the database
      3. [ optionally ] how to transform it before it is returned 
    - has a specific syntax 

## Queries with constraints: 
### WHERE
- In order to filter certain results from being returned, we need to use a WHERE clause in the query 
  - *The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.*
- More complex clauses can be constructed by joining numerous AND or OR logical keywords 
  - (ie. num_wheels >= 4 AND doors <= 2)
- When writing WHERE clauses with columns containing text data, SQL supports a number of useful operators to do things:
  - like case-insensitive string comparison 
  - wildcard pattern matching

## Filtering and sorting Query results
### DISTINCT
> Even though the data in a database may be unique, the results of any particular query may not be 
- In such cases, SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.
  - DISTINCT keyword will blindly remove duplicate rows

### ORDER BY
> a way to sort your results by a given column in ascending or descending order
  - When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. 
  - In some databases, you can also specify a collation to better sort data containing international text

  ### LIMIT
  > reduce the number of rows to return

  ### OFFSET
  > [ OPTIONAL ] specify where to begin counting the number rows from

## Schema
***database schema** is what describes:
  - the structure of each table 
  - the datatypes that each column of the table can contain.

### INSERT 
INSERT declares: 
  - which table to write into the columns of data that we are filling
  - one or more rows of data to insert. 
  
*In general, each row of data you insert should contain values for every corresponding column in the table. You can insert multiple rows at a time by just listing them sequentially.*

[ In some cases ] if you have incomplete data and the table contains columns that support default values, you can insert rows with only the columns of data you have by specifying them explicitly.
   - the number of values need to match the number of columns specified. 
   - inserting values this way has the benefit of being forward compatible. 
    - [ e.g ] if you add a new column to the table with a default value, no hardcoded INSERT statements will have to change as a result to accommodate that change.

###


###


###


###


### 


  **[SQL Cheatsheet](http://www.cheat-sheets.org/sites/sql.su/)**