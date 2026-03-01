# Task 17 — DynamoDB Table Creation (Basic)

## 📌 Objective

To create a NoSQL database table using Amazon DynamoDB and insert sample items to verify data storage and retrieval.

---

## 🏗️ Architecture

Application → DynamoDB Table → NoSQL Storage

This setup demonstrates serverless NoSQL database provisioning and data insertion using AWS.

---

## 🛠️ Services Used

- Amazon DynamoDB
- AWS Management Console

---

## 🚀 Steps Performed

### 1️⃣ Table Creation

- Created DynamoDB table: `Task17-Users`
- Partition Key:
  - `userId` (String)
- Capacity Mode:
  - **On-demand**
- Waited until table status became **Active**.

---

### 2️⃣ Data Insertion

- Navigated to **Explore Table Items**.
- Inserted a new item using JSON format.
- Saved the item.
- Verified successful storage in the table.

---

## 📄 Sample Item Inserted

```json
{
  "userId": "U001",
  "name": "Susovan DAS",
  "age": 22,
  "city": "Kolkata"
}
```

---

## 🔑 Key Concepts

- DynamoDB is a fully managed NoSQL database service.
- Uses key-value and document data models.
- Requires a primary key (Partition Key).
- On-demand mode automatically scales based on traffic.
- Provides high availability and low latency.

---

## 📷 Screenshots Included

1. `01-dynamodb-table-created.png`
2. `02-item-inserted.png`

---

## 🎯 Conclusion

Successfully created and configured a DynamoDB table and inserted sample data.

This task demonstrates:

- NoSQL database provisioning
- Table schema configuration
- JSON-based data insertion
- Basic serverless database operations in AWS

---
