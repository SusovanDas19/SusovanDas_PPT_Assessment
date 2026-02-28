# Task 3 — Attach EBS Volume from Different AZ Using Snapshot

## 📌 Objective

To create a snapshot of an EBS volume and restore it as a new volume in a different Availability Zone, then attach and verify it on another EC2 instance.

---

## 🌍 Overview

Amazon EBS volumes are **Availability Zone specific**, meaning they cannot be directly attached to an EC2 instance in a different AZ.

Snapshots are stored at the **Region level**, which allows restoring a volume in any Availability Zone within the same region.

This task demonstrates cross-AZ volume restoration using EBS snapshots.

---

## 🛠️ Steps Performed

### 1️⃣ Snapshot Creation

- Selected the source EBS volume attached to EC2.
- Created a snapshot from the volume.
- Waited until snapshot status became **Completed**.

---

### 2️⃣ Volume Creation in Different AZ

- Created a new EBS volume from the snapshot.
- Selected a different Availability Zone during volume creation.
- Verified the new volume was created successfully.

---

### 3️⃣ Volume Attachment & Verification

- Attached the new volume to an EC2 instance in the same AZ.
- Verified attachment:

```bash
lsblk
```

- Mounted the main partition:

```bash
sudo mkdir /mnt/task3
sudo mount /dev/nvme1n1p1 /mnt/task3
```

- Verified mount:

```bash
df -h
```

---

## 🔑 Key Concepts

- EBS volumes are AZ-specific.
- Snapshots are stored at the regional level.
- Snapshots capture block-level data, including:
  - Partition table
  - File system
  - Stored data
- Restoring a snapshot recreates the exact disk structure.
- Commonly used for:
  - Backup
  - Migration
  - Disaster Recovery

---

## 📷 Screenshots Included

1. `01-snapshot-created.png`
2. `02-volume-created-in-different-az.png`
3. `03-volume-attached-and-mounted.png`

---

## 🎯 Conclusion

Successfully demonstrated:

- Snapshot creation of an EBS volume  
- Cross-Availability Zone volume restoration  
- Volume attachment and verification  

This task strengthened understanding of:

- AWS storage architecture  
- Cross-AZ data handling  
- Backup and recovery strategies using EBS snapshots  

---

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project