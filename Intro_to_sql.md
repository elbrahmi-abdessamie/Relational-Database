# Introduction To SQL

## What SQL is?
SQL is a standard language that can be used with all databases. It's useful when working with relational databases, which require a language that can intract with structured data (MySQL, PostgreSQL, Oracl, and Microsoft SQL Server).

The next question this raises, is how does a database interpret or read and execute instructions given using SQL.
```
SQL is the standardized language that enables communication between applications and relational database management systems (RDBMS). It provides a comprehensive set of capabilities for defining, manipulating, querying, controlling, and administering databases, making it an essential tool for managing and utilizing data stored in relational databases (MySQL, PostgreSQL, Oracl, and Microsoft SQL Server).
```
## The role of SQL In Databases
SQL (Structured Query Language) is the industry-standard language for managing and manipulating relational databases. It plays a central role in the following aspects:

1- **Data Definition (DDL):**

- CREATE, ALTER, and DROP statements to define, modify, and delete database objects like tables, indexes, and constraints.
- Allows for structuring and organizing data within the database.


2- **Data Manipulation (DML):**

- INSERT, UPDATE, and DELETE statements to add, modify, and remove data from database tables.
- Enables data management and maintenance tasks.


3- **Data Query (DQL):**

- SELECT statement is the most commonly used for retrieving data from one or more tables.
- Supports complex queries involving joins, filtering, sorting, and aggregations.
- Provides a powerful way to extract and analyze data.


4- **Data Control (DCL):**

- GRANT and REVOKE statements to control access privileges to database objects.
- Ensures data security and privacy by managing user permissions.


5- **Transaction Management:**

- BEGIN, COMMIT, and ROLLBACK statements for managing transactions.
- Ensures data integrity and consistency by following ACID properties.


6- **Database Administration:**

- Statements for creating, managing, and maintaining databases, users, and roles.
- Enables centralized administration and control over the database environment.


7- **Integration with Programming Languages:**

- SQL can be embedded within programming languages like Java, Python, C#, etc.
- Allows applications to interact with databases programmatically.
- Facilitates the development of data-driven applications.

## Why SQL?

Now we bring the light to why do developers use SQL to interact with databases?

SQL is a popular language choice for databases because of the many advantages that it offers, It's such a bridge between a relational database and its users and offers web developers a wide range of advantages.

**Here is a some of those advantages:**

*Low Coding Requirement*

- SQL requires very little coding skills
- Just a set of keywords for basic operations
- Minimal lines of code for CRUD (Create, Read, Update, Delete) tasks

*User-Friendly and Interactive*

- Highly user-friendly language
- Allows writing complex queries quickly
- Interactive environment for efficient data manipulation

*Standard and Portable Language*

- Industry-standard for relational databases (MySQL, PostgreSQL, Oracle, etc.)
- Portable across different hardware, operating systems, and platforms
- Write once, use anywhere

*Comprehensive Database Management*

- Covers all aspects of database administration
- Data Definition, Data Manipulation, Data Control, and Querying
- Handles complex data processing and analysis

*Efficient Data Processing*

- Enables quick and efficient processing of large amounts of data
- Powerful querying capabilities for data retrieval and analysis
- Optimized for high-performance data operations

## SQL Syntax:

- The SQL Commands are grouped into four categories known as DDL, DML, DCL and TCL depending on their functionality, namely the type of operation they’re used to perform.  Let’s explore these commands in greater detail.


**Data Definition Language (DDL)**

### CREATE command:

Purpose: To create the database or tables inside the database

Syntax:
```sql
CREATE TABLE table_name (<column_name1> datatype(size), <column_name2> datatype(size), <column_name3> datatype(size));
```

### DROP Command 

Purpose: To delete a database or a table inside the database. 

Syntax:
```sql
DROP TABLE <table_name>;
```

### ALTER Command 

Purpose: To change the structure of the tables in the database such as changing the name of a table, adding a primary key to a table, or adding or deleting a column in a table.

Syntax:
- Add column into table

```sql
ALTER TABLE <table_name> ADD (<column_name> datatype(size));
```

- Add primary key to table

```sql
ALTER TABLE <table_name> ADD primary key (<column_name>);
```

### TRUNCATE Command

Purpose: To remove all records from a table, which will empty the table but not delete the table itself. 

Syntax:

```sql
TRUNCATE TABLE <table_name>
```

### COMMENT Command

Purpose: To add comments to explain or document SQL statements by using double dash (--) at the start of the line. Any text after the double dash will not be executed as part of the SQL statement. These comments are not there to build the database. They are only for your own use.   

Syntax:

```sql
--Retrieve all data from a table
SELECT * FROM table_name; 
```

**Data Query Language (DQL)**

### SELECT Command

Purpose: To retrieve data from tables in the database. 

Syntax :

```sql
SELECT * FROM table_name;
```

**Data Manipulation Language (DML)**

### INSERT Command

Purpose: To add records of data into an existing table. 
Syntax to insert data into three columns in a table:

```sql
INSERT INTO <table_name> (column1, column2, column3) VALUES (value1, value2, value3);
```

### UPDATE Command 

Purpose: To modify or update data contained within a table in the database. 

Syntax :

```sql
UPDATE <table_name> SET column1 = value1, column2 = value2 WHERE condition;
```

### DELETE Command

Purpose: To delete data from a table in the database.

Syntax :

```sql
DELETE FROM <table_name> WHERE condition;
```

**Data Control Language (DCL)**

The Data Control Language (DCL) in SQL is used to manage user privileges and access control within a database system. It allows you to grant or revoke permissions to users, enabling them to perform various operations on database objects.

The two main commands in DCL are:

### GRANT Command: 

Purpose: This command is used to provide specific privileges to users or roles, allowing them to access and manipulate the database. It grants permissions to perform actions such as creating tables, selecting data, updating data, or executing stored procedures.

syntax:

```sql
GRANT SELECT, INSERT ON table_name TO user_name;
```

### REVOKE

Purpose: This command is used to remove previously granted privileges from users or roles, restricting their access to database objects or operations.

Syntax:

```sql
REVOKE SELECT ON table_name FROM user_name;
```


**Transaction Control Language (TCL)**

The Transaction Control Language (TCL) in SQL is used to manage transactions, which are logical units of work that ensure data integrity and consistency in a database.

### COMMIT Command: 

Purpose: This command is used to save all the changes made within a transaction permanently to the database. Once a transaction is committed, it cannot be undone, and the changes become visible to other users.

Syntax:

```sql
COMMIT;
```

### ROLLBACK Command:
Purpose: This command is used to undo all the changes made within a transaction since the last commit or rollback operation. It restores the database to its previous consistent state, effectively canceling the transaction.

Syntax:

```sql
ROLLBACK;
```

TCL is essential for maintaining data integrity by allowing you to group multiple SQL statements into a single transaction. If any part of the transaction fails, the entire transaction can be rolled back, ensuring that the database remains in a consistent state.

Both DCL and TCL are essential components of SQL, providing mechanisms for controlling access and managing transactions in a database environment, ensuring data security, integrity, and consistency.