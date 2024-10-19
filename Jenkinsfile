pipeline {
    agent any
    stages {
        stage('Checkout the repo') {
            steps {
                checkout scm
            }
        }
        stage('Set up Node.js') {
            steps {
                script {
                    bat 'nvm install 20.x'
                    bat 'nvm use 20.x'
                 }
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