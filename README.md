# 🧩 DevSecOps Pipeline Project: Tic-Tac-Toe Game

## 🏗️ Architecture
![DevSecOps Pipeline Overview](devsecops%208.png)

This project demonstrates a complete **DevSecOps pipeline** built for a containerized **Tic-Tac-Toe web application**.  
It integrates continuous integration, security scanning, infrastructure automation, and GitOps deployment — ensuring a secure, automated, and observable delivery workflow.

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

<img width="1846" height="794" alt="DevSecOps 1" src="https://github.com/user-attachments/assets/3f987f82-ebeb-406b-90c3-6ea32bb3f3ad" />

This pipeline automates:
1. **Code Commit & Build** – Source changes trigger Docker image builds.  
2. **Security Scan** – Images are scanned using Trivy before deployment.  
3. **Push to GHCR (GitHub Container Registry)** – Secure storage for container images.  
4. **Automated Deployment via ArgoCD** – Ensures GitOps-based synchronization between Git and Kubernetes cluster.  

---

## 🚀 Implementation Workflow

### 1️⃣ Source & Build Stage

- Developers push code to GitHub.
- CI pipeline automatically builds a Docker image.
- **Trivy** performs vulnerability scanning on the image.
- The image is pushed to **GitHub Container Registry**.

### 2️⃣ Security Scanning
- **Trivy** scans Docker images for known vulnerabilities in base images, dependencies, and libraries.
- Pipeline fails automatically if critical vulnerabilities are found.

### 3️⃣ Deployment with ArgoCD

<img width="1191" height="397" alt="argocd" src="https://github.com/user-attachments/assets/4fead8f6-47d2-4814-a231-38ed25ace8ad" />

- ArgoCD continuously monitors the GitHub repository.  
- When a new image is pushed, it automatically syncs the updated manifest to Kubernetes.  
- Provides real-time visualization of deployments and app status.

### 4️⃣ Infrastructure Provisioning

<img width="1857" height="909" alt="ec2 instance" src="https://github.com/user-attachments/assets/be322346-aa59-435e-8019-9aeb1fee4f8c" />

- The entire Kubernetes cluster and supporting infrastructure are provisioned using **Terraform**.  
- Terraform manages the EC2 instance setup, networking, and IAM configurations.  

### 5️⃣ Cluster & Application Status
<img width="1918" height="1020" alt="devsecops 8" src="https://github.com/user-attachments/assets/3f4123f2-c69b-478a-8319-28cec0be60ab" />


- After deployment, the app runs inside the Kubernetes cluster.  
- Kubectl commands validate pod status, services, and ArgoCD sync health.  

### 6️⃣ Monitoring & Continuous Management


<img width="1191" height="397" alt="argocd" src="https://github.com/user-attachments/assets/52482385-4f1d-4903-b142-559c91519e48" />

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


<img width="1845" height="896" alt="devsecops 5 good" src="https://github.com/user-attachments/assets/e35ed42a-57bc-4627-8296-4239270efbcb" />

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

### 👨‍💻 Author
**Ibrahim Wardi**  
📧 *ibrahimwardi233@gmail.com*  
📦 [GitHub Repository](https://github.com/ibrahimwardi/DevSecOps-Pipeline-project)
