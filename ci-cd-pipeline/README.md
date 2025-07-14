# CI/CD Pipeline with Docker, GitHub Actions, and Kubernetes

## Overview
This project demonstrates a full CI/CD pipeline for a simple Flask web app using Docker, GitHub Actions, and Kubernetes (Minikube, DigitalOcean DOKS, or Azure AKS).

## Architecture
```
GitHub Repo → GitHub Actions → Docker Build → DockerHub  
           ↓  
       Kubernetes Deployment (DOKS/AKS/Minikube)
```

## Features
- Automated Docker image build and push
- Automated test run
- Automated deployment to Kubernetes
- Production-like, GitOps workflow

## Folder Structure
```
ci-cd-pipeline/
│
├── app/                  # Flask app source code
│   ├── app.py
│   └── requirements.txt
│
├── Dockerfile            # Containerization
├── README.md             # Project documentation
├── k8s/                  # Kubernetes manifests
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
└── .github/workflows/
    └── deploy.yml        # GitHub Actions pipeline
```

## Setup Instructions
1. Clone this repo and navigate to `ci-cd-pipeline/`.
2. Update `<YOUR_DOCKERHUB_USERNAME>` in manifests and workflow files.
3. Set up GitHub Secrets for `DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN`.
4. Push to `main` branch to trigger the pipeline.
5. Deploy to your Kubernetes cluster (Minikube, DOKS, or AKS).

---

Feel free to expand this README with more details as you progress!
