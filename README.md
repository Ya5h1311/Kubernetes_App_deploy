# 💬 Full Stack Chat Application - Kubernetes Deployment

A production-style deployment of a **Full Stack Chat Application** built using the **MERN Stack** and deployed on a **Kubernetes (Kind) cluster** hosted on **AWS EC2**.

This project demonstrates how to containerize a three-tier application using Docker and orchestrate it with Kubernetes by implementing Deployments, Services, Persistent Volumes, Secrets, and Ingress for scalable and reliable application deployment.

## 🚀 Tech Stack

- **Frontend:** React.js
- **Backend:** Node.js, Express.js
- **Database:** MongoDB
- **Containerization:** Docker
- **Orchestration:** Kubernetes (Kind)
- **Cloud:** AWS EC2
- **Ingress:** NGINX Ingress Controller

## 📂 Project Structure

```
full-stack_chatApp/
├── backend/
├── frontend/
├── k8s/
│   ├── namespace.yml
│   ├── mongodb-pv.yml
│   ├── mongodb-pvc.yml
│   ├── mongo-db-deployment.yml
│   ├── mongodb-service.yml
│   ├── backend-deployment.yml
│   ├── backend-service.yml
│   ├── frontend-deployment.yml
│   ├── frontend-service.yml
│   ├── ingress.yml
│   └── secrets.yml
├── docker-compose.yml
└── README.md
```

## ⚙️ Kubernetes Resources Used

- Namespace
- Deployments
- Services (ClusterIP)
- Persistent Volume (PV)
- Persistent Volume Claim (PVC)
- Secrets
- Ingress
- Labels & Selectors

## 🏗️ Architecture

```
                   Internet
                       │
                NGINX Ingress
                       │
        ┌──────────────┴──────────────┐
        │                             │
 Frontend Service              Backend Service
        │                             │
   Frontend Pod               Backend Pod
                                     │
                              MongoDB Service
                                     │
                                MongoDB Pod
                                     │
                                 PV + PVC
```

## ✨ Key Highlights

- Dockerized React and Node.js applications using multi-stage builds.
- Deployed a complete three-tier MERN application on a Kubernetes Kind cluster.
- Implemented Kubernetes Deployments and ClusterIP Services for application components.
- Configured Persistent Volumes and Persistent Volume Claims for MongoDB data persistence.
- Managed sensitive configuration using Kubernetes Secrets.
- Exposed the application through an NGINX Ingress Controller with path-based routing.
- Hosted and tested the Kubernetes cluster on an AWS EC2 instance.
- Performed end-to-end debugging of Kubernetes networking, storage, DNS resolution, and container startup issues.

## 📚 Skills Demonstrated

- Docker
- Kubernetes
- AWS EC2
- NGINX Ingress
- Kubernetes Networking
- Persistent Storage (PV/PVC)
- Secrets Management
- Container Debugging
- Microservices Deployment
- DevOps Troubleshooting

---
