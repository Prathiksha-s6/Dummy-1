pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git "https://github.com/Prathiksha-s6/Dummy-1.git"
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t dummy-image .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8080:80 dummy-image'
            }
        }
    }
}