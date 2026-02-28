# Task 2 — Disk Partitioning (Ubuntu – MBR & Windows – GPT)

## 📌 Objective

To understand disk structure and perform partition management using:

- **MBR (Master Boot Record)** on Ubuntu
- **GPT (GUID Partition Table)** on Windows

---

## 🐧 Part A — Ubuntu (MBR Partitioning)

### 🛠️ Steps Performed

1. Attached a new **5GB EBS volume** to the Ubuntu EC2 instance.
2. Verified the new disk:

```bash
lsblk
```

3. Created an MBR (DOS) partition table:

```bash
sudo fdisk /dev/nvme1n1
```

- Created a primary partition  
- Saved changes  

4. Formatted the partition:

```bash
sudo mkfs.ext4 /dev/nvme1n1p1
```

5. Created mount directory and mounted the partition:

```bash
sudo mkdir /mnt/task2disk
sudo mount /dev/nvme1n1p1 /mnt/task2disk
```

6. Verified successful mount:

```bash
lsblk
df -h
```

---

### ✅ Result

The new disk was successfully partitioned using **MBR** and mounted on the Ubuntu system.

---

## 🪟 Part B — Windows (GPT Partitioning)

### 🛠️ Steps Performed

1. Launched a Windows EC2 instance.
2. Created and attached a new **5GB EBS volume**.
3. Opened Disk Management:

```
diskmgmt.msc
```

4. Initialized the new disk as:
   - **GPT (GUID Partition Table)**

5. Created a **New Simple Volume**.
6. Formatted the partition as **NTFS**.
7. Assigned a drive letter.

---

### ✅ Result

The disk was successfully initialized as **GPT**, formatted with **NTFS**, and made accessible in Windows.

---

## 📷 Screenshots Included

1. `01-ubuntu-mbr-partition-and-mount.png`
2. `02.1-windows-gpt-before-initialization.png`
3. `02.2-windows-gpt-after-partition-creation.png`

---

## 🎯 Conclusion

Successfully demonstrated disk partitioning using:

- **MBR** on Ubuntu (Linux environment)
- **GPT** on Windows

This task enhanced understanding of:

- Disk structure
- Partition tables (MBR vs GPT)
- Formatting file systems
- Mounting and managing storage volumes

---

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project