pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/anhly23/job2.git'
            }
        }
        stage('Build and Push Docker Image') {
            steps {
                withDockerRegistry(credentialsId: 'crdes-dockerhub', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t anhly230722/web:latest .'
                    sh 'docker push anhly230722/web:latest'
                }
            }
        }
    }
}
