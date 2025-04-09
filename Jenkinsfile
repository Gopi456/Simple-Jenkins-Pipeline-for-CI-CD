pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                echo 'Building Docker Image...'
                sh 'docker build -t jenkins-demo-app:latest .'
            }
        }

        stage('Run Docker Container') {
            steps {
                echo 'Running Docker Container...'
                sh 'docker run -d -p 8080:8080 --name jenkins-demo-container jenkins-demo-app:latest'
            }
        }
    }
}
