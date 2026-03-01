# Task 18 — Azure Virtual Machine (Basic)

## 📌 Objective

To launch and configure a basic Azure Virtual Machine and access it securely via SSH.

---

## 🏗️ Architecture

User → Public IP → Azure Virtual Machine → Ubuntu Server

This setup demonstrates basic Infrastructure as a Service (IaaS) deployment in Microsoft Azure.

---

## 🛠️ Services Used

- Microsoft Azure
- Azure Virtual Machine
- Resource Group
- Network Security Group (NSG)
- SSH

---

## 🚀 Steps Performed

### 1️⃣ Resource Setup

- Created new Resource Group:
  ```
  task18-rg
  ```
- Selected Image:
  - **Ubuntu Server 22.04 LTS**
- Selected VM Size:
  - **Standard B2as v2**

---

### 2️⃣ Authentication Configuration

- Configured **password-based authentication**
- Opened inbound port:
  - **SSH (Port 22)** in Network Security Group

---

### 3️⃣ Deployment

- Successfully deployed the Virtual Machine.
- Retrieved the assigned **Public IP Address**.
- Verified VM status as **Running**.

---

### 4️⃣ Access via SSH

Connected to the VM using:

```bash
ssh azureuser@<public-ip>
```

Successfully accessed the Ubuntu server through SSH.

---

## 🔑 Key Concepts

- Azure VM provides Infrastructure as a Service (IaaS).
- Resource Groups logically organize Azure resources.
- Public IP enables remote connectivity.
- Network Security Group (NSG) controls inbound and outbound traffic.
- SSH provides secure remote access to Linux systems.

---

## 📷 Screenshots Included

1. `01-azure-vm-created.png`
2. `02-ssh-connected.png`

---

## 🎯 Conclusion

Successfully launched and accessed an Azure Virtual Machine, demonstrating:

- Basic Azure resource provisioning
- VM configuration
- Network security configuration
- Secure remote access via SSH

This task establishes foundational knowledge of Azure compute services.