# EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands


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

create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));


# insert the following values into the table


insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');


# Q1) Update all the records of manager table by increasing 10% of their salary as bonus.


# QUERY:

SQL> update manager set salary = (salary*0.10)+ salary ;


# OUTPUT:


<img width="622" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/ff9576d8-3bbb-4a1c-9cb7-30e5ad3734e2">


# Q2) Delete the records from manager table where the salary less than 2750.

# QUERY:


SQL> delete worker where salary<2750;

# OUTPUT:


<img width="623" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/84d0df87-a35f-4664-b0ec-6aca8c0022e2">



# Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


# QUERY:


SQL> SELECT
2  ename AS "name",

3  salary * 12 AS "Annual Salary" 

4  FROM

5  manger ;


# OUTPUT:

<img width="379" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/674dae99-3c3f-4984-ad14-dcec30197783">


# Q5) List the names of Clerks from emp table.

# QUERY:

<img width="572" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/502e846b-2b1d-42eb-925b-e5cd4ef9e2a8">


# OUTPUT:

<img width="337" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/df0633ba-f55c-4774-b553-173e224ad9bb">


# Q6) List the names of employee who are not Managers.

# QUERY:


<img width="610" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/7403ec28-2fc4-4ccc-9dfb-fdc657a76bf2">



# OUTPUT:


<img width="295" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/b8dc1f41-6812-4766-8a99-446a523e86a8">



# Q7) List the names of employees not eligible for commission.

# QUERY:

<img width="500" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/32f01648-532b-4767-a05b-4048359bb484">



# OUTPUT:


<img width="275" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/097b4782-ae25-4931-af81-e1df1f0d6f64">




# Q8) List employees whose name either start or end with ‘s’.

# QUERY:

<img width="629" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/af7a394a-df47-4031-98d0-3e96719f2ee3">


# OUTPUT:

<img width="278" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/24b10315-f682-4407-a478-9a83f5b934b2">



# Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.

# QUERY:

<img width="445" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/f197c4ce-0a9c-4721-85f6-154919fc0c3e">



# OUTPUT:

<img width="640" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/c5f3b867-e455-4fa6-a7f9-9b9f414fa991">



# Q10) List the Details of Employees who have joined before 30 Sept 81.

# QUERY:

<img width="488" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/de7c1c02-b38f-4e31-bbd1-67ee203c6fbf">


# OUTPUT:

<img width="600" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/c9a4bea4-db4a-4739-b5be-c436386c5001">



# Q11) List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.

# QUERY:

<img width="646" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/a26c770f-9315-4046-8d2d-1cf530c1a742">

# OUTPUT:


<img width="451" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/959263c4-cda3-4239-a011-26dafa63b3f9">


# Q12) List the names of employees not belonging to dept no 30,40 & 10

# QUERY:

<img width="568" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/85164d97-acf5-4917-b845-fec1f7d1457c">



# OUTPUT:


<img width="244" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/15501d43-2de3-43be-9694-2b11403049c1">




# Q13) Find number of rows in the table EMP


# QUERY:

<img width="389" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343892/ed939174-ac8f-4541-b6e1-6e406913974d">


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
