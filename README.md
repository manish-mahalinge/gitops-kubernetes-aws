# GitOps-Based CI/CD Pipeline using Argo CD on AWS EKS

## Overview
Engineered a declarative CI/CD pipeline using Argo CD and GitOps principles to manage containerized applications on AWS EKS. This project ensures high availability and system reliability through automated synchronization between Git and Kubernetes cluster.

---

## Technical Stack
- Cloud: AWS (EKS, VPC, IAM, ECR)
- Orchestration: Kubernetes
- GitOps Tool: Argo CD
- Observability: Prometheus, Grafana

---

## Key Achievements
- 99.9% Availability achieved through Kubernetes self-healing, health checks, and workload orchestration.
- Real-time monitoring implemented using Grafana dashboards for CPU, memory, and cluster health visibility.
- Automated deployment workflow using GitOps (Git → Argo CD → Kubernetes).

---

## Architecture Flow
Git Repository → Argo CD → AWS EKS Cluster → Application Deployment  
Monitoring Layer → Prometheus → Grafana

---

## Screenshots

### Kubernetes Dashboard
![Kubernetes Dashboard](screenshots/k8s-dashboard.png)

### Argo CD Application Dashboard
![Argo CD Dashboard](screenshots/argocd-dashboard.png)

### kubectl get all Output
![Kubectl Output](screenshots/kubectl-get-all.png)

---

## Challenges & Troubleshooting

### ImagePullBackOff Error
- Cause: Worker nodes did not have permission to pull images from private ECR.
- Solution: Added IAM policy AmazonEC2ContainerRegistryReadOnly to node role.

### OOMKilled Pods in Prometheus
- Cause: High memory usage due to default resource configuration.
- Solution: Implemented resource requests/limits and optimized retention settings.

---

## Result
- Fully automated CI/CD pipeline using GitOps
- Stable Kubernetes deployment on AWS EKS
- Improved reliability, scalability, and deployment consistency
