1. what are the difference between sql and nosql database   
2. What is ACID properties in database    
3.1 What is normalization and denormalization     
3.2 Explain different sql queries types           
4. What is truncate keyword        
5. What is indexing in SQL     
6. What is diff b/w primary key and unique key      
7.1 select db, create db , use db , drop db       
7.2 crud on table   
7.3 different constraints in db     


Create 2 different tables: Emp Table(Emp ID, Name, DeptId, Country Name, City Name)
Dept Table(Dept Id, Dept Name)

8. Alter the table(add, remove and modify column datatype), rename table
9. IN, NOT IN, BETWEEN, ORDER BY
10. Joins
11. View(Create and Drop)
12. Advantages of views
13. LIKE operator
14. SAVEPOINT, ROLLBACK AND COMMIT
15. GROUP BY
16. HAVING CLAUSE
17. GET EMP with highest salary(second highest, third highest)
18. For each DEPT highest salary

max salary of each department- 
SELECT Dept_name,Emp_name,Emp_salary FROM Employee_Table
INNER JOIN 
Dept_Table
ON Dept_Table.Dept_Id=Employee_Table.Dept_Id
WHERE Emp_salary IN (SELECT MAX(Emp_Salary) FROM Employee_Table GROUP BY Dept_Id);    

**Assignment**       
Database Operations   
1.1 Create a database named school.    
1.2 Drop the school database.    
1.3 Show all databases.    
1.4 Use the school database.    

Table DDL Operations    
2.1 Create a table named students with columns id (INT), name (VARCHAR(100)), age (INT), and class (INT).    
2.2 Drop the students table.    
2.3 Show the structure of the students table.   
2.4 Add a column email (VARCHAR(100)) to the students table.    
2.5 Drop the column email from the students table.    
2.6 Modify the name column in the students table to VARCHAR(50).     
2.7 Rename the students table to SchooStudetns.    

Table DML Operations     
3.1 Insert a record into the table with values for id, name, age, and class.    
3.2 Update the age of a record in the table based on the id.    
3.3 Delete a record from the student table based on the id.    

Simple SELECT Queries   
4.1 Select the name and age columns from the student table.    
4.2 Select all columns from the student table.        

5.1 Add a primary key to the student table on the id column.    
5.2 Add a unique key to the email column in the student table.     
5.3 Set a default value of 10 for the class column.     
5.4 Make the id column auto-increment.     

Filtering and Sorting Data    
6.1 Use the WHERE clause with IN to select student in specific classes.    
6.2 Use BETWEEN to select student within a specific age range.    
6.3 Use LIKE to select student whose names match a certain pattern.    
6.4 Sort student by name in ascending or descending order.    

Aliasing   
7.1 Use an alias for the student table in a query.    
7.2 Use an alias for the name column in a query.    

Joins    
8.1 Perform an inner join between the student table and another table classes.    
8.2 Perform a full outer join between the student table and the classes table.    
8.3 Perform a left outer join between the student table and the classes table.     
8.4 Perform a right outer join between the student table and the classes table.

Subqueries   
9.1 Write a subquery to find student who are older than the average age.    
    
Advanced SELECT Queries    
10.1 Find the employee with the highest salary.    
10.2 Find the employee with the second highest salary.    
10.3 Find the employee with the Nth highest salary (where N is provided).    

Grouping Data    
11.1 Use GROUP BY to group student by class.    
11.2 Use aggregate functions to find the average age of employee in each class.    
11.3 Use HAVING to filter groups based on an aggregate function (e.g., groups with an average age greater than a certain value).    

 ---
 **Scenario Based Problems**
 
 Scenario 1: Create 2 tables employee and deparement . employee -> empid,name,salary,deptid   department- deptid, deptname.    
render employee details with departement name having highest salary in each department.         
Calculate the average salary for each department and order the results by the average salary in descending order.    

Scenario 2: Sales Database    
Problem Statement:
You have two tables, orders and customers. The orders table includes: order_id, customer_id, order_date, order_amount. The customers table includes: customer_id, customer_name, customer_city.   

Find the total sales amount for each customer in the city 'New York'.    
List the customers who have placed more than 5 orders along with the number of orders they have placed.     

Scenario 3: Product Inventory    
Problem Statement:    
You have a products table with the following columns: product_id, product_name, category_id, price, stock_quantity.   

Identify products that are out of stock.    
Find the category with the highest total stock value (price * stock_quantity).  

Scenario 4: Education Management System     
Problem Statement:    
You have two tables, students and courses. The students table includes: student_id, student_name, age, grade. The courses table includes: course_id, course_name, student_id, grade.    
    
List all students who have taken the course 'Database Systems' and received a grade of 'A'.   
Calculate the average grade for each student and list students whose average grade is above 85.    

Scenario 5: Library Management      
Problem Statement:    
You have a books table with the following columns: book_id, title, author_id, published_year, available_copies. And an authors table with author_id, author_name, birth_year.    

Find authors who have written more than 3 books.    
List all books published before the year 2000 that are currently out of stock    

