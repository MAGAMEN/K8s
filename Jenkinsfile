pipeline {
    agent any

    stages {
        stage ('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("danielmagalhaesnascimento/kube-news:${env.BUILD.ID}", '-f .src/Dockerfile ./src')
                }
            }
        }
    }
}