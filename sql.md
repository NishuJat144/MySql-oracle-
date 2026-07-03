\# SQL DAY-2



\-> It is discovered by EF CODD



\# Rules given by EF Codd

1\. Single DATA stored in a single cell .



2\. We can store everything in tables => metadata also.



3\. MULTIPLE TABLE MEIN RELATIONSHIP HOTA HAI KEY ATTRIBUTES KA USE KARKE .



4\. Data should be store will be validated by datatype and constraints.



\# DATA TYPE



1.char(size) => limit:- 2000 character => Always use single quote '' .

&#x20;

=>  It is also known as Fixed Length Memory Location.





2.varchar => limit 2000

=> Internally varchar uses varchar2 .

3.varchar2 => limit 4000 ==> They are also known as Variable length memory location.



4.Date => syntax :-> col date

&#x20;

&#x20; Date Format :-> 'DD-MON-YY' \& 'DD-MON-YYYY'



5\. Number => col number(Precision , scale) :-

&#x20;

=> Precision :-> Integer values => mandatory parameter => Range(0 to 38)



=> scale => Double values => optional parameter => Range(-84 to 127)





\*6 LARGE OBJECT :-



Large Object is mainly used to store large number of data or values.



It is classified into two types :-

1\. CLOB => It stands for character large object , CLOB is mainly used to store large number of characters .

&#x20;  MAX SIZE => 4 GB -> It can be extended up to 1TB .



Syntax :- > columnname CLOB ;



2\. BLOB => It stands for Binary large object , It is mainly used to store binary values of images , videos , audios, Binary files.

&#x20;   Syntax :- > Col BLOB

&#x20;   Size - > 4GB   -> it can be extended up to 1TB .



\# Constraints :->



=> Rules and Regulations that we need to follow in order to insert a data into a particular column.



1\. UNIQUE ,  2.Not Null , 3. Check , 4. Primary Key , 5. Foreign Key





\#1. UNIQUE :-> It is mainly used to avoid duplicate values into a particular column.



=> Syntax :-> col DT UNIQUE



\# NULL CHARCTERISTIC :-



1\. We cannot compare null with any operator. Ex :-> 5 = null



2\. We cannot perform any mathematical operation with null values . Ex :-> 5 + null = null (it return null as a output).



\#2. NOT NULL :-> It is a Constraint used to avoid null values into a particular column.



\#3. CHECK :-> It is a Constraint mainly used to provide extra Validation(conditions) for a Column.



Syntax :-> colname DT CHECK(CONDITION)

Ex :-> AGE NUMBER(2) CHECK(age >=18)



\#4. Primary Key :->

\# CHARACTERISTIC:->



1\. It should be Unique(avoid duplicate values).It follows Unique Constraint.

2\. Not Null (avoid null values), There exist only one primary key in a Table .

3\. It is mainly used to identify the records uniquely in the table.



Syntax :-> colname DT PRIMARY KEY



Example:->



Makeup Table

|MID|MNAME|BRAND|PRICE|
|-|-|-|-|
|M1|PRIMER|LAKME|600|
|M2|FOUNDATION|BIRLA|1000|
|M3|POWDER|DERMICOOL|20|
|M4|HAIR OIL|BAJAJ|20|
|M5|FACE WASH|GARNIER|170|
|M6|EYE LINER|LAKME|500|





\#5. Foreign Key: ->

=> It is mainly used to establish a relationship between multiple tables.

=> It can be not null or not Unique(Duplicate Values can insert) .

=> There will be Multiple Foreign key exist in the table meant that we can take reference of n number of foreign key in the table.



PHONE TABLE

|PID|PNAME|PRICE|
|-|-|-|
|P1|PIXEL|40000|
|P2|SAMSUNG|100000|
|P3|VIVO|20000|
|P4|IPHONE|100000|
|P5|NOKIA|800|





STUDENT TABLE

|SID|SNAME|MID|PID|
|-|-|-|-|
|S1|RENU|NULL|P3|
|S2|VANSHIKA|M5|P3|
|S3|AARTI|M5|P2|
|S4|KUMKUM|M6|NULL|
|S5|DISHA|M5|P2|
|S6|SAHIL|M4|P5|
|S7|VARINDER|M5|NULL|









\*#. These two key attributes(Constraints) are used to create the relationship between two or more than two tables.



\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*



\# SQL Statements

1. DQL => Data Query Language is used to fetch the data from database.

=> SELECT , PROJECTION , SELECTION , JOINS



\--> SELECT => It is mainly used to fetch the data and display the data on the output screen(console).

\--> PROJECTION => It is mainly used to fetch(retrieve) the data by selecting only the columns .





\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

=> ARGUMENTS PASSING WITH SELECT CLAUSE :-> \* / \[DISTINCT] COLNAME / EXPRESSION \[ALIAS]



=> SELECT :-> USED TO FETCH ALL THE DATA FROM THE DATABASE AND PRINT THE DATA ON THE OUTPUT SCREEN/CONSOLE .





\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*



=> DISTINCT :-> USED TO AVOID DUPLICATE VALUES .

\# DISTINCT COLUMN NAME

=> HAMESHA EK DISTINCT USE KARTE HAI .

=> DISTINCT GIVE PREFERENCE TO THE FIRST ARGUMENT(PARAMETER).



====> CHARACTERISTICS OF DISTINCT

1.=> Distinct is always pass as a first argument inside select clause.

2.=> If we pass Multiple columns inside distinct it will check combination of values. If combination is matching it will consider as duplicate      records but combination is not matching then it's a unique record.



\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*



\# EXPRESSION AND ALIAS.



=> ANY MATHEMATICAL OPERATION WHICH RETURN A RESULT IS CALLED EXPRESSION.

&#x20; EX :-> 5 + 5 = 10

&#x20;        5 \* 5 = 25

&#x20;        5/5  = 1

&#x20;       SAL + 200



\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

WAY OF EXECUTION OF SQL QUERY :-> BOTTOM TO TOP





\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\--> SELECTION => It is mainly used to fetch (retrieve) the data by selecting both rows and columns.

\--> JOINS => It is mainly used to fetch the data from Multiple Tables simultaneously(ek-saath).









2\. DDL :-> DATA DEFINITION LANGUAGE , It mainly deals with the table structure.

=> CREATE , RENAME ,ALTER , TRUNCATE , DROP



3\. DML :-> Data Manipulation Language , it is to modify the data in a table.

=> insert , update , delete => these all are transactions , they cannot save automatically.



4\. TCL :-> Transaction Control Language , used for transaction is done or not.

=> Commit (Permanent save transaction), SavePoint(Temporary save transactions) , Rollback (delete transactions)



5.DCL :-> Data Control Language => It controlled access(Permissions) of data.

=> Grant , Revoke



\# PASWORD CONFIGURATION

=> Connect (conn)



\# questions :->

1. WAQTD NAME OF ALL THE EMPOLOYEE.



\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

