## SQL

 @author Heeren

 ### Topics Covered 
---
- Databases
- Query Language Classification
  - Data Definition Language (DDL)
  - Data Manipulation Language (DML)
- Datatypes in databases
- Database Operations
- Table Operations
  - CREATE Queries
  - INSERT Queries
  - UPDATE Queries
  - DELETE Queries
- Alter Table
- Constraints
  - Primary Key
  - Unique Key
  - Not Null
- Difference between Primary Key and Unique Key
- Use of >, <, <=, >=, =, != in conditions
- Keywords use in WHERE Clause
  - IN
  - BETWEEN
  - LIKE
  - ORDER BY
- Aliasing
- Joins
- LEFT, RIGHT, Inner Join, FULL OUTER JOIN
- Useful SQL Queries
- Getting Top 3 Candidates based on Highest Marks
- Getting Maximum Marks from Student table
- Details of Candidates with Maximum Marks
- Record of Candidate with Second Highest Marks
- Group By
--- 

**Databases**

- **MySQL**
- **Oracle**
- **PostgreSQL**
- **MS SQL**

### Query Language Classification

- **Data Definition Language (DDL)**
  - Create table or database or drop table or database and alter structure of tables
- **Data Manipulation Language (DML)**
  - Use to manipulate data such as inserting or updating or deleting data in database tables.

### Datatypes

- INTEGER, BIGINT, SMALLINT
- FLOAT
- varchar(20)
- char
- BOOLEAN

### All Queries

### To Start Shell
```sql
mysql -u root -p 
Enter password.
```

**Database Operations**
```sql
CREATE SCHEMA School;  -- CREATE DATABASE SCHOOL;
DROP SCHEMA School;
USE School;
SHOW DATABASES;
```
**Table Operations**
```sql
-- Create Table -
CREATE TABLE STUDENT(id int, name VARCHAR(10), address VARCHAR(10));
-- OR
CREATE TABLE student(id INT, name VARCHAR(20), contactNumber VARCHAR(15));

-- DROP TABLE -
DROP TABLE STUDENT;

-- Describe table structure -
DESCRIBE STUDENT;
-- OR
DESC STUDENT;

-- Count Number of Records - 
SELECT COUNT(*) FROM EMP;
 
-- Insert Data - 
INSERT INTO STUDENT VALUES(1, "John", "Warsaw");
INSERT INTO STUDENT (NAME, ADDRESS) VALUES("John", "Warsaw");

-- Insert multiple records - 
INSERT INTO STUDENT VALUES
    (23, "Tom", '2345678866'),
    (12, "KK", '1111678866'),
    (56, "Heeren", '56788544443');

-- Select Data -
SELECT * FROM STUDENT;

-- Delete Data -
DELETE FROM STUDENT WHERE ID = 3;

-- Update Data -
UPDATE STUDENT SET LNAME = "sharma" WHERE ID = 3;
UPDATE STUDENT SET FNAME = "AMIT", LNAME = "SHARMA" WHERE ID = 5;
```
**Alter Table**
```sql
-- ADD COLUMN -
ALTER TABLE EMP ADD SALARY MEDIUMINT NOT NULL;

-- DROP COLUMN -
ALTER TABLE EMP DROP COLUMN SALARY;

-- MODIFY COLUMN -
ALTER TABLE EMP MODIFY COLUMN SALARY INT DEFAULT 10000;
ALTER TABLE EMPLOYEE RENAME TO employee;
```

**Constraints**
```sql
-- Primary Key - Use only on id column
-- Unique Key - Value must be unique
CREATE TABLE teacher(id int primary key, name varchar(20), age int, contactno varchar(20) unique key);
ALTER TABLE student MODIFY COLUMN id INT PRIMARY KEY;
-- Not Null - If we don't want to have any attribute value as NULL.
```

**Conditions and Keywords in WHERE Clause**
- Use of >, <, <=, >=, =, != in conditions.
- Difference between Primary Key and Unique Key
  - One column can only be a primary key but we can have multiple columns with unique key constraint.

**Select Query**
```sql
SELECT * FROM STUDENT;
SELECT * FROM STUDENT WHERE id = 12 OR id = 33;
SELECT * FROM STUDENT WHERE id >= 12 AND id <= 33;
SELECT * FROM STUDENT WHERE id != 12;
```
**Keywords use in WHERE Clause**
```sql
-- IN
UPDATE STUDENT SET GENDER = 'male' WHERE id IN (18, 23, 56, 88);

-- OR	
UPDATE STUDENT SET GENDER = 'f' WHERE id = 12 OR id = 33;

-- BETWEEN
SELECT * FROM STUDENT WHERE id BETWEEN 18 AND 33;

-- LIKE
SELECT * FROM STUDENT WHERE name LIKE 'T%';
SELECT * FROM STUDENT WHERE name LIKE '_o%'; -- All names have 'o' as the second character
SELECT * FROM STUDENT WHERE name LIKE '__e%'; -- All names have 'e' as the third character
SELECT * FROM STUDENT WHERE name LIKE '%A%'; -- All names that contain 'A' anywhere in the string

-- ORDER BY
-- Arrange elements in ascending or descending order.

SELECT * FROM STUDENT ORDER BY name ASC; -- Ascending order
SELECT * FROM STUDENT ORDER BY name; -- Default is ascending
SELECT * FROM STUDENT ORDER BY id DESC; -- Descending order
SELECT * FROM STUDENT ORDER BY name DESC;

-- Select Query with Specific Fields
SELECT id, name FROM STUDENT;
SELECT student.id, student.name FROM STUDENT;
```
**Aliasing**    
Defining alternative names for tables or columns    
```sql
SELECT stud.id, stud.name FROM STUDENT AS stud;
SELECT stud.id AS student_id, stud.name AS student_name FROM STUDENT AS stud;
```
**Joins**
```sql
-- Inner Join

SELECT stud.id AS student_ID, stud.name AS student_name, sub.name AS subject_name 
FROM STUDENT AS stud, major_subject AS sub 
WHERE stud.subject_id = sub.id;
--OR
SELECT stud.id AS student_ID, stud.name AS student_name, sub.name AS subject_name 
FROM STUDENT AS stud 
INNER JOIN major_subject AS sub 
ON stud.subject_id = sub.id;

```
**USEFUL SQL QUERIES**
```sql
-- Getting Top 3 Candidates based on Highest Marks
SELECT * FROM STUDENT ORDER BY marks DESC LIMIT 3;

-- Getting Maximum Marks from Student table
SELECT MAX(marks) FROM STUDENT;

-- Details of Candidates with Maximum Marks
SELECT * FROM STUDENT WHERE marks = (SELECT MAX(marks) FROM STUDENT);

-- Record of Candidate with Second Highest Marks
SELECT * FROM STUDENT WHERE marks < (SELECT MAX(marks) FROM STUDENT) ORDER BY marks DESC LIMIT 1;

-- Joins (LEFT, RIGHT, FULL OUTER JOIN)
Left Outer Join

SELECT student.id, student.name, major_subject.name FROM STUDENT 
LEFT OUTER JOIN major_subject ON student.subject_id = major_subject.id;

-- Right Outer Join
SELECT student.id, student.name, major_subject.name FROM STUDENT 
RIGHT OUTER JOIN major_subject ON student.subject_id = major_subject.id;

-- Full Outer Join
SELECT student.id, student.name, major_subject.name FROM STUDENT 
FULL OUTER JOIN major_subject ON student.subject_id = major_subject.id;

-- Group By
SELECT MAX(marks) FROM STUDENT GROUP BY gender; 

-- Get the maximum marks from male and female candidates in class.
SELECT * FROM STUDENT WHERE marks IN (SELECT MAX(marks) FROM STUDENT GROUP BY gender);
```



