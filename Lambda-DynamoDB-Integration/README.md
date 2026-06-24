# Lambda DynamoDB Integration

## Objective

Create an AWS Lambda function that inserts employee records into an Amazon DynamoDB table using Python.

---

## Architecture

Lambda → IAM Role → DynamoDB → CloudWatch Logs

---

## Services Used

- AWS Lambda
- Amazon DynamoDB
- IAM
- Amazon CloudWatch

---

## Steps Performed

1. Created DynamoDB table named Employees
2. Added EmployeeID as Partition Key
3. Created Lambda function (employee-record-writer)
4. Attached AmazonDynamoDBFullAccess policy through IAM Role
5. Added Python code using boto3
6. Deployed Lambda function
7. Created and executed Test Event
8. Inserted employee record into DynamoDB
9. Verified data in DynamoDB table
10. Verified execution logs in CloudWatch

---

## Lambda Code

```python
import json
import boto3

dynamodb = boto3.resource('dynamodb')

table = dynamodb.Table('Employees')

def lambda_handler(event, context):

    table.put_item(
        Item={
            'EmployeeID': 101,
            'Name': 'Arjun',
            'City': 'Bangalore',
            'Experience': '6 Years'
        }
    )

    return {
        'statusCode': 200,
        'body': json.dumps('Employee Added Successfully')
    }
