pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git 'https://github.com/aditya-sridhar/simple-reactjs-app'
            }
        }

        stage('Build Docker Image') {
            steps {
                // Build Docker image
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Docker Image') {
            steps {
                // Run Docker image
                sh 'docker run -d -p 3000:3000 myapp'
            }
        }

        stage('Push Docker Image') {
            steps {
                // Push Docker image to Docker Hub
                sh 'docker push rubabzahra/myapp:latest'
            }
        }
    }
}
