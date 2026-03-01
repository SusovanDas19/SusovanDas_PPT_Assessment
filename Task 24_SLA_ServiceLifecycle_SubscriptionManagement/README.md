# Task 24 — SLA, Service Lifecycle & Subscription Management

## 📌 Objective

To understand Azure Service Level Agreements (SLA), service lifecycle stages, and subscription management fundamentals.

---

## 🏗️ Conceptual Overview

Azure Subscription  
→ Azure Services (VM, Storage, Networking, etc.)  
→ SLA Commitments + Lifecycle Stage  
→ Governance & Billing Control  

This task focuses on reliability guarantees, governance structure, and service maturity in Azure.

---

## 🛠️ Services & Areas Covered

- Microsoft Azure Virtual Machines
- Azure Subscription Management
- Azure Service Level Agreements (SLA)
- Azure Service Lifecycle

---

## 🚀 Steps Performed

### 1️⃣ SLA Review

- Reviewed **Azure Virtual Machine SLA** documentation.
- Observed availability commitments:
  - **99.9% uptime** for single VM instance
  - **99.99% uptime** when using Availability Sets
- Understood that higher availability requires redundancy architecture.

---

### 2️⃣ Subscription Management

- Navigated to:
  ```
  Azure Portal → Subscriptions
  ```
- Reviewed subscription details:
  - Subscription Name: **Azure for Students**
  - Status: **Active**
  - Subscription ID
  - Spending Limits
- Understood how subscription governs:
  - Resource access
  - Billing
  - Quotas
  - Policies

---

### 3️⃣ Service Lifecycle Understanding

Explored Azure service lifecycle stages:

- **Preview** – Early access, not production recommended
- **General Availability (GA)** – Fully supported and production-ready
- **Deprecated** – Planned retirement announced
- **Retired** – Service no longer available

Understood how lifecycle stage affects production deployment decisions.

---

## 🔑 Key Concepts

- SLA defines uptime guarantees and reliability commitments.
- Higher availability requires redundancy (Availability Sets or Zones).
- Subscription acts as a billing and governance boundary.
- Service lifecycle stages determine production readiness.
- Governance and SLA awareness are critical for enterprise cloud design.

---

## 📷 Screenshots Included

1. `01-azure-sla.png`
2. `02-subscription-overview.png`

---

## 🎯 Conclusion

Successfully reviewed Azure SLA commitments, subscription details, and service lifecycle stages.

This task demonstrates understanding of:

- Cloud reliability standards
- High availability planning
- Subscription governance
- Service maturity evaluation

These concepts are essential for designing resilient and production-ready cloud architectures.