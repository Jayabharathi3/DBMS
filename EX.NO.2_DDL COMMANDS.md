# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE : 06.03.2024
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:

### 1) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```SQL
 create table student(RegisterNumber int,Name varchar(100),Age int,Address varchar(250),PhoneNumber int) ;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/3b2ea28e-b13f-44f6-aede-bf9c1eda44da)

### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
 alter table student add dept varchar(20);
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/64c4a805-220f-4d16-b47e-439959808b5b)


### 3) Rename the student table to mystudent

### SQL QUERY: 
```SQL
alter table student rename to student1;
```
### OUTPUT:

![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/84cd3e30-6347-4a6e-97b8-20d2ea033dd6)

### 4) Drop the mystudent table
### SQL QUERY: 

```SQL
 drop table student1;

```
### OUTPUT:

![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/5f948625-f601-407a-b9c0-7833e51a999c)



## Result:
         Thus the basic DDL commands in SQL are executed. 


