pipeline {
    agent any

    stages {
        stage('Pull Source Code') {
            steps {
                git branch: 'main', url: 'https://github.com/anugrahfitra/hextris.git'
            }
        }
        stage('Build Container Images') {
            steps {
                sh 'docker compose build'
            }
        }
        stage('Deploy Container Apps') {
            steps {
                sh 'docker compose up -d'
            }
        }
        stage('Push Image') {
            steps {
                sh 'docker compose push'
            }
        }
    }
}