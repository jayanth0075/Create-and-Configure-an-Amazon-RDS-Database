# AWS RDS MySQL Database Experiment

## Student Details

- **Name:** Jayanth
- **Roll Number:** 2410080075

## Experiment Title

**Creating and Configuring an Amazon RDS MySQL Database Instance**

## Objective

To create and configure an Amazon RDS MySQL database instance, establish secure network connectivity, connect using MySQL Workbench, and perform basic database operations using SQL queries.

## Technologies Used

- Amazon Web Services (AWS)
- Amazon Relational Database Service (RDS)
- MySQL Community Edition
- MySQL Workbench
- SQL

## Database Configuration

| Parameter | Configuration |
|---|---|
| DB Instance Identifier | exp-1 |
| Database Engine | MySQL |
| Engine Version | 8.4.11 |
| Instance Class | db.t3.micro |
| Master Username | admin |
| Database Port | 3306 |
| Storage Type | General Purpose SSD (gp3) |
| Database Name | aws_experiment |

## Experiment Procedure

1. Logged into the AWS Management Console.
2. Navigated to Amazon RDS.
3. Selected MySQL as the database engine.
4. Configured the database identifier and master credentials.
5. Selected the appropriate DB instance class and storage configuration.
6. Configured the VPC, subnet group, and connectivity settings.
7. Configured the security group to allow authorized MySQL connections through port 3306.
8. Created the RDS database instance.
9. Waited until the database status changed to Available.
10. Retrieved the database endpoint from Connectivity & Security.
11. Configured a MySQL Workbench connection using the RDS endpoint.
12. Successfully connected to the MySQL database.
13. Executed SQL queries to create a database, create a table, insert records, and retrieve data.

## SQL Implementation

```sql
SHOW DATABASES;

CREATE DATABASE aws_experiment;

USE aws_experiment;

CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    course VARCHAR(50)
);

INSERT INTO students (id, name, course)
VALUES
(1, 'Jayanth', 'AI and Data Science'),
(2, 'Divij', 'AI and Data Science');

SELECT * FROM students;
```

## Expected Output

| ID | Name | Course |
|---|---|---|
| 1 | Jayanth | AI and Data Science |
| 2 | Divij | AI and Data Science |

## Result

Successfully created and configured an Amazon RDS MySQL database instance using AWS. Established a connection through MySQL Workbench and successfully executed SQL queries to create databases and tables, insert records, and retrieve the stored information.

## Conclusion

This experiment provided practical experience with Amazon RDS, cloud database provisioning, storage configuration, network connectivity, security groups, and MySQL database management using AWS.

## Cost Management

After completing the experiment, the RDS instance should be deleted if it is no longer required to avoid additional AWS charges. Any unnecessary snapshots and associated resources should also be reviewed.

---

**Created by:** Jayanth  
**Roll Number:** 2410080075
