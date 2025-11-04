# 🧩 DevSecOps Pipeline for Tic Tac Toe Game

A fully automated **DevSecOps CI/CD pipeline** for a containerized **Tic Tac Toe web application**, designed to demonstrate modern DevOps practices — including **continuous integration**, **security scanning**, **container orchestration**, and **continuous deployment** to a **Kubernetes cluster** on **AWS EC2**.

This project integrates the complete DevSecOps toolchain, ensuring every stage of the application lifecycle — from code to deployment — is secure, automated, and observable.

---

## 🚀 Project Overview

The goal of this project is to automate the process of:
1. **Building** the Tic Tac Toe web app using GitHub Actions.
2. **Containerizing** the app with Docker.
3. **Scanning** for vulnerabilities using Trivy.
4. **Pushing** the verified image to GitHub Container Registry (GHCR).
5. **Deploying** the image automatically using Argo CD into a Kubernetes cluster hosted on AWS EC2.

---

## 🧱 Tech Stack

| Layer | Tool / Service | Purpose |
|-------|----------------|----------|
| **Application** | React.js | Frontend Tic Tac Toe Game |
| **Version Control** | Git & GitHub | Source Code Management |
| **CI/CD** | GitHub Actions | Automate Build, Test & Deploy |
| **Containerization** | Docker | Build and run application in isolated environment |
| **Security Scanning** | Trivy | Detect vulnerabilities in Docker images |
| **Orchestration** | Kubernetes (k8s) | Manage containerized applications |
| **Deployment** | Argo CD | GitOps-based Continuous Deployment |
| **Cloud Infrastructure** | AWS EC2 | Host Kubernetes cluster |
| **Monitoring (optional)** | Prometheus / Grafana | Observe cluster and application metrics |

---

## 🔄 Pipeline Architecture

```text
 Developer Commit
       ↓
  GitHub Actions
       ↓
   Docker Build
       ↓
  Trivy Security Scan
       ↓
 GitHub Container Registry (GHCR)
       ↓
  Argo CD (GitOps)
       ↓
 Kubernetes Cluster (AWS EC2)
       ↓
   Deployed Tic Tac Toe App
