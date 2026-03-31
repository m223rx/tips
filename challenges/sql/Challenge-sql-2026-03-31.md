# Challenge: Employee Hierarchy Query

## Difficulty
Medium

## Description
You are given a relational database that stores information about employees in a company. Each employee may have a manager, who is also an employee. The database consists of two tables:

| Table | Columns |
|-------|---------|
| **Employees** | `employee_id` (INT, Primary Key), `first_name` (VARCHAR), `last_name` (VARCHAR), `manager_id` (INT, nullable, foreign key to `employee_id`) |
| **Salaries**   | `employee_id` (INT, Primary Key, foreign key to `Employees.employee_id`), `salary` (DECIMAL) |

Your task is to write a single SQL query that returns a list of all employees, their direct manager's full name (concatenated as **first_name last_name**), and the total number of subordinates (both direct and indirect) under each employee. Employees without a manager should have `NULL` in the manager column. The result should be ordered by the number of subordinates in descending order, and then by `employee_id` ascending.

**Output columns**:

1. `employee_id`
2. `employee_name` – concatenation of the employee's `first_name` and `last_name` with a space.
3. `manager_name` – concatenation of the manager's `first_name` and `last_name` (or `NULL` if no manager).
4. `total_subordinates` – integer count of all employees that report (directly or indirectly) to this employee.

## Requirements
- Use a **single** SQL statement (no procedural code, temporary tables, or multiple statements).
- The query must work on standard SQL (compatible with PostgreSQL, MySQL, or SQL Server).
- Properly handle cycles in the manager hierarchy (assume the data may contain erroneous cycles; your query should not enter an infinite loop).
- Return `total_subordinates` as `0` for employees who have no subordinates.
- Ensure that the manager’s name appears exactly as `first_name last_name` without extra spaces.

## Bonus
- Add a column `average_subordinate_salary` that shows the average salary of all subordinates (direct and indirect) for each employee, rounded to two decimal places. If an employee has no subordinates, this column should be `NULL`.  
- Optimize the query for performance on large datasets (e.g., millions of employees) and briefly explain the indexing strategy you would recommend.  