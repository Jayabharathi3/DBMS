# EXP NO 10: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 
## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### 1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 
```sql
CREATE TABLE EMPLOYEE (
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(255),
    employee_salary DECIMAL(10, 2)
);

INSERT INTO EMPLOYEE (employee_id, employee_name, employee_salary)
VALUES (1, 'Kayal', 50000.00);

INSERT INTO EMPLOYEE (employee_id, employee_name, employee_salary)
VALUES (2, 'Dolly', 60000.00);
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/95ffffbd-5fdd-4b48-bbba-bda181baed55)

### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
```sql
CREATE SYNONYM S1 FOR EMPLOYEE;
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/11e1f84f-cf06-44ae-8e62-9b2117dbf06f)


### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```sql
SELECT * FROM S1;
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/e6bbb905-dc8e-4571-961c-b6d7aad2d8e2)


### 4) Drop the synonym.

### SQL QUERY: 
```sql
DROP SYNONYM S1;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/16a59adf-afc2-4d3e-96dd-dc41d0a158e5)


### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
```sql
CREATE TABLE SUPPLIER (
    supplier_id INT PRIMARY KEY,
    supplier_name VARCHAR(255)
);

CREATE SEQUENCE S2;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/2599a90e-a818-4cc0-84f6-30ea6abd0a37)


### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```sql
INSERT INTO SUPPLIER (supplier_id, supplier_name)
VALUES (S2.NEXTVAL, 'AB Suppliers');

INSERT INTO SUPPLIER (supplier_id, supplier_name)
VALUES (S2.NEXTVAL, 'CD Suppliers');
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/5c60b6a6-f31e-492c-83d9-719c84240715)

### 7) Drop the sequence

### SQL QUERY: 
```sql
DROP SEQUENCE S2;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/6d0f3ee4-22dc-411a-a618-b1945ed53bfb)

## RESULT :
Thus the sequence and synonym created and used in SQL.
