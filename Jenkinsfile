pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('dckr_pat_XcBICYfBmEScNbNCmmmOxg8AFHQ')
    }
    stages {
        stage('Build and Push Docker Image') {
            steps {
                script {
                    docker.withRegistry('https://registry-1.docker.io', 'dckr_pat_XcBICYfBmEScNbNCmmmOxg8AFHQ') {
                        // Build and push Docker image commands
                        docker.build('myapp')
                        docker.image('myapp').push()
                    }
                }
            }
        }
    }
}

