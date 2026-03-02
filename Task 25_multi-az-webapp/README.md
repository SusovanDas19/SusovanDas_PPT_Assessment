# Task 01 – Multi-AZ Highly Available Web Application (AWS)

## 📌 Project Title
**Multi-AZ Highly Available Web Application Architecture on AWS**

---

## 📖 Introduction

This project demonstrates the design and deployment of a **highly available, fault-tolerant, and scalable web application architecture** on Amazon Web Services (AWS).

The implementation follows AWS best practices, including:

- Multi-Availability Zone deployment
- Network isolation
- Layered security
- Auto Scaling
- Centralized monitoring
- Decoupled static asset storage

The architecture ensures high availability, scalability, security, and production-grade reliability.

---

## 🏗 Architecture Overview

The infrastructure is deployed inside a custom VPC with the following components:

- **Custom VPC**: `10.0.0.0/16`
- **2 Public Subnets** (across 2 Availability Zones)
- **2 Private Subnets** (across 2 Availability Zones)
- **Internet Gateway**
- **NAT Gateway**
- **Application Load Balancer (Internet-facing)**
- **Auto Scaling Group**
  - Minimum: 1
  - Desired: 1
  - Maximum: 2
- **EC2 Instances** (Private Subnets)
- **Amazon S3** (Static Assets)
- **Amazon CloudWatch** (Monitoring & Scaling)
---

## 🔐 Network Design

### Public Subnets
- Application Load Balancer (ALB)
- NAT Gateway

### Private Subnets
- EC2 Instances (No public IP addresses)

### Internet Access Flow
- **Internet Gateway** → Allows public access to ALB
- **NAT Gateway** → Enables private EC2 instances to access the internet securely (updates, package installation)
- EC2 instances remain isolated from direct public access

---

## ⚖ High Availability Implementation

- Application deployed across **two Availability Zones**
- Auto Scaling Group maintains a **minimum of 2 EC2 instances**
- Unhealthy instances are automatically replaced
- Load Balancer distributes traffic evenly across healthy instances

This ensures continuous service availability even during instance or AZ failure.

---

## 🔄 Auto Scaling & Monitoring

### Monitoring
- Amazon CloudWatch monitors CPU utilization

### Scaling Policy
- If **CPU > 70%**, Auto Scaling launches additional EC2 instances
- Maximum scaling limit: 4 instances
- Automatically replaces unhealthy instances

This provides performance stability under variable traffic loads.

---

## 📦 Static Asset Management (S3 Integration)

Static files such as:

- CSS
- JavaScript

are stored in **Amazon S3**.

### Implementation Strategy

- EC2 instances serve only the HTML content
- Static assets are fetched directly from S3 via object URLs

### Benefits

- Decoupled architecture
- Stateless EC2 instances
- Improved scalability
- Easier maintenance
- Reduced load on web servers

---

## 🔒 Security Architecture

Layered security is implemented using Security Groups:

### ALB Security Group
- Allows HTTP (Port 80) from `0.0.0.0/0`

### EC2 Security Group
- Allows HTTP **only from ALB Security Group**
- No direct public access

This ensures strict traffic control and network isolation.

---

## 🧪 Testing & Validation

The application was tested using:

- Public ALB DNS URL
- Browser refresh to verify load balancing
- DevTools Network tab to confirm S3 asset loading
- Instance ID display to verify traffic distribution
- CloudWatch alarm validation

---

## 📊 Cost Estimation

A basic monthly estimate was calculated using the **AWS Pricing Calculator**, including:

- 2 × EC2 instances (t3.micro)
- 1 × Application Load Balancer
- 1 × NAT Gateway
- S3 storage (static assets)
- Data transfer costs

> ⚠️ Actual cost depends on usage patterns and AWS region.

---

## 📁 Repository Structure

```
task-01-multi-az-webapp/
│
├── architecture-diagram.png
├── screenshots/
└── README.md
```

---

## ⚙ Installation

1. Create a Custom VPC (`10.0.0.0/16`)
2. Create:
   - 2 Public Subnets (different AZs)
   - 2 Private Subnets (different AZs)
3. Attach Internet Gateway
4. Create NAT Gateway in Public Subnet
5. Configure Route Tables
6. Launch EC2 instances in Private Subnets
7. Configure Application Load Balancer
8. Create Target Group and attach Auto Scaling Group
9. Configure CloudWatch Alarm for CPU-based scaling
10. Upload static assets to S3

---

## ▶ Usage

- Access the application using the **ALB DNS URL**
- Traffic is automatically routed to healthy instances
- Auto Scaling adjusts capacity based on CPU utilization
---
## ✅ Conclusion

This project demonstrates a production-ready AWS architecture implementing:

- High Availability  
- Scalability  
- Secure Networking  
- Monitoring  
- Static Asset Decoupling  

The deployment aligns with real-world enterprise cloud architecture practices and follows AWS best practice design principles.