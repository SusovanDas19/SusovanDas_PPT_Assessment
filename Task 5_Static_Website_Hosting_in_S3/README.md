# Task 5 — Static Website Hosting using Amazon S3

## Objective
To host a static website using Amazon S3 without using EC2 instances.

---

## Steps Performed

### 1. Bucket Creation
- Created a new S3 bucket with a globally unique name.
- Disabled Block Public Access.

### 2. Website File Upload
- Uploaded index.html and related static files.

### 3. Static Hosting Configuration
- Enabled Static Website Hosting in bucket properties.
- Set index document as `index.html`.

### 4. Public Access Configuration
- Added bucket policy to allow public read access (`s3:GetObject`).

### 5. Verification
- Accessed the S3 website endpoint.
- Confirmed website loads successfully.

---

## Key Concepts

- S3 provides serverless static website hosting.
- Bucket policy is required to allow public access.
- Highly scalable and cost-effective hosting solution.
- Suitable for frontend-only applications.

---

## Screenshots Included

1. `01-s3-static-hosting-enabled.png`
2. `02-s3-website-output.png`

---

## Conclusion

Successfully hosted a static website using Amazon S3, demonstrating serverless web hosting capability in AWS.

## 👤 Author

Susovan Das  
Cloud & DevOps Practice Project