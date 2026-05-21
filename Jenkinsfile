pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout scm
            }
        }
        stage('Build image') {
            steps {
                sh 'docker build -t myimage:latest .'
            }
        }
        stage('Push image') {
            steps {
                sh 'docker push myimage:latest'
            }
        }
    }
}
