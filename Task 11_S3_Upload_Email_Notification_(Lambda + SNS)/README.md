# Task 11 — S3 Upload Email Notification using Lambda and SNS

## Objective
To configure an event-driven architecture where uploading a file to S3 triggers a Lambda function that sends an email notification using SNS.

---

## Architecture

S3 → Lambda → SNS → Email Notification

---

## Steps Performed

### 1. SNS Setup
- Created SNS topic.
- Added email subscription.
- Confirmed subscription via email.

### 2. Lambda Function
- Created Lambda function using Python runtime.
- Added SNS publish permissions.
- Wrote code to send notification to SNS topic.

### 3. S3 Trigger
- Configured S3 bucket event trigger.
- Triggered Lambda on object creation.

### 4. Testing
- Uploaded file to S3.
- Verified email notification received.

---

## Key Concepts

- Event-driven architecture
- Serverless computing using Lambda
- Messaging service using SNS
- Automated workflow using S3 triggers

---

## Screenshots Included

1. `01-sns-topic-email-confirmed.png`
2. `02-lambda-s3-trigger.png`
3. `03-email-notification-proof.png`

---

## Conclusion

Successfully implemented automated email notification using S3, Lambda, and SNS, demonstrating event-driven serverless architecture in AWS.