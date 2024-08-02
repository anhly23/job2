pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/anhly23/job2.git'
            }
        }
    }
}
