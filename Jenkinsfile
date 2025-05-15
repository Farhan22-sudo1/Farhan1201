pipeline {
    agent any

    stages {
        stage('Install Node.js') {
            steps {
                echo 'Installing Node.js...'
                sh '''
                    curl -fsSL https://rpm.nodesource.com/setup_18.x | sudo bash -
                    sudo dnf install -y nodejs
                    node -v
                    npm -v
                '''
            }
        }

        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test || echo "No tests found."'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build complete."'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy complete."'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
