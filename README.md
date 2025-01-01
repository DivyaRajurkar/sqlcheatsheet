# SQL Cheat Sheet

A comprehensive guide to SQL commands, functions, and best practices. This cheat sheet is designed to help developers and analysts master SQL quickly.

---

## 📘 Overview

This repository provides:

- A complete list of essential SQL commands.
- Examples to demonstrate usage.
- Categorized sections for easy navigation.

Download the [SQL Cheat Sheet PDF](#).

---

## 📂 Categories

1. [Creating and Managing Databases](#creating-and-managing-databases)
2. [Creating and Manipulating Data](#creating-and-manipulating-data)
3. [Querying Data](#querying-data)
4. [Filtering Data](#filtering-data)
5. [SQL Operators](#sql-operators)
6. [Aggregating Data](#aggregating-data)
7. [Constraints](#constraints)
8. [Joins](#joins)
9. [SQL Functions](#sql-functions)
10. [Subqueries](#subqueries)
11. [Views](#views)
12. [Indexes](#indexes)

---

## 🏗 Creating and Managing Databases

### 1. CREATE DATABASE

```sql
CREATE DATABASE company;
```

Creates a new database named "company."

### 2. USE

```sql
USE company;
```

Selects the database "company" for operations.

### 3. ALTER DATABASE

```sql
ALTER DATABASE database_name;
```

Modifies a database’s attributes.

### 4. DROP DATABASE

```sql
DROP DATABASE company;
```

Deletes the database "company" and its data.

---

## 🗂 Creating and Manipulating Data

### 5. CREATE TABLE

```sql
CREATE TABLE employees (
  employee_id INT PRIMARY KEY,
  first_name VARCHAR(50),
  last_name VARCHAR(50),
  department VARCHAR(50),
  salary DECIMAL(10, 2)
);
```

Creates a table named "employees."

### 6. INSERT INTO

```sql
INSERT INTO employees (employee_id, first_name, last_name, department, salary)
VALUES
  (1, 'John', 'Doe', 'HR', 50000.00);
```

Adds new records to the "employees" table.

### 7. ALTER TABLE

```sql
ALTER TABLE employees
ADD COLUMN new_column INT;
```

Adds a new column to the "employees" table.

### 8. DROP TABLE

```sql
DROP TABLE employees;
```

Deletes the table "employees."

---

## 🔍 Querying Data

### 9. SELECT

```sql
SELECT * FROM employees;
```

Retrieves all columns from "employees."

### 10. DISTINCT

```sql
SELECT DISTINCT department FROM employees;
```

Fetches unique department names.

### 11. WHERE

```sql
SELECT * FROM employees WHERE salary > 55000.00;
```

Filters rows based on conditions.

---

## 🔎 Filtering Data

### 18. WHERE

```sql
SELECT * FROM employees WHERE department = 'IT';
```

Filters employees by department.

### 19. LIKE

```sql
SELECT * FROM employees WHERE first_name LIKE 'J%';
```

Searches for patterns in data.

---

## 🔗 Joins

### 45. INNER JOIN

```sql
SELECT * FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;
```

Fetches records with matching values in both tables.

### 46. LEFT JOIN

```sql
SELECT * FROM employees
LEFT JOIN departments ON employees.department_id = departments.department_id;
```

Retrieves all records from the left table and matches from the right table.

---

## 📊 Aggregating Data

### 33. COUNT

```sql
SELECT COUNT(*) FROM employees;
```

Counts the number of rows.

### 34. SUM

```sql
SELECT SUM(salary) FROM employees;
```

Calculates the total salary of employees.

---

## 🚧 Constraints

### 40. PRIMARY KEY

```sql
CREATE TABLE employees (
  employee_id INT PRIMARY KEY,
  first_name VARCHAR(50),
  last_name VARCHAR(50)
);
```

Ensures unique identification of records.

### 41. FOREIGN KEY

```sql
CREATE TABLE employees (
  department_id INT,
  FOREIGN KEY (department_id) REFERENCES departments(department_id)
);
```

Establishes a relationship between two tables.

---

## 📝 Views

### 60. CREATE VIEW

```sql
CREATE VIEW high_paid_employees AS
SELECT * FROM employees WHERE salary > 60000;
```

Creates a virtual table "high\_paid\_employees."

### 61. DROP VIEW

```sql
DROP VIEW high_paid_employees;
```

Deletes the view.

---

## 🚀 Indexes

### Purpose

Indexes improve query performance by optimizing data retrieval.

---








