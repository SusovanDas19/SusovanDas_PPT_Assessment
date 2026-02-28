# Task 6 — S3 Replication and Lifecycle Policy

## Objective
To configure S3 versioning, replication, and lifecycle rules to demonstrate backup strategy and cost optimization.

---

## Steps Performed

### 1. Bucket Creation
- Created a Source bucket.
- Created a Destination bucket in a different region.

### 2. Versioning
- Enabled versioning on both buckets.

### 3. Replication Configuration
- Created a replication rule in the Source bucket.
- Selected Destination bucket.
- Configured IAM role automatically.
- Uploaded a test file and verified replication.

### 4. Lifecycle Policy
- Created a lifecycle rule.
- Configured transition to Glacier after 30 days.
- Configured expiration rule (optional).

---

## Key Concepts

- Versioning protects against accidental deletion.
- Replication enables disaster recovery.
- Lifecycle policies reduce storage cost.
- Glacier storage class is cost-effective for long-term backups.

---

## Screenshots Included

1. `01-s3-replication-rule.png`
2. `02-s3-replication-proof.png`
3. `03-s3-lifecycle-policy.png`

---

## Conclusion

Successfully configured S3 replication and lifecycle rules, demonstrating cost optimization and backup strategy in AWS.

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project