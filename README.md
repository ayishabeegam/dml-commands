# dml-commands
CREATE DATABASE ASSIGNMENT3;
USE ASSIGNMENT3;
CREATE TABLE MANAGER (Manager_id INT PRIMARY KEY, First_name varchar(30), Last_name varchar(30), DOB DATE, Age INT, Gender varchar(1) check (Gender in ('F','M','O')),Department varchar(30) not null, Salary INT NOT NULL);

#1. INSERT 10 ROWS
INSERT INTO MANAGER VALUES(1,'Aaliya','fazy','1990-02-01',35,'M','IT',25000);
INSERT INTO MANAGER VALUES(2,'AFIYA','sonu','1989-02-01',36,'F','HR',12000);
INSERT INTO MANAGER VALUES(3,'nyna','fasil','1991-02-01',34,'O','HR',18000);
INSERT INTO MANAGER VALUES(4,'Aysha','bgm','1992-02-01',33,'M','IT',35000);
INSERT INTO MANAGER VALUES(5,'nyha','fazil','1993-02-01',32,'F','IT',24000);
INSERT INTO MANAGER VALUES(6,'shahana','salim','1994-02-01',31,'M','ADMIN',34000);
INSERT INTO MANAGER VALUES(7,'prithvi','suku','1988-02-01',37,'F','MANAGEMENT',21000);
INSERT INTO MANAGER VALUES(8,'asif','ali','1987-02-01',38,'O','IT',28000);
INSERT INTO MANAGER VALUES(9,'parvathy','thiruvoth','1986-02-01',39,'F','SOCIAL WORK',8000);
INSERT INTO MANAGER VALUES(10,'Anamika','menon','1995-02-01',30,'F','SOCIAL WORK',9000);

#WRITE A QUERY THAT RETRIEVES THE NAME AND DATE OF BIRTH OF MNAGER WITH MANAGER_ID 1
SELECT First_name,DOB FROM MANAGER WHERE Manager_id=1;

#3. write a query to display the annual income of all managers
SELECT First_name,Salary*12 as 'annual income' FROM MANAGER;

#4.write a query to display records of all manager except aaliya
SELECT * FROM MANAGER WHERE First_name != 'Aaliya';

#5 write a query to display details of manager whose department is IT and earns more than 25000 per month.
SELECT * FROM MANAGER WHERE Department='IT' AND Salary>25000;

#6.write a query to display details of managers whose salary is between 10000 and 35000
SELECT * FROM MANAGER WHERE SALARY BETWEEN 10000 AND 35000;
