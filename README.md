**DevOps CI/CD Quiz Activity – From Code to Cluster**

**Project Overview**

This project was developed as part of the DevOps Practical Activity (Quiz) for the course Software Construction & Development.

The goal was to implement a complete CI/CD pipeline that automates the process of building, testing, and deploying an application from source code to Kubernetes using industry-standard DevOps tools.

**Pipeline Flow:**
Code → Docker → Jenkins → Kubernetes

Technologies Used

Docker

Docker Compose

Kubernetes

Jenkins

GitHub

Flask (Python)

MySQL

**Project Structure**
project/
├──  app/
│   └── web/
│       ├── app.py
│       ├── Dockerfile
│       └── requirements.txt
|   └── static/
        ├── index.html
├── docker-compose.yml
├── kubernetes/
│   ├── deployment.yaml
│   └── service.yaml
├── Jenkinsfile
└── README.md

**Phase Summary**

**Phase 1 – Docker**

Built and ran Docker images manually

Exposed containers on custom ports

**Phase 2 – Docker + Kubernetes**

Deployed Flask app using Kubernetes Deployment and Service

Verified pods and services using kubectl

**Phase 3 – Docker Compose**

Implemented multi-container app (Flask + MySQL)

Used volumes, depends_on, and logs

**Phase 4 – Jenkins CI/CD**

Automated build, test, and deployment using Jenkins pipeline

Deployment triggered via Jenkinsfile

**Jenkins Pipeline Stages**
Checkout Code → Build Docker Image → Test Image → Deploy to Kubernetes

How to Run

Docker Compose

docker-compose up --build


**Kubernetes Deployment**

kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
kubectl get pods
kubectl get svc


**Jenkins**

Open Jenkins dashboard

Select pipeline job

Click Build Now

Monitor logs and stages

**Verification**

Jenkins pipeline executed successfully

Docker image built correctly

Kubernetes pod updated after deployment

Application accessible via NodePort

**Conclusion**

This project demonstrates a fully functional CI/CD DevOps pipeline, meeting all requirements of CI/CD WAR ZONE (LAB-04) and showcasing practical skills in automation, containerization, orchestration, and debugging.

**Group Members**:

1. Umar Ahmad-BSSE23032
2. Ali Hasnain-BSSE23066
