# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
```SQL
update manager 
set salary = salary + (salary * 10/100)
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/5c0f13b1-4ecd-4311-905f-233d68e81415)


### Q2) Delete the records from manager table where the salary less than 2750.

### QUERY:
```SQL
select ename as "Name",salary*12 as annualsalary from manager;
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/9db38689-f319-4977-8f25-e49d3312de74)




### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)

### QUERY:
```SQL
select ename as "Name",salary*12 as annualsalary from manager;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/1cb51c63-b1de-4984-9819-52642c36e92e)


### Q4)	List the names of Clerks from emp table.

### QUERY:
```SQL
select ename from manager where designation = 'clerk';
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/e95a1091-6ffe-4fda-8ca7-20c1c2007e26)


### Q5)	List the names of employee who are not Managers.
### QUERY:
```SQL
select ename from manager where designation != 'manager';
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/1fe89e94-1079-496d-80b6-49af89de4e76)

### Q6)	List the names of employees not eligible for commission.

### QUERY:
```sql
select ename from manager where commission = 0;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/08ac0ddc-a034-4511-9d39-72a170e9cc60)


### Q7)	List employees whose name either start or end with ‘s’.

### QUERY:
```SQL
select ename from manager where ename like 'S%' or ename like '%S';
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/cb006aa6-92b6-41cb-b358-7a2a9d02b5f5)


### Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.

### QUERY:
```sql
select Hiredate,ename,designation,deptno from manager order by Hiredate;
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/4c13db6b-64f8-4304-910b-c76463060635)


### Q9) List the Details of Employees who have joined before 30 Sept 81.

### QUERY:
```sql
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/7b7dfd72-6b1e-4f62-b7eb-efd59a6e0e9b)


### Q10)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.

### QUERY:
```sql
select ename,deptno,salary from manager order by deptno,salary desc;
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/55e9d8f6-8128-485f-86ee-14f3ce3eaeff)



### Q11) List the names of employees not belonging to dept no 30,40 & 10
### QUERY:
```sql
select ename from manager where deptno != 30 and deptno != 40 and deptno != 10;
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/d634eecc-850b-4781-aea6-7d0b1ce869fc)

### Q12) Find number of rows in the table EMP

### QUERY:
```sql

select count (*) as count_ename from manager;
```
### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/4a7dbe03-21bc-4538-a49f-437a4b87213c)


### Q13) Find maximum, minimum and average salary in EMP table.

### QUERY:
```sql
select avg(salary) as tot_salary from manager;
select min(salary) as min_salary from manager;
select max(salary) as max_salary from manager;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/2623c80c-c9b0-455f-96aa-242a14d42ae0) ![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/2623c80c-c9b0-455f-96aa-242a14d42ae0) ![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/43702d73-3a94-4de3-bf86-8a33f9b329bc)



### Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
```sql
select designation,enumber from manager order by designation ,enumber desc;
```

### OUTPUT:
![image](https://github.com/Jayabharathi3/DBMS/assets/120367796/c1dfa7de-bc22-44bb-9a74-8efdb4cef1ce)


## RESULT :
Thus the basic DML commands are executed.
