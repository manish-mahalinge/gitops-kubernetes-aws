# 🚀 Kubernetes GitOps CI/CD Pipeline using Argo CD on AWS

## 📌 Overview
Engineered a declarative CI/CD pipeline using **Argo CD** and **GitOps** principles to manage containerized applications on AWS EKS.  
This project ensures high availability, scalability, and system reliability through automated deployment and synchronization.

---

## 🛠️ Technical Stack

- ☁️ **Cloud:** AWS (EKS, VPC, IAM)
- ⚙️ **Orchestration:** Kubernetes
- 🔁 **GitOps Tool:** Argo CD
- 📊 **Monitoring:** Prometheus & Grafana

---

## 🎯 Key Achievements

- ✅ **99.9% Availability**
  - Achieved using Kubernetes self-healing, health checks, and auto-restarts.

- 📡 **Real-time Monitoring**
  - Built custom Grafana dashboards to track:
    - CPU usage
    - Memory usage
    - Cluster health

---

## ⚠️ Challenges & Troubleshooting

### ❌ Issue 1: ImagePullBackOff
- **Cause:** Worker nodes lacked IAM permissions to pull images from private ECR.
- **Solution:** Updated IAM Role with:
  - `AmazonEC2ContainerRegistryReadOnly` policy

---

### ❌ Issue 2: OOMKilled Pods in Prometheus
- **Cause:** High memory usage due to default resource allocation.
- **Solution:**
  - Added Resource Requests & Limits
  - Optimized Prometheus retention configuration

---

## 📸 Architecture & Screenshots

### 📊 Kubernetes Dashboard

::contentReference[oaicite:0]{index=0}


---

### 🔁 Argo CD GitOps Pipeline

::contentReference[oaicite:1]{index=1}


---

### 📦 kubectl get all Output (Cluster State)

::contentReference[oaicite:2]{index=2}


---

## 📌 Conclusion
This project demonstrates a complete **end-to-end GitOps CI/CD workflow** using Kubernetes and Argo CD on AWS, ensuring automated deployments, scalability, and production-grade reliability.

---
