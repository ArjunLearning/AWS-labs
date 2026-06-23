# EventBridge Scheduled Lambda

## Objective

Create a scheduled AWS Lambda function that automatically runs every 1 minute using Amazon EventBridge and stores execution logs in Amazon CloudWatch.

---

## Architecture

EventBridge
↓
Lambda
↓
CloudWatch Logs

---

## Services Used

- AWS Lambda
- Amazon EventBridge
- Amazon CloudWatch Logs
- IAM

---

## Steps Performed

1. Created Lambda Function
2. Added Python code
3. Tested Lambda execution
4. Created EventBridge Scheduled Rule
5. Configured rule to run every 1 minute
6. Attached Lambda as target
7. Verified execution in CloudWatch Logs

---

## Screenshots

### Lambda Function

![Lambda Code](lambda-code.png)

### EventBridge Rule

![EventBridge Rule](eventbridge-rule.png)

### CloudWatch Logs

![CloudWatch Logs](cloudwatch-logs.png)

### Lambda Trigger

![Lambda Trigger](lambda-trigger.png)

---

## Outcome

Successfully implemented a serverless scheduled automation solution using EventBridge and Lambda with monitoring through CloudWatch Logs.
