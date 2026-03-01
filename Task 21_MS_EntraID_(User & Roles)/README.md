# Task 21 — Microsoft Entra ID (Users & Roles)

## 📌 Objective

To create users and assign roles using Microsoft Entra ID for identity and access management in Azure.

---

## 🏗️ Architecture

User (Identity) → Microsoft Entra ID → Azure RBAC → Subscription Resources

This demonstrates identity management and role-based access control in Azure.

---

## 🛠️ Services Used

- Microsoft Entra ID
- Azure Subscription
- Azure Role-Based Access Control (RBAC)
- Access Control (IAM)

---

## 🚀 Steps Performed

### 1️⃣ User Creation

- Navigated to **Microsoft Entra ID**.
- Selected **Users → New User**.
- Created new user:
  ```
  Student User
  ```
- Assigned:
  - Username
  - Temporary password
- Verified successful user creation.

---

### 2️⃣ Role Assignment

- Navigated to:
  ```
  Subscription → Access Control (IAM)
  ```
- Clicked **Add Role Assignment**.
- Selected Role:
  - **Reader**
- Assigned role to:
  - Student User
- Verified successful role assignment.

---

## 🔑 Key Concepts

- Microsoft Entra ID manages identities and authentication in Azure.
- RBAC (Role-Based Access Control) defines permission levels.
- Reader role provides view-only access to resources.
- IAM ensures secure and controlled access to cloud resources.
- Least privilege principle enhances security posture.

---

## 📷 Screenshots Included

1. `01-entra-user-created.png`
2. `02-role-assigned.png`

---

## 🎯 Conclusion

Successfully implemented identity management by:

- Creating a new user in Microsoft Entra ID
- Assigning appropriate RBAC permissions
- Verifying access control configuration

This task demonstrates foundational access management and security principles in Azure.