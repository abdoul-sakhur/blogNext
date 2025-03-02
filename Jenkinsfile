pipeline {
    agent any
    environment {
        NODE_VERSION = "20"  // Adapter à ta version souhaitée
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/abdoul-sakhur/blogNext.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    def nodejsHome = tool name: 'NodeJS', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
                    env.PATH = "${nodejsHome}/bin:${env.PATH}"
                }
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
                sh 'npm run start &'
            }
        }
    }
}
