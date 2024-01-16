<p class="has-line-data" data-line-start="0" data-line-end="4">Install Mysql<br>
Download link :<a href="https://dev.mysql.com/downloads/workbench/">https://dev.mysql.com/downloads/</a><br>
Sample Database Query Link: <a href="https://www.w3schools.com/MySQL/mysql_join.asp">https://www.w3schools.com/MySQL/mysql_join.asp</a></p>

<p class="has-line-data" data-line-start="0" data-line-end="4">Database Testing is a type of software testing that checks the schema, tables, triggers, etc. of<br>
the Database under test.<br>
The 3 types of Database Testing are</p>
<ol>
<li class="has-line-data" data-line-start="4" data-line-end="5">Structural Testing</li>
<li class="has-line-data" data-line-start="5" data-line-end="6">Functional Testing</li>
<li class="has-line-data" data-line-start="6" data-line-end="7">Non-functional Testing</li>
</ol>

### Functional Database Testing<br>
<p class="has-line-data" data-line-start="0" data-line-end="10">Functional Database Testing is a type of database testing that is used to validate the<br>
functional requirements of a database from the end-user’s perspective. The main goal of<br>
functional database testing is to test whether the transactions and operations performed by the<br>
end-users which are related to the database works as expected or not.<br>
Following are the basic conditions that need to be observed for database validations.<br>
● Whether the field is mandatory while allowing NULL values on that field?<br>
● Whether the length of each field is of sufficient size?<br>
● Whether all similar fields have the same names across tables?<br>
● Whether there are any computed fields present in the Database?</p>

### Non-functional testing<br>
<p class="has-line-data" data-line-start="0" data-line-end="4">Non-functional testing in the context of database testing can be categorized into various<br>
categories as required by the business requirements. These can be load testing, Stress Testing,<br>
Security Testing, Usability Testing, and Compatibility Testing, and so on.</p>


### Stored Procedure Testing<br>
#### What is stored procedure<br>
● A stored procedure is a block of SQL statements.<br>
● We can save stored procedures and can be reused multiple times.<br>
● We can also pass parameters to a stored procedure.<br>
#### Advantage<br>
● Reduce network traffic<br>
● Centralize business logic in the database<br>
● Make database more secure</p>


### Checking data integrity and consistency<br>
Following checks are important<br>

- Whether the data is logically well organized?<br>
- Whether the data stored in the tables is correct and as per the business requirements?<br>
- Whether there are any unnecessary data present in the application under test?<br>
- Whether the data has been stored as per as the requirement with respect to data which<br>
has been updated from the user interface?<br>
- Whether the TRIM operations performed on the data before inserting data into the<br>
Database under test?<br>
- Whether the transactions have been performed according to the business requirement<br>
specifications and whether the results are correct or not?<br>
- Whether the data has been properly committed if the transaction has been successfully<br>
executed?<br>
- Whether the data has been rolled backed successfully if the transaction has not been<br>
executed successfully by the end-user?<br>
- Whether the data has been rolled backed if the transaction has not been executed<br>
successfully and multiple heterogeneous databases have been involved in the<br>
transaction in question?<br>
- Whether all the transactions have been executed by using the required design<br>
procedures as specified by the system business requirements?</p>

### Login and User Security Example<br>
The validations of the login and user security credentials need to take into consideration the<br>
following things.</p>
<ol>
<li class="has-line-data" data-line-start="3" data-line-end="8">Whether the application prevents the user from proceeding further in the application in<br>
case of a<br>
● invalid username but valid password<br>
● valid username but invalid password.<br>
● invalid username and invalid password.</li>
<li class="has-line-data" data-line-start="8" data-line-end="10">Whether the user is allowed to perform only those specific operations which are<br>
specified by the business requirements?</li>
<li class="has-line-data" data-line-start="10" data-line-end="11">Whether the data is secured from unauthorized access?</li>
<li class="has-line-data" data-line-start="11" data-line-end="12">Whether there are different user roles created with different permissions?</li>
<li class="has-line-data" data-line-start="12" data-line-end="14">Whether all the users have required levels of access on the specified Database as<br>
required by the business specifications?</li>
<li class="has-line-data" data-line-start="14" data-line-end="17">Check that sensitive data like passwords, credit card numbers are encrypted and not<br>
stored as plain text in Database. It is a good practice to ensure all accounts should have<br>
passwords that are complex and not easily guessed</li>
</ol>


### Here is some database testing checklist you might have used:<br>
- Check if correct data is getting saved in database upon successful page submit<br>
- Check values for columns which are not accepting null values<br>
- Check for data integrity. Data should be stored in single or multiple tables based on<br>
design<br>
- Index names should be given as per the standards e.g.<br>
- IND_&lt;Tablename&gt;<em>&lt;ColumnName&gt;<br>
- Tables should have primary key column<br>
- Null values should not be allowed for Primary key column<br>
- Table columns should have description information available (except for audit columns<br>
like created date, created by etc.)<br>
- For every database add/update operation log should be added<br>
- Required table indexes should be created<br>
- Data should be rolled back in case of failed transactions<br>
- Check if data is committed to database only when the operation is successfully<br>
completed<br>
- Check if input data is not truncated while saving. Field length shown to user on page and<br>
in database schema should be same<br>
- Check numeric fields with minimum, maximum, and float values<br>
- Test stored procedures and triggers with sample input data<br>
- Database name should be given as per the application type i.e. test, UAT, sandbox, live<br>
(though this is not a standard it is helpful for database maintenance)<br>
- Database logical names should be given according to database name (again this is not<br>
standard but helpful for DB maintenance)<br>
- Stored procedures should not be named with prefix “sp</em>”<br>
- Check values for table audit columns (like createddate, createdby, updatedate,<br>
updatedby, isdeleted, deleted date, deleted by etc.) are populated properly<br>
- Check numeric fields with negative values (for both acceptance and non-acceptance)<br>
- Check if radio button and dropdown list options are saved correctly in database<br>
- Check if database fields are designed with correct data type and data length<br>
- Check if all table constraints like Primary key, Foreign key etc. are implemented correctly<br>
- Input field leading and trailing spaces should be truncated before committing data to<br>
database</p>

# Practice

### TABLE

<pre>

For Testing Sample Table:
CREATE TABLE EMPLOYEE
(
EmpCode INT(4),
EmpFName VARCHAR(255),
EmpLName VARCHAR(255),
Job VARCHAR(255),
Manager CHAR(4),
HireDate DATE,
Salary INT(6),
Commission INT(6),
DEPTCODE INT(2)
);
INSERT INTO EMPLOYEE
VALUES (9369, 'TONY', 'STARK', 'SOFTWARE ENGINEER', 7902, '1980-12-17', 2800,0,20),
(9499, 'TIM', 'ADOLF', 'SALESMAN', 7698, '1981-02-20', 1600, 300,30),
(9566, 'KIM', 'JARVIS', 'MANAGER', 7839, '1981-04-02', 3570,0,20),
(9654, 'SAM', 'MILES', 'SALESMAN', 7698, '1981-09-28', 1250, 1400, 30),
(9782, 'KEVIN', 'HILL', 'MANAGER', 7839, '1981-06-09', 2940,0,10),
(9788, 'CONNIE', 'SMITH', 'ANALYST', 7566, '1982-12-09', 3000,0,20),
(9839, 'ALFRED', 'KINSLEY', 'PRESIDENT', 7566, '1981-11-17', 5000,0, 10),
(9844, 'PAUL', 'TIMOTHY', 'SALESMAN', 7698, '1981-09-08', 1500,0,30),
(9876, 'JOHN', 'ASGHAR', 'SOFTWARE ENGINEER', 7788, '1983-01-12',3100,0,20),
(9900, 'ROSE', 'SUMMERS', 'TECHNICAL LEAD', 7698, '1981-12-03', 2950,0, 20),
(9902, 'ANDREW', 'FAULKNER', 'ANAYLYST', 7566, '1981-12-03', 3000,0, 10),
(9934, 'KAREN', 'MATTHEWS', 'SOFTWARE ENGINEER', 7782, '1982-01-23', 3300,0,20),
(9591, 'WENDY', 'SHAWN', 'SALESMAN', 7698, '1981-02-22', 500,0,30),
(9698, 'BELLA', 'SWAN', 'MANAGER', 7839, '1981-05-01', 3420, 0,30),
(9777, 'MADII', 'HIMBURY', 'ANALYST', 7839, '1981-05-01', 2000, 200, NULL),
(9860, 'ATHENA', 'WILSON', 'ANALYST', 7839, '1992-06-21', 7000, 100, 50),
(9861, 'JENNIFER', 'HUETTE', 'ANALYST', 7839, '1996-07-01', 5000, 100, 50);


CREATE TABLE Persons (
ID int NOT NULL,
LastName varchar(255) NOT NULL,
FirstName varchar(255),
Age int,
PRIMARY KEY (ID)
);
FOREIGN KEY Constraint
CREATE TABLE Persons (
ID int NOT NULL,
LastName varchar(255) NOT NULL,
FirstName varchar(255),
Age int,
PRIMARY KEY (ID)
);
CREATE TABLE Orders (
OrderID int NOT NULL,
OrderNumber int NOT NULL,
PersonID int,
PRIMARY KEY (OrderID),
FOREIGN KEY (PersonID) REFERENCES Persons(ID)
);
	
</pre>

### QUERY

<pre>
CREATE DATABASE Statement
The CREATE DATABASE statement is used to create a new SQL
database.
Syntax: CREATE DATABASE databasename;
DROP DATABASE Statement
The DROP DATABASE statement is used to drop an existing SQL
database.
Syntax: DROP DATABASE databasename;
CREATE TABLE Statement
The CREATE TABLE statement is used to create a new table in a
database.
CREATE DATABASE Statement
The CREATE DATABASE statement is used to create a new SQL
database.
Syntax: CREATE DATABASE databasename;
DROP DATABASE Statement
The DROP DATABASE statement is used to drop an existing SQL
database.
Syntax: DROP DATABASE databasename;
CREATE TABLE Statement
The CREATE TABLE statement is used to create a new table in a
database.
INSERT INTO Statement
The INSERT INTO statement is used to insert new records in a
table.
Syntax: INSERT INTO table_name (column1, column2, column3,
...) VALUES (value1, value2, value3, ...);
Sample: INSERT INTO Customers (CustomerName, ContactName,
Address, City, PostalCode, Country) VALUES ('Cardinal',
'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006',
'Norway');
SELECT Statement
The SELECT statement is used to select data from a database.
Syntax: SELECT column1, column2, … FROM table_name;
Sample: SELECT * FROM Customers;
WHERE Clause
The WHERE clause is used to filter records.
WHERE Syntax: SELECT column1, column2, … FROM table_name
WHERE condition;
MySQL AND and OR Operators
The WHERE clause can be combined with AND, OR operators.
The AND and OR operators are used to filter records based on
more than one condition:
● The AND operator displays a record if all the conditions
separated by AND are TRUE.
● The OR operator displays a record if any of the conditions
separated by OR is TRUE.
AND Syntax: SELECT column1, column2, … FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
OR Syntax: SELECT column1, column2, … FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
ORDER BY Keyword
The ORDER BY keyword is used to sort the result-set in ascending
or descending order.
The ORDER BY keyword sorts the records in ascending order by
default. To sort the records in descending order, use the DESC
keyword.
ORDER BY Syntax: SELECT column1, column2, … FROM
table_name ORDER BY column1, column2, ... ASC|DESC;
UPDATE Statement
The UPDATE statement is used to modify the existing records in a
table.
UPDATE Syntax: UPDATE table_name SET column1 = value1,
column2 = value2, … WHERE condition;
Sample: UPDATE Customers SET ContactName = 'Alfred
Schmidt', City = 'Frankfurt' WHERE CustomerID = 1;
DELETE Statement
The DELETE statement is used to delete existing records in a
table.
DELETE Syntax: DELETE FROM table_name WHERE condition;
Example: DELETE FROM Customers WHERE
CustomerName='Alfreds Futterkiste';
LIMIT Clause
The LIMIT clause is used to specify the number of records to
return.
LIMIT Syntax: SELECT column_name(s) FROM table_name WHERE
condition LIMIT number;
Example: SELECT * FROM Customers LIMIT 3;
LIKE Operator
The LIKE operator is used in a WHERE clause to search for a
specified pattern in a column.
Syntax: SELECT column1, column2, … FROM table_name WHERE
columnN LIKE pattern;
LIKE Operator Description
WHERE
CustomerName
LIKE 'a%'
Finds any values that start with "a"
WHERE
CustomerName
LIKE '%a'
Finds any values that end with "a"
WHERE
CustomerName
LIKE '%or%'
Finds any values that have "or" in any
position
WHERE
CustomerName
LIKE '_r%'
Finds any values that have "r" in the
second position
WHERE
CustomerName
LIKE 'a_%'
Finds any values that start with "a" and
are at least 2 characters in length
WHERE
CustomerName
LIKE 'a__%'
Finds any values that start with "a" and
are at least 3 characters in length
WHERE
ContactName LIKE
'a%o'
Finds any values that start with "a" and
ends with "o"
BETWEEN Operator
The BETWEEN operator selects values within a given range. The
values can be numbers, text, or dates.
Syntax: SELECT column_name(s) FROM table_name WHERE
column_name BETWEEN value1 AND value2;
Example: SELECT * FROM Products WHERE Price BETWEEN 10
AND 20
</pre>
