pipeline {
    agent any
    stages {
        stage('Checkout the repo') {
            steps {
                checkout scm
            }
        }
        stage('Install dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Start the application') {
            steps {
                bat 'npm run start'
            }
        }
        stage('Run the tests') {
            steps {
                bat 'npm run test'
            }
        }
    }
}