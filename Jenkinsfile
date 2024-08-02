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
                // This step should not normally be used in your script. Consult the inline help for details.
                withDockerRegistry(credentialsId: 'crdes-dockerhub', url: '') {
                // some block
                    sh 'docker build -t anhly230722/web:latest .'
                    sh 'docker push anhly230722/web:latest'
                }
            }
        }
    }
}
