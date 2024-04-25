## SQL

 @author Heeren

 **Topics Covered**    
---
1.Lambda Expression   
2.Functional Interface  
3.Default Method   
4.Static methods   
5.Consumer and supplier   
6.Predicates   
7.Functions   
8.Date time api   
9.Optional   
10.Stream api   

--- 

**Databases**

- **MySQL**
- **Oracle**
- **PostgreSQL**
- **MS SQL**

## Query Language Classification

- **Data Definition Language (DDL)**
  - Create table or database or drop table or database and alter structure of tables
- **Data Manipulation Language (DML)**
  - Use to manipulate data such as inserting or updating or deleting data in database tables.

## Datatypes

- `int`
- `varchar(20)`
- `char`

## All Queries

### To Start Shell

```sql
mysql -u root -p 

Certainly! Here's the content formatted with Markdown tags for easy copy-pasting into your GitHub Markdown (.md) file:

markdown
Copy code
# Databases

- **MySQL**
- **Oracle**
- **PostgreSQL**
- **MS SQL**

## Query Language Classification

- **Data Definition Language (DDL)**
  - Create table or database or drop table or database and alter structure of tables
- **Data Manipulation Language (DML)**
  - Use to manipulate data such as inserting or updating or deleting data in database tables.

## Datatypes

- `int`
- `varchar(20)`
- `char`

## All Queries

### To Start Shell

```sql
mysql -u root -p 
Enter password.

**Database Operations**
CREATE SCHEMA School;  -- CREATE DATABASE SCHOOL;
DROP SCHEMA School;
USE School;
SHOW DATABASES;
**Table Operations**
CREATE TABLE STUDENT(id int, name VARCHAR(10), address VARCHAR(10));
-- OR
CREATE TABLE student(id INT, name VARCHAR(20), contactNumber VARCHAR(15));

DROP TABLE STUDENT;

-- Describe table structure
DESCRIBE STUDENT;
-- OR
DESC STUDENT;
Count Number of Records
sql
Copy code
SELECT COUNT(*) FROM EMP; 
Insert Data
sql
Copy code
INSERT INTO STUDENT VALUES(1, "HEERENDRA", "Chandigarh");
INSERT INTO STUDENT (NAME, ADDRESS) VALUES("VINEET", "BANGLORE");

-- Insert multiple records
INSERT INTO STUDENT VALUES
    (23, "Tom", '2345678866'),
    (12, "KK", '1111678866'),
    (56, "Heeren", '56788544443');
Select Data
sql
Copy code
SELECT * FROM STUDENT;
Delete Data
sql
Copy code
DELETE FROM STUDENT WHERE ID = 3;
Update Data
sql
Copy code
UPDATE STUDENT SET LNAME = "sharma" WHERE ID = 3;
UPDATE STUDENT SET FNAME = "AMIT", LNAME = "SHARMA" WHERE ID = 5;
Alter Table
sql
Copy code
ALTER TABLE EMP ADD SALARY MEDIUMINT NOT NULL; -- ADD COLUMN
ALTER TABLE EMP DROP COLUMN SALARY; -- DROP COLUMN
ALTER TABLE EMP MODIFY COLUMN SALARY INT DEFAULT 10000;
ALTER TABLE EMPLOYEE RENAME TO employee;
Constraints
Primary Key
Use only on id column
sql
Copy code
CREATE TABLE teacher(id int primary key, name varchar(20), age int, contactno varchar(20) unique key); 
Unique Key
Value must be unique
sql
Copy code
ALTER TABLE student MODIFY COLUMN id INT PRIMARY KEY;
Not Null
If we don't want to have any attribute value as NULL.
Difference between Primary Key and Unique Key
One column can only be a primary key but we can have multiple columns with unique key constraint.
Conditions and Keywords in WHERE Clause
Use of >, <, <=, >=, =, != in conditions.
sql
Copy code
SELECT * FROM STUDENT;
SELECT * FROM STUDENT WHERE id = 12 OR id = 33;
SELECT * FROM STUDENT WHERE id >= 12 AND id <= 33;
SELECT * FROM STUDENT WHERE id != 12;
Keywords in WHERE Clause
IN
sql
Copy code
UPDATE STUDENT SET GENDER = 'male' WHERE id IN (18, 23, 56, 88);
-- OR	
UPDATE STUDENT SET GENDER = 'f' WHERE id = 12 OR id = 33;
BETWEEN
sql
Copy code
SELECT * FROM STUDENT WHERE id BETWEEN 18 AND 33;
LIKE
sql
Copy code
SELECT * FROM STUDENT WHERE name LIKE 'T%';
SELECT * FROM STUDENT WHERE name LIKE '_o%'; -- All names have 'o' as the second character
SELECT * FROM STUDENT WHERE name LIKE '__e%'; -- All names have 'e' as the third character
SELECT * FROM STUDENT WHERE name LIKE '%A%'; -- All names that contain 'A' anywhere in the string
ORDER BY
Arrange elements in ascending or descending order.
sql
Copy code
SELECT * FROM STUDENT ORDER BY name ASC; -- Ascending order
SELECT * FROM STUDENT ORDER BY name; -- Default is ascending
SELECT * FROM STUDENT ORDER BY id DESC; -- Descending order
SELECT * FROM STUDENT ORDER BY name DESC;
Select Query with Specific Fields
sql
Copy code
SELECT id, name FROM STUDENT;
SELECT student.id, student.name FROM STUDENT;
Aliasing
Defining alternative names for tables or columns
sql
Copy code
SELECT stud.id, stud.name FROM STUDENT AS stud;
SELECT stud.id AS student_id, stud.name AS student_name FROM STUDENT AS stud;
Joins
Inner Join
sql
Copy code
SELECT stud.id AS student_ID, stud.name AS student_name, sub.name AS subject_name 
FROM STUDENT AS stud, major_subject AS sub 
WHERE stud.subject_id = sub.id;
sql
Copy code
SELECT stud.id AS student_ID, stud.name AS student_name, sub.name AS subject_name 
FROM STUDENT AS stud 
INNER JOIN major_subject AS sub 
ON stud.subject_id = sub.id;
Getting Top Candidates based on Highest Marks
sql
Copy code
SELECT * FROM STUDENT ORDER BY marks DESC LIMIT 3;
Aggregation Functions
Maximum Marks
sql
Copy code
SELECT MAX(marks) FROM STUDENT;
Details of Candidates with Maximum Marks
sql
Copy code
SELECT * FROM STUDENT WHERE marks = (SELECT MAX(marks) FROM STUDENT);
Record of Candidate with Second Highest Marks
sql
Copy code
SELECT * FROM STUDENT WHERE marks < (SELECT MAX(marks) FROM STUDENT) ORDER BY marks DESC LIMIT 1;
Joins (LEFT, RIGHT, FULL OUTER JOIN)
Left Outer Join
sql
Copy code
SELECT student.id, student.name, major_subject.name FROM STUDENT 
LEFT OUTER JOIN major_subject ON student.subject_id = major_subject.id;
Right Outer Join
sql
Copy code
SELECT student.id, student.name, major_subject.name FROM STUDENT 
RIGHT OUTER JOIN major_subject ON student.subject_id = major_subject.id;
Full Outer Join
sql
Copy code
SELECT student.id, student.name, major_subject.name FROM STUDENT 
FULL OUTER JOIN major_subject ON student.subject_id = major_subject.id;
Group By
sql
Copy code
SELECT MAX(marks) FROM STUDENT GROUP BY gender; 

-- Get the maximum marks from male and female candidates in class.
SELECT * FROM STUDENT WHERE marks IN (SELECT MAX(marks) FROM STUDENT GROUP BY gender);
css
Copy code

You can directly copy the above Markdown-formatted content and paste it into your GitHub Markdown (.md) file. This will display the formatted content correctly with headings, code blocks, and lists.




