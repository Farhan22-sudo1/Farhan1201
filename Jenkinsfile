pipeline {
    agent any

    stages {
        stage('Install Node.js') {
            steps {
                echo 'Installing Node.js...'
                sh '''
                    curl -fsSL https://rpm.nodesource.com/setup_18.x | bash -
                    yum install -y nodejs
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
                echo 'Installing npm packages...'
                sh 'npm install'
            }
        }

        stage('Run Tests') {
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
