pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git 'https://github.com/aditya-sridhar/simple-reactjs-app'
            }
        }
        
        // stage('Dependency Installation') {
        //     steps {
        //         // Install dependencies for frontend

        //         // bat 'npm install' // Assuming npm is used for dependency management

        //     }
        // }
        
        stage('Build Docker Image') {
            steps {
                // Build Docker image
                bat 'docker build -t myapp .'
            }
        }
        
        stage('Run Docker Image') {
            steps {
                // Run Docker image
                bat 'docker run -d -p 8080:80 myapp'
            }
        }
        
        stage('Push Docker Image') {
            steps {
                // Push Docker image to Docker Hub
                bat 'docker push rubabzahra/myapp:latest'
            }
        }
    }
}
