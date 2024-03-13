# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE:06.03.2024
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
```
create table student(reg_no int,name varchar(20),age int,address varchar(255),ph_no int);
```
### OUTPUT:
![Screenshot 2024-03-13 105956](https://github.com/Dhanudhanaraj/DBMS/assets/119218812/358e5550-9731-4b7c-84e3-08735bc50107)

### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
alter table student add department varchar(20);
```
### OUTPUT:
![Screenshot 2024-03-13 110017](https://github.com/Dhanudhanaraj/DBMS/assets/119218812/cd862501-bda1-4f53-8b1c-d32d7d0c4a8d)

### 3) Rename the student table to mystudent

### SQL QUERY: 
```
alter table student rename to mystudent1;
```
### OUTPUT:
![Screenshot 2024-03-13 110017](https://github.com/Dhanudhanaraj/DBMS/assets/119218812/03389f22-d94e-4bae-966c-1ba1db316689)


### 4) Drop the mystudent table
 
### SQL QUERY: 
```
drop table mystudent1;
```

### OUTPUT:
![Screenshot 2024-03-13 110034](https://github.com/Dhanudhanaraj/DBMS/assets/119218812/124136ca-aff8-4f30-bf13-ab050a90a552)


## Result:
Thus the basic DDL commands in SQL are executed. 


