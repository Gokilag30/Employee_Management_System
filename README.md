# Employee Management System

A simple **Employee Management System** built using **Python and MySQL** that performs basic CRUD (Create, Read, Update, Delete) operations on employee records.

The project uses Python to connect with a MySQL database and provides a menu-driven command-line interface for managing employee information.

## Features

* Add a new employee record
* View all employee records
* Update employee information
* Delete an employee record
* Display records in a formatted table
* Store employee data permanently in a MySQL database

## Technologies Used

* **Python**
* **MySQL**
* **mysql-connector-python**
* **Tabulate**

## CRUD Operations

| Operation | Description                          |
| --------- | ------------------------------------ |
| Create    | Insert a new employee record         |
| Read      | Display all employee records         |
| Update    | Modify existing employee information |
| Delete    | Remove an employee record            |

## Database Structure

The project uses a MySQL database named `officedb` with a table named `data`.

### Table: `data`

| Column    | Description             |
| --------- | ----------------------- |
| `id`      | Unique employee ID      |
| `name`    | Employee name           |
| `age`     | Employee age            |
| `address` | Employee address        |
| `contact` | Employee contact number |
| `mail`    | Employee email address  |

## Project Structure

```text
Employee-Management-System/
│
├── employee_management.py
└── README.md
```

## Requirements

Make sure the following are installed on your system:

* Python 3.x
* MySQL Server
* MySQL Workbench

Install the required Python packages:

```bash
pip install mysql-connector-python
pip install tabulate
```

## Database Setup

Open MySQL Workbench and create the database:

```sql
CREATE DATABASE officedb;
```

Select the database:

```sql
USE officedb;
```

Create the employee table:

```sql
CREATE TABLE data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    address VARCHAR(255),
    contact VARCHAR(20),
    mail VARCHAR(100)
);
```

## MySQL Connection

Update the MySQL connection details in the Python program:

```python
con = mysql.connector.connect(
    host="localhost",
    user="root",
    password="YOUR_MYSQL_PASSWORD",
    database="officedb"
)
```

**Important:** Do not upload your actual MySQL password to GitHub.

For a real-world project, database credentials should be stored using environment variables instead of directly writing them in the Python file.

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Gokilag30/Employee_Management_System.git
```

### 2. Navigate to the project directory

```bash
cd Employee_Management_System
```

### 3. Install dependencies

```bash
pip install mysql-connector-python tabulate
```

### 4. Make sure MySQL Server is running

Verify that the `officedb` database and `data` table have been created.

### 5. Run the Python program

```bash
python MySQL_Database.py
```

## Menu Options

When the program starts, the following menu is displayed:

```text
1. Insert Record
2. Select Record
3. Update Record
4. Delete Record
5. Exit
```

### Insert Record

Allows the user to add a new employee by entering:

* Name
* Age
* Address
* Contact
* Email

### Select Record

Retrieves all employee records from MySQL and displays them in a formatted table using the `tabulate` library.

Example:

```text
+----+--------+-----+-------------+------------+-------------------+
| ID | NAME   | AGE | ADDRESS     | CONTACT    | MAIL              |
+----+--------+-----+-------------+------------+-------------------+
|  1 | Arun   |  25  | Coimbatore  | 9876543210 | arun@email.com    |
|  2 | Priya  |  24  | Pollachi    | 9876543211 | priya@email.com   |
+----+--------+-----+-------------+------------+-------------------+
```

### Update Record

Allows the user to update a specific field of an employee record:

```text
1. Name
2. Age
3. Address
4. Contact
5. Mail
```

The record is identified using its employee ID.

### Delete Record

Allows the user to delete an employee record by entering the employee ID.

## Concepts Demonstrated

This project demonstrates practical usage of:

* Python functions
* User input
* Conditional statements
* `while` loops
* MySQL database connectivity
* SQL `INSERT` statements
* SQL `SELECT` statements
* SQL `UPDATE` statements
* SQL `DELETE` statements
* Python-MySQL integration
* Database transactions using `commit()`
* MySQL cursors
* Parameterized SQL queries
* Tabular data formatting using `tabulate`

## Learning Outcome

Through this project, I gained practical experience in connecting Python applications with MySQL databases and performing CRUD operations. I also learned how to execute SQL queries from Python, retrieve database records, update and delete records, and display the results in a structured format.

## Future Improvements

The project can be enhanced by adding:

* Input validation
* Exception handling
* Search employee functionality
* Employee record filtering
* A graphical user interface
* Environment variables for database credentials
* Better database connection management
* Logging and error handling

## Author

**Gokila Gopinath**

---

If you found this project useful, feel free to explore the repository and suggest improvements.
