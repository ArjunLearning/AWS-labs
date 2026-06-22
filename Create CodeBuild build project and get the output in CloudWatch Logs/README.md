# AWS CodeBuild Project with CloudWatch Logs

## Objective
Created an AWS CodeBuild project using source code from Amazon S3, ran the build, stored artifacts in S3, and verified build output in CloudWatch Logs.

## Services Used
- AWS CodeBuild
- Amazon S3
- Amazon CloudWatch Logs
- IAM Service Role

## Steps Performed
1. Created/used S3 bucket for source zip file: MessageUtil.zip
2. Created S3 bucket for build artifacts.
3. Created CodeBuild project.
4. Selected Amazon S3 as source provider.
5. Enabled CloudWatch Logs.
6. Ran the build successfully.
7. Verified logs in CloudWatch.
8. Verified build artifact in S3.

## Result
Build completed successfully and generated artifact was stored in the S3 output bucket.

