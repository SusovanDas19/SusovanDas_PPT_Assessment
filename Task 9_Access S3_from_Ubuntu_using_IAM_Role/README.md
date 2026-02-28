# Task 9 — Access S3 from Ubuntu using IAM Role

## Objective
To securely access Amazon S3 from an EC2 Ubuntu instance using IAM Role instead of access keys.

---

## Steps Performed

### 1. IAM Role Creation
- Created IAM Role for EC2.
- Attached policy: AmazonS3FullAccess.

### 2. Attach Role to EC2
- Attached IAM role to Ubuntu EC2 instance.

### 3. AWS CLI Installation
- Installed AWS CLI on Ubuntu.
- Verified installation.

### 4. S3 Access Verification
- Executed `aws s3 ls` without configuring credentials.
- Successfully accessed S3 buckets.
- Uploaded test file to S3.

---
## Key Concepts

- IAM Roles provide temporary security credentials.
- Avoids storing access keys on EC2.
- Uses Instance Metadata Service.
- Recommended best practice for EC2 to AWS service access.

---

## Screenshots Included

1. `01-ec2-role-attached.png`
2. `02-s3-access-from-ec2.png`

---

## Conclusion

Successfully configured secure role-based access from EC2 to S3 without using access keys, demonstrating AWS best security practices.

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project