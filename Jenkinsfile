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
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
                // Add deployment steps here
            }
        }
    }
}