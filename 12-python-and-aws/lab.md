# Lab 12 — AWS Inventory Reporter

## Objective
Use boto3 to create a basic AWS inventory report.

## Prerequisites
- AWS lab account
- Least-privilege IAM permissions
- AWS CLI credentials or IAM role configured safely

## Tasks
1. Install boto3.
2. Create an EC2 client.
3. List instance IDs and states.
4. Create an S3 client.
5. List bucket names.
6. Save the inventory to JSON.

## Important
Never put access keys in source code or commit credential files.

## Challenge
Filter EC2 instances using a tag such as `Environment=Lab`.

## Extension
Create a dry-run report identifying resources that could be stopped without actually stopping anything.
