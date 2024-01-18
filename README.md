# use existing employee table
Write a SQL query to find the average salary for each department and also include the total number of employees in each department. Display the results in descending order of the average salary.
```SQL
SELECT 
	e.department_id, 
	d.department_name, 
	ROUND(avg(e.salary),2) AS average_salary, 
	COUNT(*) AS total_employees 
FROM 
	employees e
JOIN 
	departments d ON e.department_id = d.department_id
GROUP BY 
	e.department_id, department_name
ORDER BY 
	average_salary DESC;
```
