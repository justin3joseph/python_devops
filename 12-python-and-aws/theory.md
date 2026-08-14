# Module 12 — Python + AWS

## Objectives
- Understand boto3.
- Configure AWS credentials safely.
- Query EC2 and S3.
- Automate basic cloud operations.

Install:
```bash
python3 -m pip install boto3
```

## Credentials
Do not hard-code access keys in Python source code.

Use the AWS CLI credential configuration, environment variables, or an appropriate IAM role.

## EC2 Example
```python
import boto3

ec2 = boto3.client("ec2")

response = ec2.describe_instances()

for reservation in response["Reservations"]:
    for instance in reservation["Instances"]:
        print(instance["InstanceId"], instance["State"]["Name"])
```

## S3 Example
```python
s3 = boto3.client("s3")

for bucket in s3.list_buckets()["Buckets"]:
    print(bucket["Name"])
```

## Safety
For start/stop/delete operations:
- Confirm the target.
- Use tags where possible.
- Test in a lab account.
- Apply least privilege IAM permissions.
