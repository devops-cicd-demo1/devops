pipeline {
    agent any

    stages {

        stage('Check Docker') {
            steps {
                bat 'where docker'
                bat 'docker --version'
                bat 'docker compose version'
            }
        }

        stage('Pull Images') {
            steps {
                bat 'docker compose pull'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker compose up -d'
            }
        }

        stage('Verify') {
            steps {
                bat 'docker compose ps'
            }
        }

    }
}