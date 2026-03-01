# Task 13 — Start/Stop EC2 using Lambda and API Gateway

## 📌 Objective

To automate EC2 instance start and stop operations using an AWS Lambda function triggered via Amazon API Gateway.

---

## 🏗️ Architecture

API Gateway → Lambda → EC2 Instance

This architecture enables serverless control of EC2 instances through an HTTP endpoint.

---

## 🛠️ Steps Performed

### 1️⃣ IAM Role Configuration

- Created a Lambda execution role.
- Attached required permissions:
  - EC2 permissions (StartInstances, StopInstances, DescribeInstances)
  - AWSLambdaBasicExecutionRole

---

### 2️⃣ Lambda Function Setup

- Created a Lambda function (Python runtime).
- Wrote Python code to:
  - Read query parameter (`action=start` or `action=stop`)
  - Trigger EC2 start or stop operation
- Deployed the function.

---

### 3️⃣ API Gateway Configuration

- Created an **HTTP API**.
- Integrated API Gateway with the Lambda function.
- Deployed the API.
- Generated a public endpoint URL.

---

### 4️⃣ Testing

- Triggered the API using query parameters.
- Verified EC2 instance state change via:
  - AWS Console
  - EC2 Instance State Monitoring

---

## 🌐 API Usage

### ▶️ Start Instance

```
https://gvtjvkdmug.execute-api.ap-south-1.amazonaws.com/ec2?action=start
```

### ⏹️ Stop Instance

```
https://gvtjvkdmug.execute-api.ap-south-1.amazonaws.com/ec2?action=stop
```

---

## 🔑 Key Concepts

- Serverless automation
- API-driven infrastructure control
- IAM role-based secure access
- Event-driven architecture
- Cloud resource automation using Lambda

---

## 📷 Screenshots Included

1. `01-lambda-ec2-code.png`
2. `02-api-gateway-endpoint.png`
3. `03-api-start-stop-output.png`

---

## 🎯 Conclusion

Successfully implemented EC2 start/stop automation using:

- AWS Lambda
- Amazon API Gateway
- IAM Role-based permissions

This task demonstrates practical serverless infrastructure management and API-driven cloud automation.

---

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project