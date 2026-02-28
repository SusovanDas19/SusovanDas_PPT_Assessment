# Task 10 — VPC 3-Tier Architecture

## Objective
To design a secure 3-tier architecture using public and private subnets, Internet Gateway, NAT Gateway, and SSH tunneling.

---

## Architecture Design

- Created custom VPC (10.0.0.0/16)
- Created three subnets:
  - Public Subnet (Web/Bastion)
  - Private App Subnet
  - Private DB Subnet

---

## Networking Configuration

### Internet Gateway
- Attached IGW to VPC
- Public Route Table routes 0.0.0.0/0 to IGW

### NAT Gateway
- Created in Public Subnet
- Attached Elastic IP
- Private Route Table routes 0.0.0.0/0 to NAT

---

## EC2 Deployment

- Bastion host deployed in Public Subnet
- App server deployed in Private Subnet
- DB server deployed in Private Subnet

---

## Security Implementation

- Bastion allows SSH from trusted IP only
- App allows SSH only from Bastion
- DB allows traffic only from App

---

## Key Concepts

- Public subnets provide internet accessibility.
- Private subnets improve security.
- NAT Gateway enables outbound internet access.
- Bastion host enables secure administrative access.
- 3-tier architecture separates concerns (Web, App, DB).

---

## Screenshots Included

1. `01-vpc-architecture-overview.png`
2. `02-route-table-configuration.png`
---

## Conclusion

Successfully implemented a secure 3-tier VPC architecture demonstrating networking, security isolation, and controlled access using NAT and Bastion host.