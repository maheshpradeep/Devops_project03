# Static Website – DevOps Learning Project on AWS ☁️🚀

This repository documents the **DevOps workflow** I followed to host a static HTML/CSS website using **AWS S3 + CloudFront**, and fully automate deployment via **GitHub Actions CI/CD**.

The goal was to understand **serverless architecture**, use a **global CDN (CloudFront)**, and practice **CI/CD automation** — all using AWS free-tier services.

---

## 📌 Project Goal

✅ Host a static website (HTML + CSS)  
✅ Enable HTTPS using AWS CloudFront  
✅ Learn about CDN and caching behavior  
✅ Automate deployments using GitHub Actions  

---

## 🚀 Project Summary

| **Category**     | **Description**                             |
|------------------|---------------------------------------------|
| App              | Static Website (HTML, CSS)                  |
| Host             | AWS S3 (Static Website Hosting)             |
| CDN              | AWS CloudFront (HTTPS + Caching)            |
| Deployment       | Automated with GitHub Actions               |
| Access Control   | IAM user + GitHub Secrets                   |
| CI/CD Flow       | Push to GitHub → Deploy to S3 + Invalidate CDN |

---

## 📚 Phase-by-Phase DevOps Journey

### ✅ Phase 1 – Setup and Hosting with S3
- Created an S3 bucket for website files
- Enabled static website hosting
- Uploaded `index.html`, CSS, etc.
- Verified it via the public S3 website URL

### ✅ Phase 2 – Global Delivery with CloudFront
- Created CloudFront distribution linked to the S3 bucket
- Configured HTTPS and caching policies
- Accessed site through the secure CloudFront URL
- Learned how to handle **cache invalidation**

### ✅ Phase 3 – CI/CD with GitHub Actions
- Created `.github/workflows/deploy.yml` file
- Set up GitHub Secrets for AWS credentials
- On every push to `main`:
  - Syncs files to S3
  - Automatically invalidates CloudFront cache
- Deployment and updates are now **fully automated**

---

## 📁 Repository Files

| File / Folder            | Purpose                                     |
|--------------------------|---------------------------------------------|
| `index.html`             | Website homepage                            |
| `styles.css`             | CSS styling                                 |
| `.github/workflows/`     | Contains GitHub Actions CI/CD YAML file     |
| `deploy.yml`             | Automates S3 upload and CloudFront invalidation |

---

## 📌 DevOps Tools and Skills Practiced

- **AWS S3** – static website hosting  
- **CloudFront** – CDN for global delivery + HTTPS  
- **GitHub Actions** – CI/CD automation pipeline  
- **IAM** – secure access control using policies  
- **AWS CLI** – used in GitHub Actions to deploy + invalidate CDN  
- **Secrets Management** – GitHub Secrets for credentials  

---

## 🔒 Security Considerations

- Used IAM user with limited permissions (S3 + CloudFront only)
- Stored all AWS credentials securely in GitHub Secrets
- Avoided hardcoding keys or region in code

---

## 🌐 Live URL

👉 [https://d293dltozjus3r.cloudfront.net/](https://d293dltozjus3r.cloudfront.net/)

---

