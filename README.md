# EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands


# DATE:


# AIM:

To create a manager database and execute DML queries using SQL.


# DML(Data Manupulation Language)


The SQL commands that deal with the manipulation of data present in the database belong to DML or Data

Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that

controls access to data and to the database. Basically, DCL statements are grouped with DML statements.


# List of DML commands:


INSERT: It is used to insert data into a table.


UPDATE: It is used to update existing data within a table.


DELETE: It is used to delete records from a database table.


# Create the table as given below:
```

create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```

# insert the following values into the table

```
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

# Q1) Update all the records of manager table by increasing 10% of their salary as bonus.


# QUERY:
```
SQL> update manager set salary = (salary*0.10)+ salary ;
```

# OUTPUT:


<img width="622" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/ff9576d8-3bbb-4a1c-9cb7-30e5ad3734e2">


# Q2) Delete the records from manager table where the salary less than 2750.

# QUERY:

```
SQL> delete worker where salary<2750;
```
# OUTPUT:


<img width="623" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/84d0df87-a35f-4664-b0ec-6aca8c0022e2">



# Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


# QUERY:

```
SQL> SELECT
2  ename AS "name",

3  salary * 12 AS "Annual Salary" 

4  FROM

5  manger ;

```
# OUTPUT:

<img width="379" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/674dae99-3c3f-4984-ad14-dcec30197783">


# Q5) List the names of Clerks from emp table.

# QUERY:
```
SQL> select ename from empn where designation='clerk' ;

```
# OUTPUT:

<img width="337" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/df0633ba-f55c-4774-b553-173e224ad9bb">


# Q6) List the names of employee who are not Managers.

# QUERY:

```
SQL> select ename from empn where designation !='manager' ;

```

# OUTPUT:


<img width="295" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/b8dc1f41-6812-4766-8a99-446a523e86a8">



# Q7) List the names of employees not eligible for commission.

# QUERY:
```
SQL> select ename from empn where commission=0;

```

# OUTPUT:


<img width="275" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/097b4782-ae25-4931-af81-e1df1f0d6f64">




# Q8) List employees whose name either start or end with ‘s’.

# QUERY:
```
SQL> select ename from empn where ename LIKE 'S%' OR ename LIKE '%s';

```
# OUTPUT:

<img width="278" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/24b10315-f682-4407-a478-9a83f5b934b2">



# Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.

# QUERY:
```
SQL> SELECT ename, designation, deptno, hiredate

2 from empn

3 order by hiredate ASC;


```
# OUTPUT:

<img width="640" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/c5f3b867-e455-4fa6-a7f9-9b9f414fa991">



# Q10) List the Details of Employees who have joined before 30 Sept 81.

# QUERY:
```
SQL> SELECT * FROM empn WHERE hiredate <'30 sep 81';

```
# OUTPUT:

<img width="600" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/c9a4bea4-db4a-4739-b5be-c436386c5001">



# Q11) List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.

# QUERY:
```
SQL> SELECT ename, designation, salary from empn ORDER BY deptno ASC, salary DESC;
```
# OUTPUT:


<img width="451" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/959263c4-cda3-4239-a011-26dafa63b3f9">


# Q12) List the names of employees not belonging to dept no 30,40 & 10

# QUERY:
```
SQL> SELECT ename from empn WHERE deptno NOT IN (30, 40, 10);

```

# OUTPUT:


<img width="244" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/15501d43-2de3-43be-9694-2b11403049c1">




# Q13) Find number of rows in the table EMP


# QUERY:
```
SQL> SELECT COUNT(*) AS num_rows FROM empn;

```
# OUTPUT:


<img width="138" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/378d6d3f-f013-40d9-a420-c9fe1aab0164">


# Q14) Find maximum, minimum and average salary in EMP table.

# QUERY:

<img width="622" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/4e51d334-b5b9-419c-8de4-a164bb169aef">

# OUTPUT:

<img width="320" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/9b08ed54-8647-44f6-8b9a-5f964d563b93">



# Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

# QUERY:


<img width="607" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/8fa00bc5-e856-4b32-8250-a51641947a97">


# OUTPUT:

<img width="325" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/211a9877-2d0f-40a0-9b9a-b755197f3fe9">

