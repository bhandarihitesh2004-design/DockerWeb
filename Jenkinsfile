pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t web-image-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8090:80 web-image-app'
            }
        }
    }
}