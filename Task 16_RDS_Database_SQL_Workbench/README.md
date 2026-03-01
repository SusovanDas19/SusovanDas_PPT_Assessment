# Task 16 — RDS Database + SQL Workbench Connection & Queries

## 📌 Objective

To create a managed MySQL database using Amazon RDS and execute SQL queries through MySQL Workbench.

---

## 🏗️ Architecture

Client (MySQL Workbench) → RDS Endpoint → MySQL Database

This setup demonstrates secure external connectivity to a managed cloud database service.

---

## 🛠️ Services Used

- Amazon RDS (MySQL)
- MySQL Workbench
- Amazon EC2 (Security Group configuration)

---

## 🚀 Steps Performed

### 1️⃣ RDS Instance Creation

- Selected **MySQL** engine.
- Chose **Free Tier** configuration.
- Configured:
  - DB instance identifier
  - Master username and password
- Enabled **Public Access** (for external connectivity).
- Modified Security Group to allow:
  - **Port 3306 (MySQL)** from trusted IP address only.
- Waited for database status to become **Available**.

---

### 2️⃣ Connection Setup

- Retrieved the **RDS Endpoint** from AWS Console.
- Opened **MySQL Workbench**.
- Created new connection using:
  - Hostname: `<RDS-endpoint>`
  - Port: `3306`
  - Username: `<master-username>`
  - Password: `<master-password>`
- Successfully established connection.

---

### 3️⃣ SQL Execution

Executed the following SQL operations:

#### Create Database

```sql
CREATE DATABASE task16db;
USE task16db;
```

#### Create Table

```sql
CREATE TABLE students (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    age INT,
    course VARCHAR(50)
);
```

#### Insert Sample Record

```sql
INSERT INTO students (name, age, course)
VALUES ('John Doe', 22, 'Cloud Computing');
```

#### Query Data

```sql
SELECT * FROM students;
```

---

## 📊 Query Output

The query successfully returned the inserted student record, confirming:

- Database creation
- Table creation
- Data insertion
- Successful connectivity

---

## 🔑 Key Concepts

- Amazon RDS is a managed relational database service.
- RDS provides automated backups and maintenance.
- Security Groups control database access.
- Port 3306 is used for MySQL connections.
- Managed databases reduce operational overhead.

---

## 📷 Screenshots Included

1. `01-rds-instance-created.png`
2. `02-mysql-workbench-connection.png`
3. `03-sql-query-output.png`

---

## 🎯 Conclusion

Successfully created and connected to a managed MySQL database using Amazon RDS and MySQL Workbench.

This task demonstrates:

- Cloud-based database provisioning
- Secure external database connectivity
- SQL database creation and query execution
- Managed database best practices in AWS