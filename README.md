# 💼 Job Portal Management System – SQL Project

## 📌 Project Title
**Job Portal Management System Using MySQL**

## 📖 Project Overview

The Job Portal Management System is a database management project developed using MySQL. It is designed to manage job seekers, recruiters, companies, job opportunities, applications, and interview information in an organized way.

This project demonstrates how SQL can be used to store, retrieve, update, delete, and analyze job portal data efficiently.

The project focuses on database operations, relationships between tables, SQL queries, joins, stored procedures, functions, views, triggers, indexes, and transaction management.

## ✨ Features

- **User Management:** Manage job seekers and recruiters.
- **Company Management:** Store and manage company information.
- **Job Management:** Add, update, view, and delete job postings.
- **Job Search:** Filter jobs based on location, salary, and job title.
- **Application Management:** Track application statuses such as Applied, Shortlisted, Selected, Rejected, and Interview.
- **Interview Management:** Maintain interview-related information.
- **Data Analysis:** Generate reports using aggregate functions.
- **Stored Procedures:** Perform reusable database operations.
- **Views:** Display simplified job and application details.
- **Triggers:** Maintain audit information and validate salary entries.
- **Indexes:** Improve query performance.
- **Transactions:** Manage database changes using COMMIT and ROLLBACK.

## 🗄️ Database Schema

The project uses a relational database named `job_portal`.

The database includes the following main tables:

| Table Name | Description |
|---|---|
| users | Stores user and account information |
| skills | Stores available skills |
| seeker_skills | Connects job seekers with skills |
| jobs | Stores job posting details |
| job_seekers | Stores job seeker information |
| companies | Stores company details |
| categories | Stores job categories |
| applications | Stores job application information |
| education | Stores educational information |
| interviews | Stores interview details |
| user_audit | Maintains user audit records |
| job_audit | Maintains job audit records |

## 🔗 Database Relationships

The database uses primary keys and foreign keys to connect related information.

Main relationships:

1. **Companies → Jobs:** One company can post multiple jobs.
2. **Categories → Jobs:** One category can contain multiple job postings.
3. **Users → Applications:** One job seeker can submit multiple applications.
4. **Jobs → Applications:** One job can receive multiple applications.
5. **Applications → Interviews:** An application can have interview records.
6. **Users → Seeker Skills:** Job seekers can be associated with multiple skills.
7. **Skills → Seeker Skills:** A skill can be associated with multiple job seekers.

These relationships help maintain data consistency and reduce unnecessary duplication.

## 💻 SQL Concepts Demonstrated

This project covers the following SQL concepts:

- Database creation and selection
- CREATE, INSERT, UPDATE, DELETE
- SELECT statements
- WHERE conditions
- DISTINCT
- ORDER BY
- GROUP BY and HAVING
- Aggregate functions (COUNT, SUM, AVG, MIN, MAX)
- LIKE, IN, BETWEEN
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- Subqueries
- Single-row and multi-row subqueries
- Views
- Stored Procedures
- User-defined Functions
- Triggers
- Primary Keys and Foreign Keys
- Indexing
- Composite Indexes
- Transactions
- COMMIT and ROLLBACK
- CRUD operations
- Database reporting and analysis

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| MySQL | Database management |
| SQL | Query writing and data manipulation |
| MySQL Workbench | Database development and execution |
| Git | Version control |
| GitHub | Project hosting and documentation |

## 📂 Project Files

```text
Job-Portal-SQL/
│
├── README.md
│
├── final sql project (1).sql
│
└── ER_Diagram.png
```

*Note: ER_Diagram.png is a suggested file to add when you create and export your database diagram.*

## 🚀 Getting Started

Follow these steps to run the project on your local system.

### 1. Clone the Repository

```bash
git clone https://github.com/Aruna0107/job-portal-sql.git
```

### 2. Navigate to the Project Folder

```bash
cd job-portal-sql
```

### 3. Open MySQL Workbench

- Open MySQL Workbench.
- Connect to your MySQL server.
- Open the project SQL file.
- Ensure the database and required tables are created.

### 4. Select the Database

```sql
USE job_portal;
```

### 5. Execute SQL Queries

Run the SQL script in MySQL Workbench to explore the database operations and SQL concepts.

## ⚙️ Installation and Setup

**Requirements:**

- MySQL Server
- MySQL Workbench
- Git
- Basic knowledge of SQL

**Setup Steps:**

1. Install MySQL Server.
2. Install MySQL Workbench.
3. Connect to your local MySQL server.
4. Create the `job_portal` database.
5. Create the required tables and relationships.
6. Import or execute the SQL project script.
7. Execute the queries and explore the results.

**Important:** The uploaded SQL script references an existing `job_portal` database and its tables. Make sure the database schema is created before executing the script.

## 🔍 Explore the Database

The project includes queries to explore and analyze database information.

Examples:

**Display all jobs:**

```sql
SELECT * FROM jobs;
```

**Find jobs in Hyderabad:**

```sql
SELECT *
FROM jobs
WHERE location = 'Hyderabad';
```

**Find jobs with salaries above 5 lakhs:**

```sql
SELECT *
FROM jobs
WHERE salary > 500000;
```

**Count total registered users:**

```sql
SELECT COUNT(*) AS total_users
FROM users;
```

**Find applications by status:**

```sql
SELECT status, COUNT(*) AS total_applications
FROM applications
GROUP BY status;
```

## ⚡ Stored Procedures

Stored procedures are used to execute reusable SQL operations.

The project demonstrates:

| Procedure | Purpose |
|---|---|
| get_jobs_by_location | Retrieves jobs based on location |
| get_jobs_by_salary | Retrieves jobs based on minimum salary |
| search_jobs | Searches jobs using location and salary |
| get_all_applications | Retrieves all applications |
| get_applications_by_status | Filters applications by status |
| get_application_details | Retrieves application details using joins |

Example:

```sql
CALL get_jobs_by_location('Hyderabad');
```

## 📊 Views

Views are virtual tables created using SQL queries.

The project includes:

- `job_details` – Displays job information.
- `job_seeker_details` – Displays job seeker information.
- `application_details` – Displays application and company information.
- `shortlisted_candidates` – Displays shortlisted candidates.
- `high_salary_jobs` – Displays jobs with salaries of 5 lakhs or above.

Example:

```sql
SELECT * FROM application_details;
```

## 🔔 Triggers

Triggers automatically execute when specific database operations occur.

The project demonstrates:

**1. after_user_insert**
- Executes after inserting a new user.
- Stores user information in the `user_audit` table.

**2. before_job_insert**
- Executes before inserting a new job.
- Checks whether the salary is negative.
- Changes a negative salary to zero.

These triggers demonstrate automatic database validation and auditing.

## 🏗️ ER Diagram

The Entity Relationship Diagram represents the structure of the Job Portal Management System and the relationships between its tables.

Main entities:

- Users
- Job Seekers
- Companies
- Jobs
- Categories
- Skills
- Seeker Skills
- Applications
- Education
- Interviews

The ER diagram helps understand how data is connected through primary keys and foreign keys.

## ⚠️ Limitations

- The project focuses mainly on database operations rather than a complete web application.
- No frontend user interface is included.
- Authentication and authorization are not fully implemented.
- Job notifications and email alerts are not implemented.
- Real-time job recommendations are not available.
- Database security and access control can be improved.

## 🔮 Future Improvements

- Develop a frontend using HTML, CSS, and JavaScript.
- Integrate a backend using Python or Java.
- Implement user registration and login authentication.
- Add resume upload and management functionality.
- Introduce job recommendations based on skills.
- Implement email notifications for application updates.
- Add advanced reporting and data visualization.
- Improve database security and performance.

## 📌 Disclaimer

This project is developed for educational and learning purposes to demonstrate MySQL and SQL database management concepts.

The project uses sample job portal data and is not intended to represent a fully operational commercial job portal.

## 👩‍💻 Author

**Magatapalli Aruna**

**Project Repository:** [Job Portal SQL Project](https://github.com/Aruna0107/job-portal-sql)

---

**Thank You for Visiting My Project!**
