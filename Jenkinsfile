pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Pull Images') {
            steps {
                bat '"C:\\Users\\georg\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker-compose.exe" pull'
            }
        }

        stage('Deploy') {
            steps {
                bat '"C:\\Users\\georg\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker-compose.exe" up -d'
            }
        }

        stage('Verify') {
            steps {
                bat '"C:\\Users\\georg\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker-compose.exe" ps'
            }
        }

    }
}