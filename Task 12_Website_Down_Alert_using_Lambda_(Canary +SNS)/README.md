# Task 12 — Website Down Alert using Lambda (Canary) and SNS

## Objective
To monitor website uptime and send automated email alerts when the website becomes unavailable.

---

## Architecture

CloudWatch Synthetics (Canary) → CloudWatch Alarm → SNS → Email

---

## Steps Performed

### 1. SNS Setup
- Created SNS topic for alert notifications.
- Added and confirmed email subscription.

### 2. Canary Configuration
- Created CloudWatch Synthetics Canary.
- Configured HTTP check for website URL.
- Scheduled periodic execution.

### 3. Alarm Setup
- Created CloudWatch Alarm based on Canary failure metric.
- Configured alarm action to trigger SNS.

### 4. Testing
- Simulated website downtime.
- Verified email alert was received.

---

## Key Concepts

- Automated monitoring using Canary.
- Real-time alerting using SNS.
- Event-driven alerting system.
- Useful for production uptime monitoring.

---

## Screenshots Included

1. `01-canary-created.png`
2. `02-cloudwatch-alarm.png`
3. `03-website-down-email-alert.png`

---

## Conclusion

Successfully implemented automated website monitoring and alert system using CloudWatch Synthetics and SNS, demonstrating production-level monitoring architecture.