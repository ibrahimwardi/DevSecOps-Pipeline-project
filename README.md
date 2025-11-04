# 🧩 DevSecOps Pipeline Project: Tic-Tac-Toe Game

## 🏗️ Architecture
<img width="1755" height="634" alt="image" src="https://github.com/user-attachments/assets/97f63ede-91a6-4375-a941-6242c72f4f13" />


This project demonstrates a complete **DevSecOps pipeline** built for a containerized **Tic-Tac-Toe web application**.  
It integrates continuous integration, security scanning, infrastructure automation, and GitOps deployment ensuring a secure, automated, and observable delivery workflow.

---

## 🧰 Tools & Technologies

| Category | Tools |
|-----------|-------|
| **Version Control** | GitHub |
| **CI/CD** | GitHub Actions / Jenkins |
| **Containerization** | Docker |
| **Orchestration** | Kubernetes |
| **GitOps** | ArgoCD |
| **Security Scanning** | Trivy, SonarQube |
| **Infrastructure as Code** | Terraform |
| **Cloud Infrastructure** | AWS EC2 |
| **Monitoring** | ArgoCD Dashboard, kubectl |

---

## ⚙️ Pipeline Overview
![Pipeline Flow](devsecops%205%20good.png)

This pipeline automates:
1. **Code Commit & Build** – Source changes trigger Docker image builds.  
2. **Security Scan** – Images are scanned using Trivy before deployment.  
3. **Push to GHCR (GitHub Container Registry)** – Secure storage for container images.  
4. **Automated Deployment via ArgoCD** – Ensures GitOps-based synchronization between Git and Kubernetes cluster.  

---

## 🚀 Implementation Workflow

### 1️⃣ Source & Build Stage
![Build Process](1a14b784-4144-416c-b94a-28bf37d6983a.png)

- Developers push code to GitHub.
- CI pipeline automatically builds a Docker image.
- **Trivy** performs vulnerability scanning on the image.
- The image is pushed to **GitHub Container Registry**.

### 2️⃣ Security Scanning
- **Trivy** scans Docker images for known vulnerabilities in base images, dependencies, and libraries.
- Pipeline fails automatically if critical vulnerabilities are found.

### 3️⃣ Deployment with ArgoCD
![ArgoCD Dashboard](argocd.png)

- ArgoCD continuously monitors the GitHub repository.  
- When a new image is pushed, it automatically syncs the updated manifest to Kubernetes.  
- Provides real-time visualization of deployments and app status.

### 4️⃣ Infrastructure Provisioning
![EC2 Infrastructure](ec2%20instance.png)

- The entire Kubernetes cluster and supporting infrastructure are provisioned using **Terraform**.  
- Terraform manages the EC2 instance setup, networking, and IAM configurations.  

### 5️⃣ Cluster & Application Status
![Cluster Operations](10f9406b-9174-4156-af8c-3b2ed5557968.png)

- After deployment, the app runs inside the Kubernetes cluster.  
- Kubectl commands validate pod status, services, and ArgoCD sync health.  

### 6️⃣ Monitoring & Continuous Management
![ArgoCD Monitoring 1](37a5578f-1265-461e-99ba-7473b20b321c.png)  
![ArgoCD Monitoring 2](824ae39a-5aea-4177-bf47-afee8a2256ba.png)

- ArgoCD dashboard provides clear visibility into the running applications.  
- Enables rollback, re-deployment, and sync checks.  

---

## 🔐 Security Integration

- **Trivy** ensures only vulnerability-free images reach production.  
- **GitHub Secrets** protect sensitive data such as tokens and credentials.  
- **SonarQube** (optional extension) for static code analysis.  
- Ensures **compliance**, **traceability**, and **security shift-left** principles.

---

## 📊 Results & Observations

- Fully automated CI/CD pipeline integrating security at every stage.  
- GitOps-based delivery ensures consistent and auditable deployments.  
- Terraform IaC simplifies environment setup and teardown.  
- ArgoCD provides instant visibility and rollback capabilities.  

---

## 🧾 Project Summary

This **DevSecOps Pipeline Project** demonstrates end-to-end automation — from code commit to production deployment — with security baked in at every step.  

By combining **GitHub**, **Docker**, **Terraform**, **Trivy**, and **ArgoCD**, the pipeline ensures:  
✅ Reliable CI/CD automation  
✅ Secure image scanning  
✅ Immutable infrastructure provisioning  
✅ Declarative GitOps deployment  

This approach embodies the true **DevSecOps culture**, bridging the gap between development, security, and operations while maintaining agility and compliance.

---


**Ibrahim Wardi**  
📧 *ibrahimwardi233@gmail.com*  
📦 [GitHub Repository](https://github.com/ibrahimwardi/DevSecOps-Pipeline-project)

