pipeline {
    agent any

    stages {
        stage ('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("danielmagalhaesnascimento/kube-news:v5", '-f ./src/Dockerfile ./src')
                }
            }
        }
        stage ('Push Docker image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub')
                        dockerapp.push('latest')
                        dockerapp.push("v5")
                }
            }
        }
    }
}

