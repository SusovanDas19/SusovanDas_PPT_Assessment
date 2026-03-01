# Task 19 — Azure Storage Account (Blob, File, Table)

## 📌 Objective

To create an Azure Storage Account and explore multiple storage services including Blob Storage, File Share, and Table Storage.

---

## 🏗️ Architecture

User/Application → Azure Storage Account  
→ Blob Storage (Object)  
→ File Share (Managed File Storage)  
→ Table Storage (NoSQL Data)

This demonstrates Azure’s unified storage architecture within a single storage account.

---

## 🛠️ Services Used

- Microsoft Azure
- Azure Storage Account
- Blob Storage
- Azure File Share
- Table Storage

---

## 🚀 Steps Performed

### 1️⃣ Storage Account Creation

- Created Storage Account:
  ```
  susovanstorage19
  ```
- Performance Tier:
  - **Standard**
- Redundancy:
  - **LRS (Locally Redundant Storage)**
- Resource Group:
  ```
  susovan-azure-t18-t24-rg
  ```
- Deployment completed successfully.

---

### 2️⃣ Blob Storage

- Created Blob Container:
  ```
  sample-container
  ```
- Uploaded sample file.
- Verified successful upload and accessibility.

---

### 3️⃣ File Share

- Created File Share:
  ```
  sample-fileshare
  ```
- Verified share creation under File Service.

---

### 4️⃣ Table Storage

- Created Table:
  ```
  sampletable
  ```
- Verified successful creation under Table Service.

---

## 🔑 Key Concepts

- Azure Storage Account acts as a unified storage container.
- Blob Storage is used for object storage (images, videos, backups).
- File Share provides fully managed file storage accessible via SMB.
- Table Storage supports NoSQL structured data.
- LRS ensures data is replicated within a single data center.

---

## 📷 Screenshots Included

1. `01-storage-account-created.png`
2. `02-blob-upload.png`
3. `03-file-table-created.png`

---

## 🎯 Conclusion

Successfully created and explored multiple Azure Storage services within a single Storage Account.

This task demonstrates:

- Multi-service storage architecture
- Object storage management
- Managed file share setup
- NoSQL table storage provisioning
- Basic Azure storage configuration knowledge