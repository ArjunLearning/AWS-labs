# AWS Lambda Error Monitoring using CloudWatch and SNS

## Objective

Monitor Lambda failures and send email notifications using CloudWatch Alarm and SNS.

## Services Used

* AWS Lambda
* Amazon CloudWatch
* Amazon SNS

## Architecture

Lambda Function

↓

CloudWatch Error Metric

↓

CloudWatch Alarm

↓

SNS Topic

↓

Email Notification

## Implementation Steps

### Step 1

Created Lambda Function: test-error-lambda

### Step 2

Generated an exception using Python code.

### Step 3

Created SNS Topic: lambda-error-alert

### Step 4

Added Email Subscription and confirmed it.

### Step 5

Created CloudWatch Alarm on Lambda Error Metric.

### Step 6

Triggered Lambda failure and received email notification.

## Result

Successfully implemented monitoring and alerting using AWS Lambda, CloudWatch, and SNS.

## Screenshots

* Lambda Function Code
* Lambda Execution Failure
* CloudWatch Alarm
* SNS Subscription
* Email Notification
