# Task 8 — Create IAM Users and Groups

## Objective
To manage user access and permissions in AWS using IAM Users and Groups.

---

## Steps Performed

### 1. Group Creation
- Created IAM Group named "Developers".
- Attached managed policy: AmazonS3FullAccess.

### 2. User Creation
- Created IAM user "dev-user".
- Enabled AWS Management Console access.
- Added user to the "Developers" group.

### 3. Verification
- Logged in using IAM credentials.
- Verified S3 access permissions.

---

## Key Concepts

- IAM controls authentication and authorization in AWS.
- Groups allow centralized permission management.
- Policies define allowed and denied actions.
- Following least privilege improves security.

---

## Screenshots Included

1. `01-iam-group-with-policy.png`
2. `02-iam-user-in-group.png`

---

## Conclusion

Successfully created IAM users and groups, demonstrating structured access control and policy-based permission management in AWS.

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project