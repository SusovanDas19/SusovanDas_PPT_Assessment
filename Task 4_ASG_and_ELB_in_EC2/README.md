# Task 4 — Auto Scaling Group (ASG) with Application Load Balancer (ELB)

## Objective
To configure an Auto Scaling Group with an Application Load Balancer to achieve high availability and automatic scaling in AWS.

---

## Steps Performed

### 1. Launch Template Creation
- Created a Launch Template using Amazon Linux.
- Installed Apache using User Data script.
- Configured Security Group to allow HTTP and SSH.

### 2. Target Group Creation
- Created a Target Group with HTTP protocol (Port 80).
- Configured health check path as "/".

### 3. Application Load Balancer
- Created an Internet-facing Application Load Balancer.
- Selected multiple subnets for high availability.
- Attached the Target Group.

### 4. Auto Scaling Group
- Created ASG using the Launch Template.
- Attached ASG to the Load Balancer.
- Configured capacity:
  - Minimum: 1
  - Desired: 2
  - Maximum: 3

---

## Key Concepts

- Load Balancer distributes incoming traffic across instances.
- Auto Scaling Group automatically adjusts the number of EC2 instances.
- Health checks ensure only healthy instances receive traffic.
- Multi-AZ deployment ensures high availability.

---

## Screenshots Included

1. `01-asg-configuration.png`
2. `02-alb-active.png`
3. `03-load-balancer-output.png`
4. `04-Traget-Group.png`

---

## Conclusion

Successfully implemented an Auto Scaling Group integrated with an Application Load Balancer, demonstrating high availability and scalable architecture in AWS.

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project