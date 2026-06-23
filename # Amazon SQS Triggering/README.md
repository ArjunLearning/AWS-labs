# Amazon SQS Triggering AWS Lambda Function

## Objective

To create an event-driven architecture where messages sent to an Amazon SQS queue automatically trigger an AWS Lambda function and the execution logs are monitored in Amazon CloudWatch.

---

## Architecture

Amazon SQS Queue
        ↓
AWS Lambda Function
        ↓
Amazon CloudWatch Logs

---

## AWS Services Used

- Amazon SQS
- AWS Lambda
- Amazon CloudWatch Logs
- AWS IAM

---

## Steps Performed

### Step 1: Created SQS Queue

Created a Standard Queue named:

demo-sqs-queue

---

### Step 2: Created Lambda Function

Created a Lambda function:

sqs-message-processor

Runtime Used:

Python 3.x

---

### Step 3: Added IAM Permissions

Attached policy:

AWSLambdaSQSQueueExecutionRole

This allowed Lambda to:

- Receive messages from SQS
- Delete messages from SQS
- Read queue attributes
- Write logs to CloudWatch

---

### Step 4: Configured SQS Trigger

Connected the SQS queue with Lambda using Lambda Trigger configuration.

---

### Step 5: Developed Lambda Function

```python
import json

def lambda_handler(event, context):
    print("Message received from SQS")

    for record in event['Records']:
        print("Message Body:", record['body'])

    return {
        'statusCode': 200,
        'body': json.dumps('Message processed successfully')
    }
Step 6: Sent Test Message

Message sent to SQS Queue:

{
  "name": "Arjun",
  "message": "Hello from SQS"
}
Step 7: Verified CloudWatch Logs

Successfully verified:

Lambda execution
SQS message processing
CloudWatch log generation
Output

Lambda successfully processed incoming messages from Amazon SQS and generated logs in Amazon CloudWatch.

Learning Outcome
Learned Amazon SQS fundamentals
Configured Lambda triggers
Managed IAM permissions
Implemented event-driven architecture
Monitored execution using CloudWatch Logs
```
