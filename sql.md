# Introduction to SQL

## What is SQl? SQL its a Language that allows both technical and non-technical users to:-
    1 Query
    2 Manipulate
    3 Transform

### Ex1
>Selecting a Column, OR different columns...
#####  Solution:
![image](./images/Sql_Imgs/ex1.1.png)
___
![image](./images/Sql_Imgs/ex1.2.png)
___
![image](./images/Sql_Imgs/ex1.3.png)
___
![image](./images/Sql_Imgs/ex1.4.png)
___
![image](./images/Sql_Imgs/ex1.5.png)
___

## Ex2
>Use WHERE to  add a condition for checking a specific column values.

#### Syntax example:
    SELECT column, another_column, …
    FROM mytable
    WHERE condition
        AND/OR another_condition
        AND/OR …;

>**Operators:**
![image](./images/Sql_Imgs/ex2.table.png)

#####  Solutions:
![image](./images/Sql_Imgs/ex2.1.png)
___
![image](./images/Sql_Imgs/ex2.2.png)
___
![image](./images/Sql_Imgs/ex2.3.png)
___
![image](./images/Sql_Imgs/ex2.4.png)
___

### Ex3
>Using WHERE with the Regular Expressions (Strings)

![image](./images/Sql_Imgs/ex3.table.png)

#####  Solutions:
![image](./images/Sql_Imgs/ex3.1.png)
___
![image](./images/Sql_Imgs/ex3.2.png)
___
![image](./images/Sql_Imgs/ex3.3.png)
___
![image](./images/Sql_Imgs/ex3.4.png)
___

## Ex4
>**DISTINCT KEYWORD:**
- Using **Distinct** to remove duplicate rows !!.

#### Syntax example: 
    SELECT DISTINCT column, another_column, …
    FROM mytable
    WHERE condition(s);

>**Sorting(ORDER BY) (ASC/DESC):**
- Sort the results by a given column in ascending or descending order.
- Each row is sorted alpha-numerically based on the specified column's value.

#### Syntax: 
    SELECT column, another_column, …
    FROM mytable
    WHERE condition(s)
    ORDER BY column ASC/DESC;

>**Limiting results to a subset:**
- LIMIT: will reduce the number of rows to return!
- OFFSET: will specify where to begin counting the number rows from. _(Optional !!)_

#### Syntax: 
    SELECT column, another_column, …
    FROM mytable
    WHERE condition(s)
    ORDER BY column ASC/DESC
    LIMIT num_limit OFFSET num_offset;

##### Solution:
![image](./images/Sql_Imgs/ex4.1.png)
___
![image](./images/Sql_Imgs/ex4.2.png)
___
![image](./images/Sql_Imgs/ex4.3.png)
___
![image](./images/Sql_Imgs/ex4.4.png)
___

## Ex5
>**Review,Simple SELECT Queries**

##### Solution:
![image](./images/Sql_Imgs/rev1.1.png)
___
![image](./images/Sql_Imgs/rev1.2.png)
___

## Ex6
>Database normalization
>>Database normalization is useful because it minimizes duplicate data in any single table, and allows for data in the database to grow independently of each other.

>Multi-table queries with JOINs**
>>Tables that share information about single-table entity should have a primary key that identifies that entity uniquely across the database.

### **JOIN**
Combine row data across two separate tables using the unique key.
### **INNER JOIN**
Matches rows from the first table and the second table which have the same key

#### Syntax example: 
    SELECT column, another_table_column, …
    FROM mytable
    INNER JOIN another_table 
        ON mytable.id = another_table.id
    WHERE condition(s)
    ORDER BY column, … ASC/DESC
    LIMIT num_limit OFFSET num_offset;

##### Solutions:
![image](./images/Sql_Imgs/ex6.1.png)
___
![image](./images/Sql_Imgs/ex6.2.png)
___
![image](./images/Sql_Imgs/ex6.3.png)

## Ex13:
>what is Schema?
>>it is what describes the structure of each table, and the datatypes that each column of the table can contain.
___
>**Inserting new data[all cloumns/specific one]**

    - Insert statement with values for all columns
    INSERT INTO mytable
    VALUES (value_or_expr, another_value_or_expr, …),
        (value_or_expr_2, another_value_or_expr_2, …),
        …;
___
    - Insert statement with specific columns
    INSERT INTO mytable
    (column, another_column, …)
    VALUES (value_or_expr, another_value_or_expr, …),
        (value_or_expr_2, another_value_or_expr_2, …),
        …;

##### Solutions:
![image](./images/Sql_Imgs/ex13.1.png)
___
![image](./images/Sql_Imgs/ex13.2.png)
___
## Ex14:
>**Updating rows**

#### Syntax:
    UPDATE mytable
    SET column = value_or_expr, 
        other_column = another_value_or_expr, 
        …
    WHERE condition;
___
##### Solutions:
![image](./images/Sql_Imgs/ex14.1.png)
___
![image](./images/Sql_Imgs/ex14.2.png)
___
![image](./images/Sql_Imgs/ex14.3.png)

## Ex15:
>**Deleting Rows**

#### Syntax:
    DELETE FROM mytable
    WHERE condition;
>If you decide to leave out the WHERE constraint, then all rows are removed, which is a quick and easy way to clear out a table completely !!

##### Solutions:
![image](./images/Sql_Imgs/ex15.1.png)
___
![image](./images/Sql_Imgs/ex15.2.png)
___

## Ex16:
>**Creating tables**
>When you have new entities and relationships to store in your database, you can create a new database table using the CREATE TABLE statement,the new table is defined by its table schema
>>If there already exists a table with the same name, the SQL implementation will usually throw an error, so to suppress the error and skip creating a table if one exists, you can use the IF NOT EXISTS clause!!.

#### Syntax example:
    CREATE TABLE IF NOT EXISTS mytable (
        column DataType TableConstraint DEFAULT default_value,
        another_column DataType TableConstraint DEFAULT default_value,
        …
    );

#### Table Data Types:
![image](./images/Sql_Imgs/ex16.table.dataType.png)

#### Table Constraints:
![image](./images/Sql_Imgs/ex16.table.Constrains.png)

##### Solutions:
![image](./images/Sql_Imgs/ex16.1.png)
___

## Ex17:
**Altering tables(Editing!)**
>To add, remove, or modify columns and table constraints.

>**Adding Columns**

#### Syntax example:
    ALTER TABLE mytable
    ADD column DataType OptionalTableConstraint 
        DEFAULT default_value;

>**Removing columns**

#### Syntax Example:
    ALTER TABLE mytable
    DROP column_to_be_deleted;

>**Renaming the table**

#### Syntax:
    ALTER TABLE mytable
    RENAME TO new_table_name;

##### Solutions:
![image](./images/Sql_Imgs/ex17.1.png)
___
![image](./images/Sql_Imgs/ex17.2.png)
___

## Ex18:
**Dropping tables**
To remove an entire table including all of its data and metadata

#### Syntax example:
    DROP TABLE IF EXISTS mytable;

##### Solution:
![image](./images/Sql_Imgs/ex18.1.png)
___
![image](./images/Sql_Imgs/ex18.2.png)
___
___