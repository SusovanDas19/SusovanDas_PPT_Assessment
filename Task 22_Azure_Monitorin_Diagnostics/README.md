# Task 22 — Azure Monitoring & Diagnostics

## 📌 Objective

To enable monitoring and diagnostics for Azure resources using Azure Monitor.

---

## 🏗️ Architecture

Azure Resource (Storage Account)  
→ Azure Monitor (Metrics & Logs)  
→ Log Analytics Workspace  

This setup enables centralized monitoring, performance tracking, and log collection.

---

## 🛠️ Services Used

- Microsoft Azure
- Azure Monitor
- Log Analytics Workspace
- Azure Storage Account

---

## 🚀 Steps Performed

### 1️⃣ Metrics Monitoring

- Opened **Azure Monitor**.
- Selected target resource:
  - Storage Account
- Viewed performance metrics such as:
  - Transactions
  - Ingress
- Verified graphical visualization of metrics over time.
- Adjusted time range for analysis.

---

### 2️⃣ Diagnostic Settings Configuration

- Opened **Storage Account → Diagnostic Settings**.
- Enabled diagnostic settings.
- Configured destination:
  - Log Analytics Workspace
- Selected monitoring categories (metrics and logs).
- Saved configuration.
- Verified successful activation.

---

## 🔑 Key Concepts

- Azure Monitor provides centralized monitoring for Azure resources.
- Metrics measure performance and operational health.
- Diagnostic settings collect platform logs and metrics.
- Log Analytics Workspace stores and analyzes monitoring data.
- Monitoring improves observability and troubleshooting capability.

---

## 📷 Screenshots Included

1. `01-azure-monitor-metrics.png`
2. `02-diagnostic-settings.png`

---

## 🎯 Conclusion

Successfully enabled monitoring and diagnostics for Azure resources.

This task demonstrates:

- Performance monitoring using Azure Monitor
- Log collection configuration
- Integration with Log Analytics
- Basic observability implementation in Azure