pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/Jawacar/HPE-POC-Jenkins.git'

            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t poc-jenkins-nginx .'
                sh 'docker images ls'
            }
        }
        stage('push Docker Image') {
            steps {
                sh 'docker push jawacarv/jawa-poc:poc-jenkins-nginx'
            }
        }
    }
}
