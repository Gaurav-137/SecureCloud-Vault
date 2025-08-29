# SecureCloud Vault - A Zero Trust File Storage and Access Management System

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

## 🔐 Key Security Principles

- **Zero Trust** → every request is re-authenticated & authorized
- **Encryption by Default** → files encrypted at rest & in transit
- **Least Privilege IAM** → Lambda roles scoped only to bucket & KMS key
- **Short-lived Access** → presigned URLs expire in seconds
- **Auditability** → every upload/share/download logged & monitored

---

<!--## 🚀 Demo Scenarios (for recruiters/interviewers)

1. **Upload a File** → Presigned PUT URL → Encrypted in S3 (verify via metadata).
2. **Time-Bound Share** → Share with another user for 2 minutes → Attempt after expiry → Access Denied.
3. **Audit Logs** → Admin views recent file actions and anomalies.
4. **Anomaly Detection** → Trigger multiple downloads → SNS alert sent to user + admin.

---  -->

## ⚙️ Tech Stack

- **Cloud:** AWS (S3, KMS, IAM, API Gateway, Lambda, DynamoDB/RDS, CloudWatch, SNS)
- **Frontend:** Next.js (React), hosted on Vercel
- **Authentication:** Amazon Cognito (or Firebase)
- **Database:** DynamoDB (serverless) or PostgreSQL (RDS)
- **Infrastructure as Code (optional):** Terraform / CloudFormation
- **CI/CD (optional):** GitHub Actions with IaC scanning (Checkov/Tfsec)

---

## 📈 Future Enhancements

- Replace heuristic anomaly detection with **GuardDuty + ML-based UBA**.
- Multi-cloud extension (Azure Blob + Key Vault, GCP Storage + KMS).
- SCIM/IdP integration for enterprise identity management.

---

## 🙋 About the Author
**Gaurav Lad** 
- Passionate about **Cloud Security, AI/ML, and Scalable Web Applications**  
- 📩 Email: ladgaurav601@gmail.com  
- 🌐 [LinkedIn](https://www.linkedin.com/in/gaurav-lad137) | [GitHub](https://github.com/Gaurav-137)

---
