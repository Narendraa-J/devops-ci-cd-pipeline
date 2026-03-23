# 🚀 CI/CD Pipeline for Static Web App (Jenkins, Docker & AWS)

## 📌 Project Overview
This project demonstrates an end-to-end CI/CD pipeline where a static To-Do application (HTML/CSS/JS) is containerized using Docker and automatically deployed to AWS EC2 using Jenkins.

## 🛠️ Tech Stack
* **CI/CD:** Jenkins
* **Containerization:** Docker
* **Web Server:** Nginx
* **Cloud:** AWS (EC2)
* **Source Control:** GitHub

## ⚙️ Workflow
1. Developer pushes code to **GitHub**.
2. **Jenkins** triggers the pipeline.
3. **Docker** builds a new image using Nginx.
4. Image is pushed to **DockerHub**.
5. Jenkins SSHs into **AWS EC2**, pulls the new image, and runs the container.

## 📂 Project Structure
* `index.html` - The To-Do application.
* `Dockerfile` - Instructions to build the Nginx container.
* `Jenkinsfile` - The automation script for the pipeline.
