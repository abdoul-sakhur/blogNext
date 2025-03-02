pipeline {
    agent any

    tools {
        nodejs "NodeJS" // Ensure this matches the name in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/abdoul-sakhur/blogNext.git'
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

        stage('Test') {
            steps {
                sh 'npm test' // Add your test command if applicable
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "en cours de deploiement"'
                // Add deployment steps here (e.g., deploying to a server or cloud platform)
            }
        }
    }
}