# Static Web Hosting on EC2 (Ubuntu + Nginx)

## 📌 Project Overview
This project demonstrates the deployment of a static website on an AWS EC2 Ubuntu instance using Nginx as the web server.  

The objective was to configure a cloud-based Linux server, install and configure Nginx, and successfully host a static website accessible via the instance's public IP address.

---

## 🎯 Objective

- Launch an EC2 instance (Ubuntu)
- Configure security groups for HTTP access
- Install and configure Nginx
- Deploy a static website
- Verify public accessibility

---



## 🚀 Implementation Steps

### 1️⃣ EC2 Instance Setup

- Launched an Ubuntu EC2 instance.
- Configured Security Group to allow:
  - SSH (Port 22)
  - HTTP (Port 80)

---

### 2️⃣ Server Configuration

Connected to the instance via SSH:

```bash
ssh -i my-key.pem ubuntu@<Public-IP-Address>
```

Updated system packages:

```bash
sudo apt update -y
```

Installed Nginx:

```bash
sudo apt install nginx -y
```

---

### 3️⃣ Website Deployment

Removed default Nginx content:

```bash
sudo rm -rf /var/www/html/*
```

Uploaded static website files to /var/www/html/:

```
sudo git clone https://github.com/SusovanDas19/Todo_Application_Frontend.git
sudo mv Todo_Application_Frontend/* .
```
---

## 📊 Outcome

- Successfully deployed and hosted a static website on AWS EC2
- Verified live accessibility through public IP
- Demonstrated understanding of:
  - Cloud provisioning
  - Linux server configuration
  - Web server setup

---

## 📘 Key Learnings

- EC2 instance provisioning
- Security Group configuration
- Linux server management
- Nginx installation and configuration
- Static website hosting in a cloud environment

---

## 🌐 Author

Developed as part of a Cloud & DevOps practice project.