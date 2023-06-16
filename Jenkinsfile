pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo/your-node-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('SAST Scan') {
            steps {
                sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebapp002 -Dsonar.organization=buggywebapp002 -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=59a7deca67268789983da4b436c23bc6e6517653'
            }
        }
    }
}
