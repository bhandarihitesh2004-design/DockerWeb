pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'git@github.com:bhandarihitesh2004-design/DockerWeb.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t web-image-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -o 8090:80 web-image-app '
            }
        }
    }
}