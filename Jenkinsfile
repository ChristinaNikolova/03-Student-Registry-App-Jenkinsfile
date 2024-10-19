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
                    bat 'npm -v'
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