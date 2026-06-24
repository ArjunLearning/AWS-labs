# EC2 to S3 Access using IAM Role

## Objective
Allow an EC2 instance to access an S3 bucket securely without using Access Keys or Secret Keys.

## Services Used
- Amazon EC2
- Amazon S3
- IAM Role
- AWS CLI

## Steps Performed

### 1. Created S3 Bucket
Created an S3 bucket named:

arjun-s3-lab-2026

Uploaded a sample PDF file.

### 2. Created IAM Role
Created an IAM Role for EC2 with the following policy:

AmazonS3ReadOnlyAccess

### 3. Attached Role to EC2
Attached the IAM Role to the EC2 instance.

### 4. Connected to EC2
Connected using EC2 Instance Connect.

### 5. Verified S3 Access
Executed AWS CLI commands:

```bash
**aws s3 ls
aws s3 ls s3://arjun-s3-lab-2026

Successfully listed the bucket contents from EC2.

Outcome
EC2 accessed S3 securely using IAM Role.
No Access Key or Secret Key was required.
AWS automatically provided temporary credentials.
Demonstrated secure service-to-service authentication.
Key Learning

IAM Roles are the recommended way to grant AWS service permissions without storing credentials inside instances.**
