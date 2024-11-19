pipeline {
    agent any
    stages {
        stage("Build Backend Image") {
            steps {
                // Build backend Docker image
                script {
                    docker.build('backend-image', '-f backend/Dockerfile .')
                }
            }
        }
        stage("Build Frontend Image") {
            steps {
                // Build frontend Docker image
                script {
                    docker.build('frontend-image', '-f frontend/Dockerfile .')
                }
            }
        }
        stage("Build MongoDB Image") {
            steps {
                // Build MongoDB Docker image
                script {
                    docker.build('mongodb-image', '-f mongodb/Dockerfile .')
                }
            }
        }
        stage("Deploy") {
            steps {
                // Deploy using Docker Compose
                sh 'docker-compose up -d --build'
            }
        }
    }
}
