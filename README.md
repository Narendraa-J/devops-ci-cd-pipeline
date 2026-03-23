# 🚀 CI/CD Pipeline using Jenkins, Docker & AWS EC2

## 📌 Project Overview

This project demonstrates an end-to-end CI/CD pipeline that automates the build, containerization, and deployment of a static web application using Jenkins, Docker, and AWS EC2.

The application is served using Nginx inside a Docker container and deployed automatically through a Jenkins pipeline.

---

## 🛠️ Tech Stack

* Jenkins (CI/CD)
* Docker
* Nginx (Web Server)
* AWS EC2
* GitHub
* HTML, CSS, JavaScript

---

## ⚙️ CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins pipeline is triggered
3. Jenkins pulls the latest code
4. Docker image is built using Nginx
5. Image is pushed to DockerHub
6. EC2 instance pulls the image
7. Application is deployed as a container

---

## 🏗️ Architecture

GitHub → Jenkins → Docker → DockerHub → AWS EC2 → Nginx → Web Application

---

## 📂 Project Structure

```
.
├── index.html
├── Dockerfile
├── Jenkinsfile
```

---

## 🐳 Docker Setup

### Build Image

```
docker build -t todo-app .
```

### Run Container

```
docker run -p 8080:80 todo-app
```

Access the application locally:

```
http://localhost:8080
```

---

## ⚡ Jenkins Pipeline Stages

* Clone Code
* Build Docker Image
* Login to DockerHub
* Push Docker Image
* Deploy to AWS EC2

---

## 🌐 Deployment

Application is deployed on AWS EC2 and can be accessed via:

```
http://<EC2-IP>
```

---

## 🔐 Prerequisites

* Docker installed
* Jenkins installed with required plugins
* AWS EC2 instance configured
* DockerHub account
* GitHub repository

---

## 🎯 Key Features

* Automated CI/CD pipeline
* Containerized static web application
* Deployment on AWS EC2 using Docker
* Lightweight Nginx server
* Pipeline as Code using Jenkinsfile

---

## 💡 Learnings

* CI/CD pipeline creation using Jenkins
* Docker image build and management
* Deployment automation on AWS EC2
* Nginx configuration for static hosting
* SSH-based remote deployment

---

## 🔥 Future Enhancements

* Kubernetes deployment
* AWS ECR integration
* GitHub Webhooks for auto-trigger
* HTTPS setup using Nginx
* Monitoring using Prometheus & Grafana

---

## 👨‍💻 Author

Narendraa Jeyaraman

---
