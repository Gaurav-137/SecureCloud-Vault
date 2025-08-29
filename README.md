# SecureCloud Vault-A Zero Trust File Storage and Access Management System

A security-first file storage system that enforces **least privilege**, **short-lived presigned access**, and **end-to-end auditing** on AWS.

---

## 🌟 Why This Project Matters
Misconfigurations and oversharing are leading causes of cloud data breaches.  
**SecureCloud Vault** demonstrates a pragmatic **Zero Trust** approach for file storage:
- Files are encrypted at rest using **AWS KMS**.
- **Presigned URLs** provide time-bound access (upload/download).
- **Role-Based Access Control (RBAC)** and **audit logging** ensure accountability.
- Every request is **authenticated, authorized, and logged**.

This project showcases **real-world cloud security skills** and can scale from personal projects to enterprise use cases.

---

## 🏗️ Architecture Overview

**Frontend**
- Next.js (hosted on Vercel)
- Authentication with **Cognito** (or Firebase/Azure AD alternative)

**Backend**
- AWS API Gateway + AWS Lambda (stateless APIs)
- Metadata storage in **DynamoDB** (beginner path) or **RDS PostgreSQL** (advanced path)

**Storage & Security**
- **Amazon S3** for file storage
- **SSE-KMS** (server-side encryption with customer-managed keys)
- Presigned URLs for upload/download (short expiry)

**Monitoring**
- **CloudWatch Logs & Metrics**
- **SNS Alerts** on anomalies (suspicious IPs, request spikes)


