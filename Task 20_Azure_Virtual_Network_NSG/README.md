# Task 20 — Azure Virtual Network (Basic Networking Practical)

## 📌 Objective

To configure a Virtual Network (VNet), create subnets, and apply Network Security Group (NSG) rules in Microsoft Azure.

---

## 🏗️ Architecture

**Virtual Network:**  
```
task20-vnet
```

**Address Space:**  
```
10.0.0.0/16
```

### Subnets

- `web-subnet` → 10.0.1.0/24  
- `app-subnet` → 10.0.2.0/24  

### Network Security Group

- `task20-nsg`
- Inbound Rule:
  - Allow HTTP (Port 80)

---

## 🛠️ Services Used

- Microsoft Azure
- Virtual Network (VNet)
- Subnets
- Network Security Group (NSG)

---

## 🚀 Steps Performed

### 1️⃣ Virtual Network Creation

- Created VNet:
  ```
  task20-vnet
  ```
- Configured address space:
  ```
  10.0.0.0/16
  ```

---

### 2️⃣ Subnet Configuration

- Created subnet:
  - `web-subnet` → 10.0.0.0/27
- Created subnet:
  - `app-subnet` → 10.0.2.0/24

These subnets logically separate web and application layers.

---

### 3️⃣ Network Security Group Creation

- Created NSG:
  ```
  task20-nsg
  ```

---

### 4️⃣ NSG Rule Configuration

- Configured inbound security rule:
  - Protocol: TCP
  - Port: 80
  - Action: Allow
  - Source: Any (or restricted IP if configured)

---

### 5️⃣ NSG Association

- Associated `task20-nsg` with:
  - `web-subnet`

This enables HTTP access to resources inside the web subnet.

---

## 🔑 Key Concepts

- VNet provides an isolated virtual network in Azure.
- Subnets logically divide the network for layered architecture.
- NSG controls inbound and outbound traffic at subnet or NIC level.
- CIDR notation defines IP address ranges.
- Network segmentation improves security and organization.

---

## 📷 Screenshots Included

1. `01-vnet-subnets.png`
2. `02-nsg-rule.png`

---

## 🎯 Conclusion

Successfully configured basic cloud networking components in Azure, demonstrating:

- Virtual Network setup
- Subnet segmentation
- Network Security Group configuration
- Traffic rule implementation

This task strengthens understanding of foundational Azure networking concepts.