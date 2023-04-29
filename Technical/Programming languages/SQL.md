# SQL
**Q: What is SQL?**  
SQL (Structured Query Language) is a programming language designed to manage data in relational database management systems (RDBMS). SQL is used to perform various operations on data such as creating, modifying, and deleting data in databases.

**Q: What are the types of SQL statements?**  
There are four types of SQL statements: 
- Data Definition Language (DDL) statements: used to create, modify, and delete database objects such as tables, views, indexes, and so on.
- Data Manipulation Language (DML) statements: used to insert, update, and delete data in a database.
- Data Control Language (DCL) statements: used to manage user permissions and access rights in a database.
- Transaction Control Language (TCL) statements: used to manage transactions in a database.

**Q: What is the difference between INNER JOIN and OUTER JOIN?**  
INNER JOIN returns only the matching rows from both tables, while OUTER JOIN returns all rows from one table and matching rows from the other table. There are three types of OUTER JOIN: LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN.

**Q: What is normalization in SQL?**  
Normalization is a process of organizing data in a database to minimize redundancy and dependency. Normalization ensures that each table has a unique key (primary key) and that each column depends only on the primary key.

**Q: What is a subquery in SQL?**  
A subquery is a query within another query. A subquery is used to retrieve data from one or more tables based on a condition that is evaluated in another query.

**Q: What is a stored procedure in SQL?**  
A stored procedure is a set of SQL statements that are stored in a database and can be executed as a single unit. Stored procedures are used to encapsulate complex logic and perform repetitive tasks in a database.

**Q: What is indexing in SQL?**  
Indexing is a technique used to speed up the data retrieval process from a database. Indexing involves creating an index on one or more columns in a table, which allows the database to quickly locate the required data.

**Q: What is a transaction in SQL?**  
A transaction is a set of SQL statements that are executed as a single unit of work. Transactions ensure that a set of operations is either completed in full or not at all. Transactions ensure that the data in a database remains consistent.

**Q: What is the difference between UNION and UNION ALL in SQL?**  
UNION and UNION ALL are used to combine the results of two or more SELECT statements into a single result set. The difference between UNION and UNION ALL is that UNION removes duplicate rows from the result set, while UNION ALL includes all rows, including duplicates.

**Q: What is the difference between GROUP BY and ORDER BY in SQL?**  
GROUP BY is used to group the rows of a table based on one or more columns, while ORDER BY is used to sort the result set based on one or more columns. GROUP BY is used with aggregate functions (such as COUNT, SUM, AVG, etc.) to calculate the summary data for each group. ORDER BY sorts the rows in ascending or descending order based on the specified column(s).

**Q: Given a table called `employees` with columns `employee_id`, `employee_name`, and `salary`, write a SQL query to retrieve the names and salaries of all employees earning more than $50,000 per year.**  

```sql
SELECT employee_name, salary
FROM employees
WHERE salary > 50000;
```

**Q: Given a table called `orders` with columns `order_id`, `customer_id`, and `order_date`, write a SQL query to retrieve the number of orders per customer for the month of January 2023.**  

```sql
SELECT customer_id, COUNT(*) AS order_count
FROM orders
WHERE order_date >= '2023-01-01' AND order_date < '2023-02-01'
GROUP BY customer_id;
```

**Q: Given a table called `students` with columns `student_id`, `student_name`, and `course_id`, and a table called `courses` with columns `course_id` and `course_name`, write a SQL query to retrieve the names of all students enrolled in the course "Database Systems".**  

```sql
SELECT student_name
FROM students
JOIN courses ON students.course_id = courses.course_id
WHERE courses.course_name = 'Database Systems';
```

**Q: Given a table called `sales` with columns `sale_id`, `sale_date`, and `amount`, write a SQL query to retrieve the total sales amount for each month in the year 2022.**  

```sql
SELECT DATE_TRUNC('month', sale_date) AS month, SUM(amount) AS total_sales
FROM sales
WHERE sale_date >= '2022-01-01' AND sale_date < '2023-01-01'
GROUP BY month;
```

**Q: Given a table called `books` with columns `book_id`, `book_title`, and `publisher_id`, and a table called `publishers` with columns `publisher_id` and `publisher_name`, write a SQL query to retrieve the names of all publishers who have published more than 10 books.**  

```sql
SELECT publisher_name
FROM publishers
JOIN books ON publishers.publisher_id = books.publisher_id
GROUP BY publishers.publisher_id
HAVING COUNT(*) > 10;
```
