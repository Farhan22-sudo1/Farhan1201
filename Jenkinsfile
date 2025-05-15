pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repo...'
                checkout scm
            }
        }

        stage('Fake Install') {
            steps {
                echo 'Pretending to install dependencies...'
                sh 'echo "npm install successful"'
            }
        }

        stage('Fake Test') {
            steps {
                echo 'Pretending to run tests...'
                sh 'echo "All tests passed ✅"'
            }
        }

        stage('Fake Build') {
            steps {
                echo 'Pretending to build app...'
                sh 'echo "Build complete 🎉"'
            }
        }

        stage('Fake Deploy') {
            steps {
                echo 'Pretending to deploy app...'
                sh 'echo "Deployed to production 🚀"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline simulation completed.'
        }
    }
}
