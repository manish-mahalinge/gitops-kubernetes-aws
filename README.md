# GitOps-Based CI/CD Pipeline using Argo CD on AWS EKS

## Overview
Engineered a declarative CI/CD pipeline using Argo CD and GitOps principles to manage containerized applications on AWS EKS. The system ensures high availability, scalability, and automated synchronization between Git repository and Kubernetes cluster.

---

## Technical Stack
- Cloud: AWS (EKS, VPC, IAM, ECR)
- Orchestration: Kubernetes
- GitOps Tool: Argo CD
- Observability: Prometheus, Grafana

---

## Key Achievements
- 99.9% availability achieved using Kubernetes self-healing and health checks
- Real-time monitoring using Grafana dashboards for cluster performance
- Fully automated GitOps deployment workflow (Git → Argo CD → Kubernetes)
- Stable multi-service microservices deployment on Kubernetes

---

## Architecture Flow
Git Repository → Argo CD → AWS EKS Cluster → Application Deployment  
Monitoring → Prometheus → Grafana

---

## Screenshots

### Kubernetes Monitoring Dashboard
![Kubernetes Dashboard](sandbox:/mnt/data/Screenshot%20(86).png)

### kubectl Cluster State
![kubectl output](sandbox:/mnt/data/Screenshot%20(89).png)

### Argo CD Application Sync
![Argo CD Dashboard](sandbox:/mnt/data/Screenshot%20(83).png)

---

## Challenges & Troubleshooting

### ImagePullBackOff
- Cause: Missing IAM permissions for ECR access in worker nodes
- Fix: Attached AmazonEC2ContainerRegistryReadOnly policy to EKS node role

---

### OOMKilled in Prometheus
- Cause: High memory consumption due to default configuration
- Fix:
  - Added resource requests and limits
  - Optimized Prometheus retention settings

---

## Result
- Fully automated GitOps-based CI/CD pipeline
- Stable and scalable Kubernetes deployment on AWS EKS
- Improved observability, reliability, and deployment efficiency
