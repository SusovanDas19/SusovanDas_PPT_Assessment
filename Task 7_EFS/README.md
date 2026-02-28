# Task 7 — Create EFS and Connect to Multiple Ubuntu Instances

## Objective
To create an Amazon EFS file system and mount it across multiple Ubuntu EC2 instances to demonstrate shared storage.

---

## Steps Performed

### 1. EC2 Setup
- Launched two Ubuntu EC2 instances in the same VPC.
- Configured Security Group to allow NFS (Port 2049).

### 2. EFS Creation
- Created a new EFS file system.
- Verified mount targets were available.

### 3. Mounting EFS
- Installed NFS client (nfs-common) on both instances.
- Created mount directory `/mnt/efs`.
- Mounted EFS using NFS command.

### 4. Verification
- Created a file on Instance 1.
- Verified same file was visible on Instance 2.

---

## Key Concepts

- EFS is a scalable shared file system.
- Supports mounting across multiple EC2 instances.
- Uses NFS protocol.
- Automatically scales storage capacity.

---

## Screenshots Included

1. `01-efs-created.png`
2. `02-efs-file-created.png`
3. `03-efs-shared-proof.png`

---

## Conclusion

Successfully demonstrated shared storage using Amazon EFS across multiple EC2 instances, validating scalable and distributed file system capabilities in AWS.

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project