pipeline {
    agent any

    stages {
        stage ('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("danielmagalhaesnascimento/kube-news:v6", '-f .src/Dockerfile ./src')
                }
            }
        }
    }
}