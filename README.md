# 🚀 GitOps-Based CI/CD Pipeline with Argo CD on AWS EKS

## 📌 Overview
This project demonstrates a fully automated CI/CD pipeline built using GitOps principles with Argo CD on AWS EKS.  
It enables seamless deployment, high availability, and self-healing infrastructure for containerized applications.

The system continuously synchronizes the desired state from Git repository to Kubernetes cluster, ensuring reliability and consistency across deployments.

---

## 🧰 Tech Stack

- ☁️ Cloud Provider: AWS (EKS, VPC, IAM, ECR)
- ⚙️ Container Orchestration: Kubernetes
- 🔁 GitOps Tool: Argo CD
- 📊 Monitoring & Observability: Prometheus, Grafana
- 🐳 Container Registry: Docker Hub / Amazon ECR
- 📦 CI/CD Approach: Declarative GitOps Workflow

---

## 🏗️ Architecture

Git → Argo CD → Kubernetes Cluster (EKS) → Application Deployment  
Monitoring → Prometheus → Grafana Dashboards

---

## ✨ Key Features & Achievements

- 🚀 99.9% Uptime Achieved through Kubernetes self-healing and health checks
- 🔄 Fully Automated Deployment using GitOps (Git push → Argo CD sync)
- 📊 Real-time Monitoring using Grafana dashboards (CPU, Memory, Pod metrics)
- 🔐 Secure AWS Setup using IAM roles for EKS and ECR access

---

## 📸 Screenshots (Proof of Work)

### Kubernetes Dashboard
Shows active pods, services, and deployments running on EKS.

![Kubernetes Dashboard](screenshots/k8s-dashboard.png)

---

### Argo CD Application Dashboard
Displays GitOps synchronization status and deployment health.

![Argo CD Dashboard](screenshots/argocd-dashboard.png)

---

### kubectl get all Output
Verification of all Kubernetes resources running in the cluster.

![Kubectl Output](screenshots/kubectl-get-all.png)

---

## ⚠️ Challenges & Solutions

### ImagePullBackOff Issue
- Cause: Worker nodes lacked permissions to pull images from private ECR
- Solution: Added IAM policy `AmazonEC2ContainerRegistryReadOnly`

---

### OOMKilled in Prometheus
- Cause: High memory usage due to default configuration
- Solution:
  - Added resource limits and requests
  - Optimized Prometheus retention settings

---

## 📈 Results

- Stable and scalable Kubernetes deployment on AWS EKS
- Fully automated GitOps-based CI/CD workflow using Argo CD
- Real-time observability using Prometheus + Grafana
- Improved system reliability and deployment speed

---

## 📂 Repository Structure
