👩‍💼 HR Employee Analytics (SQL Project)

📌 Project Overview

This project demonstrates how to perform HR data analysis using SQL.
The focus is on analyzing employee salaries, attrition trends, and performance to support better workforce planning and decision-making.

🗄️ Database & Tables:

Database: hr_employee_analytics
Table: employees

| Column             | Type          | Description                        |
| ------------------ | ------------- | ---------------------------------- |
| emp\_id            | INT (PK)      | Unique Employee ID                 |
| name               | VARCHAR(50)   | Employee Name                      |
| department         | VARCHAR(50)   | Department (IT, HR, Finance, etc.) |
| salary             | DECIMAL(10,2) | Employee Salary                    |
| hire\_date         | DATE          | Date of Joining                    |
| attrition          | VARCHAR(10)   | Whether the employee left (Yes/No) |
| performance\_score | INT           | Employee performance rating (1–10) |

📊 Sample Data

INSERT INTO employees VALUES

(1, 'Ravi Kumar', 'IT', 60000, '2023-10-01', 'No', 8),

(2, 'Pooja Sharma', 'HR', 45000, '2024-03-15', 'Yes', 7),

(3, 'Amit Singh', 'Finance', 70000, '2022-11-20', 'No', 9),

(4, 'Surbhi Masih', 'IT', 50000, '2024-02-05', 'No', 6),

(5, 'Neha Gupta', 'HR', 40000, '2023-12-10', 'Yes', 5);

📈 Analysis Performed

🔹 1. Average Salary by Department
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;


👉 Output: Shows average employee salary per department.

🔹 2. Attrition Rate by Department
SELECT department,
       (SUM(CASE WHEN attrition='Yes' THEN 1 ELSE 0 END)*100.0 / COUNT(*)) AS attrition_rate
FROM employees
GROUP BY department;


👉 Output: Calculates percentage of employees who left in each department.

🛠️ Tools & Technologies

SQL (MySQL / PostgreSQL / MariaDB) – Data analysis

Database Schema Design – HR dataset with employee details

Analytical Queries – AVG(), CASE WHEN, GROUP BY

📌 Key Insights (from sample data)

Finance has the highest salary average.

HR shows higher attrition compared to IT and Finance.

Performance scores vary, indicating areas for employee training and retention strategies.

🚀 Future Enhancements

Add employee demographics (age, gender, education) for deeper HR insights.

Track promotion trends and performance over time.

Integrate with Power BI to build interactive HR dashboards.

✍️ Author: Surbhi Masih
