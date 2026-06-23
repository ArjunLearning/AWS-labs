# DynamoDB Employee Records

## Objective
Create an Amazon DynamoDB table and perform CRUD operations on employee records.

## Services Used
- Amazon DynamoDB
- IAM

## Steps Performed

1. Created DynamoDB table named Employees
2. Configured Partition Key: EmployeeID (Number)
3. Inserted employee records
4. Queried records using Partition Key
5. Verified data retrieval from DynamoDB

## Sample Data

| EmployeeID | Name  | City    | Experience |
|------------|--------|---------|------------|
| 101 | Arjun | Amroha | 3.6 Years |
| 102 | Kajal | Amroha | 5 Years |

## Outcome

Successfully created a DynamoDB table, stored employee data, and retrieved records using the partition key.

## Architecture

User → DynamoDB Table → Query Results
