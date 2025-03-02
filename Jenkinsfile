pipeline {
    agent any

    tools {
        nodejs 'NodeJS' // Ensure this matches the name in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/abdoul-sakhur/blogNext.git'
            }
        }

        stage('Check NodeJS Version') {
            steps {
                bat 'node -v'
                bat 'npm -v'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo "Deploying..."'
                // Add deployment steps here
            }
        }
    }
}