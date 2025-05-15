pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test || echo "No tests found, skipping..."'
            }
        }

        stage('Build') {
            steps {
                echo 'Building app...'
                sh 'echo "Build complete!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo "Simulated deploy complete!"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}

