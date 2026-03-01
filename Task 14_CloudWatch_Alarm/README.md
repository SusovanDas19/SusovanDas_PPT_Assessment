# Task 14 — CloudWatch Alarm (70% CPU → Auto Stop + Email)

## 📌 Objective

To configure an automated monitoring system using Amazon CloudWatch that stops an EC2 instance when CPU utilization exceeds 70% and sends an email notification via Amazon SNS.

---

## 🏗️ Architecture

EC2 Instance → CloudWatch Metric (CPUUtilization) → CloudWatch Alarm  
→ EC2 Stop Action + SNS Email Notification

This setup enables automated monitoring and cost-control through event-driven actions.

---

## 🛠️ Services Used

- Amazon EC2
- Amazon CloudWatch
- Amazon SNS

---

## 🚀 Steps Performed

### 1️⃣ SNS Configuration

- Created SNS Topic: `Task14-HighCPU-Alerts`
- Added an email subscription
- Confirmed subscription via verification email

---

### 2️⃣ CloudWatch Alarm Creation

- Selected Metric:
  ```
  AWS/EC2 → CPUUtilization
  ```
- Selected the target EC2 instance
- Statistic: **Average**
- Period: **300 seconds (5 minutes)**
- Evaluation Periods: **2**
- Threshold Condition: **CPU ≥ 70%**

---

### 3️⃣ Alarm Actions Configured

- EC2 Action: **Stop Instance**
- SNS Action: Send notification to `Task14-HighCPU-Alerts`

---

### 4️⃣ Testing

- Simulated high CPU usage on EC2 instance
- Alarm transitioned to **ALARM** state
- EC2 instance stopped automatically
- Email notification successfully received

---

## 📊 Key Configuration Details

| Parameter | Value |
|-----------|--------|
| Metric | CPUUtilization |
| Threshold | ≥ 70% |
| Period | 60 seconds |
| EC2 Action | Stop Instance |
| Notification | SNS Email |

---

## 🔑 Key Concepts

- CloudWatch monitors AWS resource metrics in real time.
- Alarms trigger automated actions based on defined thresholds.
- Automated EC2 stop helps reduce unexpected costs.
- SNS provides real-time alerting.
- Demonstrates integration of monitoring and automation.

---

## 📷 Screenshots Included

1. `01-cloudwatch-alarm-config.png`
2. `02-email-and-ec2-stopped.png`

---

## 🎯 Conclusion

Successfully implemented automated infrastructure control using CloudWatch Alarm.

When CPU utilization exceeds 70%:
- The EC2 instance stops automatically.
- An email notification is sent via SNS.

This task demonstrates effective monitoring, automation, and cost-optimization practices in AWS.

---

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project