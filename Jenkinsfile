pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/anhly23/job2.git'
            }
        }
        stage('Push Docker Hub'){
            steps{
                // This step should not normally be used in your script. Consult the inline help for details.
                withDockerRegistry(credentialsId: 'github', url:'') {
                // some block
                    sh label: '', script: 'docker build -t anhly2307/web:latest .'
                    sh label: '', script: 'docker push -t anhly2307/web:latest'
                }
            }
        }
    }
}
