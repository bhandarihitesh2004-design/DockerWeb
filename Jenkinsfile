pipeline {
    agent any
    
    environment {
        // Explicitly defining the absolute path to your Docker binary
        DOCKER = '/usr/local/bin/docker'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                // Using the variable instead of the bare 'docker' command
                sh '${DOCKER} build -t web-image-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                // Using the variable instead of the bare 'docker' command
                sh '${DOCKER} run -d -p 8090:80 web-image-app'
            }
        }
    }
}