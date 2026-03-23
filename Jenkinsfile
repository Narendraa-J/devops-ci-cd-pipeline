pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "narendraa2311/todo-app:latest"
    }

    stages {

        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Clone Code') {
            steps {
                git 'https://github.com/Narendraa-J/devops-ci-cd-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Login to DockerHub') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'USER',
                    passwordVariable: 'PASS')]) {
                    sh 'echo $PASS | docker login -u $USER --password-stdin'
                }
            }
        }

        stage('Push Image') {
            steps {
                sh 'docker push $DOCKER_IMAGE'
            }
        }

        stage('Deploy to EC2') {
            steps {
                sh '''
                ssh -o StrictHostKeyChecking=no ec2-user@43.205.111.30 << EOF
                docker pull $DOCKER_IMAGE
                docker stop app || true
                docker rm app || true
                docker run -d -p 80:80 --name app $DOCKER_IMAGE
                EOF
                '''
            }
        }
    }
}