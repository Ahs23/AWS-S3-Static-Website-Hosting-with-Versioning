# 🚀 AWS S3 Static Website Hosting with Versioning

This project demonstrates how to host a **static website using Amazon S3**, enable **bucket versioning**, and manage **multiple versions of the same file** (`index.html`) without overwriting previous content.

It is designed as a **hands-on AWS fundamentals project** showcasing storage, access control, and version management best practices.

---

## 📌 Project Overview

In this project, I:

- Created an Amazon S3 bucket from scratch
- Hosted a static website using S3 Static Website Hosting
- Configured public read access using a **bucket policy (ACLs disabled)**
- Enabled **S3 Versioning**
- Uploaded multiple versions of the same `index.html` file
- Verified and displayed object version history
- Demonstrated how S3 preserves older versions automatically

---

## 🧱 Architecture

**Flow:**
1. User accesses the S3 static website endpoint
2. Amazon S3 serves the `index.html` file
3. When the file is updated and re-uploaded, S3 stores a new version
4. Older versions remain available for rollback or auditing

---

## ⚙️ AWS Services Used

- **Amazon S3**
  - Static Website Hosting
  - Bucket Versioning
  - Bucket Policies
  - Same-region replication (optional extension)

---

## 🔐 Security & Access Configuration

- **ACLs disabled** (Bucket owner enforced)
- Public access provided **only via bucket policy**
- Read-only access (`s3:GetObject`)
- No write, delete, or list permissions exposed publicly

---

## 📂 Project Structure

AWS-S3-Static-Website-Versioning/
│
├── index.html # Same file used for Version 1 and Version 2
├── README.md
└── screenshots/ # (Optional) Console & website screenshots

yaml

---

## 🔁 S3 Versioning Demonstration

### Version 1
- Initial upload of `index.html`
- Displays **Version 1.0** on the website

### Version 2
- Same file (`index.html`) edited and re-uploaded
- Displays **Version 2.0**
- S3 automatically stores the previous version

✔ No file renaming  
✔ No overwriting  
✔ Same object key, multiple versions

---

## 🧪 How to Verify Versioning

1. Go to **S3 → Bucket → Objects**
2. Enable **Show versions**
3. Observe multiple entries for `index.html`, each with a unique Version ID

---

## 💡 Key Learnings

- S3 versioning works at the **object key level**
- Versioning must be enabled **before uploading objects**
- ACLs are legacy and should be disabled
- Bucket policies are the preferred way to manage public access
- Static websites can be hosted directly from S3 without servers

---

## 🎯 Real-World Use Cases

- Portfolio websites
- Documentation hosting
- Resume websites
- Backup & rollback protection
- Audit and change tracking
Author-Arman Shaikh
