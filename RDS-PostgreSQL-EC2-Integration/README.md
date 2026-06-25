# Amazon RDS PostgreSQL + EC2 Integration

## Project Overview

This project demonstrates how to connect an Amazon EC2 instance to an Amazon RDS PostgreSQL database using the PostgreSQL client.

The lab covers:

- Amazon RDS PostgreSQL database creation
- EC2 instance launch
- Security Group configuration
- Database connectivity
- PostgreSQL client installation
- SQL operations (CREATE, INSERT, SELECT)

---

## AWS Services Used

- Amazon RDS
- PostgreSQL
- Amazon EC2
- VPC
- Security Groups
- IAM
- Amazon Linux 2023

---

## Architecture

EC2 Instance
        │
        │ PostgreSQL Client (psql)
        │
        ▼
Amazon RDS PostgreSQL

---

## Step 1 - Create RDS PostgreSQL Database

Created an Amazon RDS PostgreSQL database named:

employees

Master User:

postgres

---

## Step 2 - Launch EC2 Instance

Created an Amazon Linux EC2 instance in the same VPC.

AWS automatically configured connectivity between EC2 and RDS.

---

## Step 3 - Install PostgreSQL Client

```bash
sudo dnf install postgresql15 -y
```

---

## Step 4 - Connect to Database

```bash
psql -h <RDS-ENDPOINT> -U postgres -d employees
```

---

## Step 5 - Create Table

```sql
CREATE TABLE employees (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    department VARCHAR(50)
);
```

---

## Step 6 - Insert Records

```sql
INSERT INTO employees(name, department)
VALUES
('Arjun','DevOps'),
('Rahul','Cloud'),
('Amit','SRE');
```

---

## Step 7 - Verify Data

```sql
SELECT * FROM employees;
```

Output:

| ID | Name | Department |
|----|------|------------|
|1|Arjun|DevOps|
|2|Rahul|Cloud|
|3|Amit|SRE|

---

## What I Learned

- Amazon RDS
- PostgreSQL
- EC2 Integration
- Security Groups
- Database Endpoint
- PostgreSQL Client
- SQL Basics
- Managed Database Services

---

## Author

Arjun Singh

