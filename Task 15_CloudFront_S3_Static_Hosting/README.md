# Task 15 — CloudFront Distribution for S3 Static Website

## 📌 Objective

To configure Amazon CloudFront as a Content Delivery Network (CDN) for an S3 static website in order to enable global content delivery with low latency and improved performance.

---

## 🌍 Architecture

User → CloudFront Edge Location → S3 Bucket (Origin)

CloudFront caches content at edge locations worldwide, reducing latency and improving availability.

---

## 🛠️ Services Used

- Amazon S3
- Amazon CloudFront

---

## 🚀 Steps Performed

### 1️⃣ S3 Static Website Setup

- Created an S3 bucket.
- Enabled **Static Website Hosting**.
- Uploaded:
  - `index.html`
  - CSS, JS, and asset files
- Configured bucket permissions for public access (if applicable).
- Verified website using S3 website endpoint.

---

### 2️⃣ CloudFront Distribution Creation

- Created a new CloudFront distribution.
- Selected the S3 bucket as the **Origin**.
- Configured:
  - Default Root Object: `index.html`
  - Viewer Protocol Policy: Redirect HTTP to HTTPS
- Left other settings as default (unless customized).
- Created distribution and waited for deployment status to become **Deployed**.

---

### 3️⃣ Testing & Verification

- Accessed the website using the CloudFront domain name.
- Verified:
  - Website loads successfully.
  - Content is delivered via HTTPS.
  - Improved performance through CDN caching.

---

## 🔑 Key Concepts

- CloudFront is a global CDN service.
- Uses edge locations to cache content closer to users.
- Reduces latency and improves performance.
- Supports HTTPS for secure content delivery.
- Integrates seamlessly with S3 as origin.

---

## 📷 Screenshots Included

1. `01-cloudfront-distribution.png`
2. `02-cloudfront-website-proof.png`

---

## 🎯 Conclusion

Successfully implemented global content delivery using CloudFront CDN for an S3 static website.

This task demonstrates:

- CDN configuration in AWS
- Performance optimization techniques
- Secure HTTPS content delivery
- Distributed web architecture principles

---

## 👤 Author

Susovan Das
Cloud & DevOps Practice Project